[product-zone-design-system.md](https://github.com/user-attachments/files/25614044/product-zone-design-system.md)
# Product.Zone Design System
## Reference Document — February 2026

**What this is:** The complete design language extracted from the homepage, Buying Path X-RAY page, and Agency Partners page. Use this as the reference for any new surface — landing pages, sales pages, one-pagers, email templates.

**Canonical source:** `xray-landing-v12.html` is the most complete and correct implementation. When in doubt, defer to that file.

**Known inconsistency:** The original partners page draft (`partners.html`, `partners-v2.html`) uses Inter instead of the canonical font stack. Any future page should use the X-RAY system below, not the Inter system.

---

## 1. Tokens

### Color

```css
:root {
  /* Dark backgrounds */
  --black:    #0a0a0a;   /* Page background */
  --dark:     #111111;   /* Alternate dark section */
  --surface:  #141414;   /* Cards on dark */
  --surface2: #1c1c1c;   /* Secondary cards, timeline labels */
  --border:   #2a2a2a;   /* Dark section borders */

  /* Light backgrounds */
  --light:    #F5F4EF;   /* Primary light section bg */
  --light2:   #ECEAE3;   /* Alternating light, table rows */
  --lborder:  #D8D6CF;   /* Light section borders */
  --ltext:    #1a1a1a;   /* Primary text on light */
  --lmuted:   #555555;   /* Body text on light */
  --lmuted2:  #888888;   /* Labels, captions on light */

  /* Brand accents */
  --orange:   #F5A623;   /* Primary CTA, prices, highlights */
  --teal:     #33C4D9;   /* Secondary accent, investor lens */
  --green:    #7ED49A;   /* Positive outcomes, "after" states */
  --red:      #FF6B6B;   /* Broken states, risk signals */
  --yellow:   #E8C85A;   /* Fuzzy/warning states */

  /* Text on dark */
  --white:    #F0EFE9;   /* Primary text on dark */
  /* Muted on dark: use literal #999, #aaa, #777, #555 */
}
```

**Usage rules:**
- Orange is the only CTA color. All primary buttons, prices, and key callouts use `--orange`.
- Teal is the investor/VC lens color and secondary proof signals. Never use it for primary CTAs.
- Green/Red/Yellow are exclusively status indicators (CLEAR / MISSING / FUZZY). Do not use for decoration.
- Dark and light sections alternate to create visual rhythm. Never stack two light sections or two dark sections in a row without a visual reason.

---

### Typography

```css
:root {
  --mono:    'Space Mono', monospace;         /* Labels, eyebrows, codes, nav */
  --display: 'Barlow Condensed', sans-serif;  /* Headlines, large numbers */
  --body:    'Barlow', sans-serif;            /* Body copy, UI text */
}
```

**Google Fonts import:**
```
https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Barlow+Condensed:wght@400;600;700;800;900&family=Barlow:wght@400;500;600&display=swap
```

**Font roles:**

| Font | Used for | Never used for |
|------|----------|---------------|
| Space Mono | Nav links, section labels, eyebrows, monospace data, CTAs, footer | Headlines, body copy |
| Barlow Condensed | All headlines (H1–H4), large proof numbers, pricing amounts | Body copy, labels |
| Barlow | Body paragraphs, card text, descriptions | Headlines, labels |

---

### Type Scale

```css
/* Headlines — always Barlow Condensed, font-weight 900, uppercase */
.h-xl  { font-size: clamp(40px, 7.5vw, 72px); line-height: 0.93; letter-spacing: -0.01em; }
.h-lg  { font-size: clamp(28px, 5.5vw, 52px); line-height: 0.97; letter-spacing: -0.01em; }
.h-md  { font-size: clamp(22px, 3.8vw, 36px); line-height: 1.05; }
.h-sm  { font-size: clamp(18px, 2.5vw, 24px); line-height: 1.1; }

/* Body — Barlow */
.body-lg { font-size: 18px; line-height: 1.7; }
.body-md { font-size: 15px; line-height: 1.7; }
.body-sm { font-size: 13px; line-height: 1.6; }

/* Labels — Space Mono, uppercase, tracked */
/* Standard: font-size: 10–11px; letter-spacing: 0.10–0.14em; text-transform: uppercase */
```

**Headline rules:**
- All headlines: `text-transform: uppercase`
- Line height always tight: 0.93–1.05 (not 1.4–1.6 like body)
- Letter spacing: `-0.01em` on large display headings, `0` on smaller
- Max-width: headlines never run full container width — cap at 780px for H1, 640px for H2

**Body copy rules:**
- Light sections: `color: var(--lmuted)` (#555) for body, `color: var(--ltext)` (#1a1a1a) for strong/emphasis
- Dark sections: `color: #999` or `#aaa` for body, `color: var(--white)` for strong/emphasis
- Max-width: body paragraphs never exceed 640px (prevents overly long line length)

---

## 2. Layout

### Container

```css
.wrap { max-width: 960px; margin: 0 auto; padding: 0 clamp(20px, 5vw, 48px); }
```

Single container width across all pages. Fluid padding with clamp — never fixed pixel padding on mobile.

### Section Padding

```css
.section { padding: clamp(48px, 8vw, 80px) 0; }
```

All sections use the same vertical rhythm. No section should have tighter padding unless it's a connecting strip.

### Section Types

```css
.section-dark  { background: var(--black); }   /* Most common: dark primary */
.section-mid   { background: var(--dark); }    /* Secondary dark: slightly lighter */
.section-light { background: var(--light); color: var(--ltext); }  /* Light breakout */
```

**Alternation pattern used across X-RAY page:**
```
Dark  → hero, problem recognition
Light → reframe / root cause
Dark  → zones / system explanation
Light → deliverables / what you get
Dark  → timeline / process
Light → proof cases / evidence
Dark  → dual audience / CTA
Light → FAQ
Dark  → final CTA
```

The contrast between dark and light sections is a primary design tool — it creates pacing and signals a shift in content type. Problem sections are dark. Clarity/output sections are light.

---

## 3. Navigation

```css
.nav {
  position: sticky; top: 0; z-index: 100;
  background: rgba(10,10,10,0.96);
  border-bottom: 1px solid var(--border);
  backdrop-filter: blur(10px);
  height: 52px;
}
.nav-logo  { font-family: var(--mono); font-size: 11px; color: #777; letter-spacing: 0.05em; }
.nav-logo span { color: var(--orange); }  /* The dot in Product.Zone */
.nav-link  { font-family: var(--mono); font-size: 10px; color: #555; text-transform: uppercase; letter-spacing: 0.12em; }
.nav-cta   { font-family: var(--mono); font-size: 10px; color: var(--black); background: var(--orange);
             padding: 7px 14px; text-transform: uppercase; letter-spacing: 0.1em; font-weight: 700; }
```

**Rules:**
- Nav CTA is always orange, no border-radius (square corners throughout)
- Logo renders as text in Space Mono — no image dependency
- Nav links hidden at ≤480px. CTA always visible.
- No dropdown menus. Nav links go directly to product pages.

---

## 4. Buttons

Three button styles. All use Space Mono. No border-radius.

```css
/* Primary — orange fill */
.btn-primary {
  font-family: var(--mono); font-size: 11px; font-weight: 700;
  color: var(--black); background: var(--orange);
  padding: 13px 24px; text-transform: uppercase; letter-spacing: 0.1em;
  text-decoration: none; display: inline-block;
}

/* Secondary — bordered ghost */
.btn-secondary {
  font-family: var(--mono); font-size: 11px;
  color: #888; border: 1px solid var(--border);
  padding: 13px 24px; text-transform: uppercase; letter-spacing: 0.1em;
  text-decoration: none; display: inline-block;
}
.btn-secondary:hover { color: var(--white); border-color: #555; }

/* Ghost text link */
.btn-ghost { color: #888; font-family: var(--mono); font-size: 11px; text-decoration: none; }
.btn-ghost:hover { color: var(--white); }
```

**Usage rules:**
- One primary CTA per section. Never two orange buttons side by side.
- Secondary buttons are always directional (scroll anchors, "see how it works") — not conversion CTAs.
- CTA copy always ends with `→` or ` ↓` — directional arrows are part of the language.
- Button copy is imperative, short: "Book the X-RAY →", "See how it works ↓". Never passive.

---

## 5. Section Labels (Eyebrows)

```css
.section-label {
  font-family: var(--mono); font-size: 10px; text-transform: uppercase;
  letter-spacing: 0.14em; margin-bottom: 32px;
  display: flex; align-items: center; gap: 14px;
}
/* Extends with a horizontal rule to the right */
.section-label::after { content: ''; flex: 1; height: 1px; }

/* On dark sections */
.section-label { color: #555; }
.section-label::after { background: var(--border); }

/* On light sections */
.section-label { color: var(--lmuted2); }
.section-label::after { background: var(--lborder); }

/* Accent variants */
.section-label.teal   { color: var(--teal); }
.section-label.orange { color: var(--orange); }
.section-label.red    { color: var(--red); }
```

**Usage rules:**
- Every section opens with a section-label above the H2. No section should begin cold with a headline.
- Label text is 2–5 words, describes the purpose of the section from the reader's perspective: "What this reveals", "The situation you recognise", "How it works".
- Accent colors (teal, orange, red) signal the emotional register of the section. Orange = action/priority. Teal = investor/VC. Red = broken/problem state.

---

## 6. Core Components

### Card (Dark Surface)

```css
.capability-card {
  background: var(--surface); border: 1px solid var(--border);
  padding: 32px; display: flex; flex-direction: column;
}
/* Top label */
.capability-num { font-family: var(--mono); font-size: 9px; color: #555;
                  text-transform: uppercase; letter-spacing: 0.12em; margin-bottom: 10px; }
/* Card headline */
.capability-title { font-family: var(--display); font-size: 22px; font-weight: 800;
                    text-transform: uppercase; color: var(--white); line-height: 1.1; margin-bottom: 12px; }
/* Body */
.capability-body { font-size: 14px; color: #aaa; line-height: 1.65; margin-bottom: 14px; }
/* Teal proof strip inside card */
.capability-proof { font-family: var(--mono); font-size: 10px; color: var(--teal); line-height: 1.5;
                    padding: 10px 12px; background: rgba(51,196,217,0.05);
                    border-left: 2px solid rgba(51,196,217,0.3); }
/* Footer label */
.capability-artifact { font-family: var(--mono); font-size: 10px; color: var(--orange);
                       text-transform: uppercase; letter-spacing: 0.1em;
                       padding-top: 16px; border-top: 1px solid var(--border); margin-top: auto; }
```

### Card (Light Surface)

```css
.proof-card { background: #fff; border: 1px solid var(--lborder); padding: clamp(24px,4vw,36px); }
/* Alternating: every even card uses var(--light2) background */
```

### Highlighted Call-out Block (Light)

Used for pivots and reframes — the moment where the problem is restated as a solution.

```css
.pattern-pivot {
  padding: 36px 44px;
  border-left: 3px solid var(--orange);
  background: var(--light2);
}
.pattern-pivot-text {
  font-family: var(--display); font-size: clamp(26px,3.5vw,34px);
  font-weight: 800; text-transform: uppercase; line-height: 1.1;
  color: var(--ltext);
}
.pattern-pivot-text span { color: var(--orange); }
```

### Scorecard Status Tokens

Used in zone scorecards, diagnostic tables, portfolio dashboards.

```css
.z-clear   { font-family: var(--mono); font-size: 10px; color: var(--green); }  /* ● CLEAR */
.z-fuzzy   { font-family: var(--mono); font-size: 10px; color: var(--yellow); } /* ◐ FUZZY */
.z-missing { font-family: var(--mono); font-size: 10px; color: var(--red); }    /* ○ MISSING */
```

**Always rendered in Space Mono.** Status labels are always one word: CLEAR, FUZZY, MISSING. Never "Good", "Okay", "Bad".

### Timeline / Process Row

```css
.timeline { border: 1px solid var(--border); }
.timeline-row {
  display: grid;
  grid-template-columns: clamp(72px, 12vw, 120px) 1fr clamp(72px, 12vw, 120px);
  border-bottom: 1px solid var(--border);
}
.timeline-phase {
  background: var(--surface2); border-right: 1px solid var(--border);
  font-family: var(--mono); font-size: 10px; color: var(--orange);
  text-transform: uppercase; letter-spacing: 0.1em;
}
.timeline-time { border-left: 1px solid var(--border);
                 font-family: var(--mono); font-size: 11px; color: #777; }
.timeline-time.active { color: var(--teal); }
.timeline-time.zero   { color: #444; }
```

The three-column grid (label | content | time) is the standard for any sequential process. Never use bullet lists for process steps — always this table format.

### Proof Case Block

Standard structure for client case studies:

```
[Header: company name + big result number]
[Three columns: Before | After | How it ran]
[Footer: quote + attribution]
```

Before column uses `—` prefix in Space Mono. After column uses `✓` in green. Timeline column uses `background: var(--surface2)` and Courier New monospace.

### Dual Lens Card

For founder vs investor audience splits:

```css
.dual-card.founder  { border-left: 3px solid var(--teal); }
.dual-card.investor { border-left: 3px solid var(--orange); }
```

Teal always = VC/investor lens. Orange always = founder lens. This is a fixed convention — do not reverse.

---

## 7. Responsive Breakpoints

```css
/* Tablet: ≤ 768px */
@media (max-width: 768px) {
  /* Two-column grids → single column */
  /* Nav links: reduce font size to 9px, reduce gaps */
  /* Timeline: compress column widths */
  /* Portfolio table: reduce font size, tighter padding */
  /* CTA path grid → 2 columns */
}

/* Mobile: ≤ 480px */
@media (max-width: 480px) {
  /* Nav links: hide entirely. Keep logo + CTA only. */
  /* Section padding: 40px 0 */
  /* Zone strip → single column */
  /* All multi-column grids → single column */
  /* Scorecard detail column (sc-note) → display: none */
}
```

**Rules:**
- Mobile nav: logo + CTA only. Nav links collapse completely.
- No horizontal scroll on mobile except portfolio comparison table (min-width 560px on the inner table).
- All `clamp()` values handle the middle range — no need for tablet-specific font-size overrides.
- Touch target minimum: 44px height on all interactive elements.

---

## 8. Section Architecture

The standard section sequence for a Product.Zone sales page. Not every section is required — this is the full menu, in order.

| Section | Background | Purpose |
|---------|-----------|---------|
| Hero | Dark | Name the problem, establish who it's for, primary CTA |
| Familiar pain | Dark | Numbered rows of situations the reader recognises |
| Root cause (light) | Light | Reframe: what's actually happening. Ends with pivot block. |
| System / zones | Dark or Light | Explain the framework underlying the solution |
| Deliverables | Light | What you get — instruments, not reports |
| Process / timeline | Dark | How it runs — sequential, timed, transparent |
| Proof cases | Light | Evidence. 1–3 cases. Before / After / How it ran format. |
| Dual audience | Dark | If serving two audiences — show both lenses explicitly |
| FAQ | Light | 4–8 questions. Pre-answers the objections not raised. |
| Final CTA | Dark | One clear action. Price visible. Timeline visible. |

**Compression rule:** The architecture lives behind the curtain. The output surfaces it. Sections show outcomes and instruments — not methodology names and internal frameworks.

---

## 9. Copy Conventions

**Voice:**
- Direct, no throat-clearing. First sentence does work.
- Peer-to-peer, not consultant-to-client. "You" not "companies like yours".
- Plain English. ESL-safe. No jargon that isn't explained.
- Lowercase for casual connectors: "and", "or", "but" — never mid-sentence capitalisation for emphasis.

**Headline pattern:**
- H1 hero: States the problem or the reframe. Never the product name.
- H2 section: States what the section proves or shows. Never a question.
- All uppercase, tight line height, orange accent on the key phrase.

**CTA copy:**
- Always ends with `→`
- Imperative verb: Book, Start, Run, See, Download
- Never: "Learn more", "Get started", "Click here"
- Primary CTA names the specific thing: "Book the X-RAY →", not "Get in touch →"

**Proof / evidence:**
- Numbers before context: "15 decisions locked" not "we locked 15 decisions"
- Results in before/after format — not narrative descriptions
- Quote attribution always: Name, Title, Company. Never anonymous.
- Caveat any unverified or VC-reported outcome: small Space Mono text below the result.

**Labels / eyebrows:**
- 2–5 words. Situation description, not section title.
- Good: "The situation you recognise" / "What this reveals" / "How it runs"
- Bad: "About" / "Features" / "Our Process"

---

## 10. Known Inconsistency to Resolve

The partners page (`partners.html`, `partners-v2.html`) was built with Inter instead of the canonical font stack. This creates a visible brand inconsistency if a visitor moves between the X-RAY page and the partners page.

**To fix:** Replace Inter with Barlow + Barlow Condensed + Space Mono on the partners page. The structural decisions (sections, card layouts, colors) are correct — it's only the font stack that needs updating.

The homepage (Framer) uses a different implementation but should be considered the source of truth for the logo, OG image, and meta copy. HTML prototypes align to the homepage's visual identity, not the other way around.

---

*Extracted from: xray-landing-v12.html, partners-v2.html, partners.html*
*Product.Zone · Make A Difference Ventures B.V. · Amsterdam · February 2026*
