# Buying Path Diagnostic Framework v3.2
## Surface-First Outside-In Diagnostic System

**Purpose:** Systematic GTM diagnostic starting with what's observable  
**Design:** Surface audit → Decision inference → Indicator validation → Results proof  
**Version:** 3.2 — February 2026

---

## Framework Philosophy

### **The Core Insight**

From the outside, GTM problems look like **stalled buyer momentum**:
- Deals that should close but don't
- Buyers who engage then ghost
- Pipeline that fills but doesn't convert

From the inside, they trace to **missing or fuzzy decisions**:
- Category unclear → buyer can't place you
- Alternative unnamed → no urgency
- Buyer economics unknown → pricing feels random

**The diagnostic maps the gap:**  
What the buyer experiences (momentum breaking) ← traces to → What the founder hasn't locked (decision missing)

---

### **Diagnostic Flow Inverted**

**Conceptual Model (How it works):**
```
Decisions → Surfaces → Indicators → Results
```
What powers what.

**Diagnostic Flow (How we discover):**
```
Surface Audit → Decision Inference → Indicator Validation → Results Proof
```
What we can SEE reveals what's MISSING.

**Start with what's observable (surfaces), not what's invisible (decisions in founder's head).**

---

### **Why Surface-First Works**

**Traditional approach (inside-out):**
- Ask founder "What's your category?"
- Founder says "We're AI-powered X for Y teams"
- Sounds reasonable in conversation
- BUT homepage says something completely different
- Founder THINKS decision is locked, but surface proves it's fuzzy

**Surface-first approach (outside-in):**
- Pull up homepage
- Ask "Does this answer: What is this?"
- Score: Explicit / Partial / Missing
- If missing → Category decision is NOT locked, regardless of what founder says
- Surface audit reveals truth, not founder's belief

**Surfaces don't lie. Decisions are invisible. Start with what's real.**

---

### **Outside-In Principle**

Every decision must be stated from **buyer perspective**, not seller operations.

**Wrong (inside-out):**
- "Our pricing model is seat-based"
- "Our primary channel is outbound"
- "Our sales motion is enterprise"

**Right (outside-in):**
- "What does buyer currently pay for alternatives?"
- "Where does buyer search when they have this problem?"
- "How does buyer approve purchases in this category?"

**Test:** If decision doesn't describe buyer experience/behavior, it's inside-out.

---

### **Both/And Indicators**

**Qualitative (high fidelity, low scale):**
- Observed in calls, emails, buyer behavior
- Example: "Buyer repeats value back accurately"
- Track: Manual observation, call notes

**Quantitative (lower fidelity, high scale):**
- Measured systematically, real-time
- Example: "Homepage bounce rate <50%"
- Track: PostHog, email tools, CRM

**Use BOTH for complete picture.**

---

### **Implementability Standard**

**Every indicator must pass the test:**
1. Can I measure this in <24 hours?
2. Do I know which tool to use?
3. Do I know what "good" looks like?
4. Can I set this up in <30 minutes?

**If no to any → not implementable → not in framework.**

---

## Zone Clusters

```
PRIMARY ZONES (Zones 1-5)
Every venture needs these, in sequence.
Run in every diagnostic session.

EXPANSION ZONES (Zones 6-10)
Triggered by specific conditions or stage.
Run when primary path is working OR specific symptom appears.
```

---

## Health Scoring

**Per Zone (0-15 points):**
```
🟢 GREEN (12-15 points): Decisions locked, indicators positive
   - Decisions: 80-100% locked
   - Qualitative: 70%+ positive signals, <20% negative
   - Quantitative: Meet/exceed thresholds

🟡 YELLOW (8-11 points): Decisions fuzzy, indicators mixed
   - Decisions: 60-80% locked
   - Qualitative: 40-70% positive signals
   - Quantitative: Below threshold but improving

🔴 RED (0-7 points): Decisions missing, indicators negative
   - Decisions: <60% locked
   - Qualitative: <40% positive, >40% negative
   - Quantitative: Far below threshold
```

**Overall Health (0-75 points):**
- 60-75 (80%+): Strong foundation
- 45-59 (60-80%): Fixable gaps
- 30-44 (40-60%): Major intervention needed
- <30 (<40%): Crisis mode

---

# SURFACE AUDIT METHODOLOGY

## The Diagnostic Principle

**Start with what you can SEE, not what founder SAYS.**

Every surface has JOBS it must do for the buyer. If surface doesn't do the job, buyer experience breaks — regardless of what decisions founder believes they've made.

**Surface audit answers:**
1. Which buyer questions does this surface answer?
2. How well does it answer them? (Explicit / Partial / Missing)
3. Which decisions are fuzzy/missing based on surface gaps?

**Then validate with indicators and results.**

---

## How Surface Jobs Frameworks Work

**Each surface framework defines:**
- **Buyer questions:** What must buyer understand at this moment?
- **Decision mapping:** Which decisions answer which questions?
- **Scoring criteria:** Explicit / Partial / Missing definitions
- **Inference rules:** Surface gaps → Decision gaps

**We've proven this for Homepage. Build others as needed.**

---

## Homepage Jobs Framework (Proven Example)

### **15 Buyer Questions Across 6 Stages**

**LAND (2 questions):**

**Q1: What is this? (3-second read)**
- Maps to: Category decision
- Explicit: Category name visible in hero ("AI copilot for X")
- Partial: Vague description ("intelligent platform")
- Missing: No category frame at all
- Score: ⬜ Explicit / Partial / Missing

**Q2: What category is this in?**
- Maps to: Category decision
- Explicit: Bucket clear ("replaces spreadsheets")
- Partial: Category implied but not named
- Missing: Buyer can't place this
- Score: ⬜ Explicit / Partial / Missing

---

**MAKE SENSE (2 questions):**

**Q3: What pain is worth a switch?**
- Maps to: Outcome decision + Alternative decision
- Explicit: Specific pain stated ("spreadsheets break at scale")
- Partial: Generic pain ("make better decisions")
- Missing: No pain mentioned
- Score: ⬜ Explicit / Partial / Missing

**Q4: Why does this matter now?**
- Maps to: Alternative decision (why it fails today)
- Explicit: Trigger event clear ("AI makes old tools obsolete")
- Partial: Urgency implied but not explicit
- Missing: No "why now"
- Score: ⬜ Explicit / Partial / Missing

---

**SELECT (2 questions):**

**Q5: Is this for my team?**
- Maps to: Customer decision (ICP boundary)
- Explicit: Role + company type named ("for R&D teams at tech companies")
- Partial: Too broad ("for companies")
- Missing: No ICP mentioned
- Score: ⬜ Explicit / Partial / Missing

**Q6: Do I see my use case?**
- Maps to: Customer decision + Outcome decision
- Explicit: Specific use case shown ("analyze experiment data")
- Partial: Generic use case ("process data")
- Missing: No use case
- Score: ⬜ Explicit / Partial / Missing

---

**COMPARE (3 questions):**

**Q7: Do I understand the approach?**
- Maps to: Approval Criteria decision (how it works differently)
- Explicit: Mechanism clear ("AI replaces manual analysis")
- Partial: Capability list ("AI-powered")
- Missing: No approach explanation
- Score: ⬜ Explicit / Partial / Missing

**Q8: What result do I get?**
- Maps to: Outcome decision
- Explicit: Measurable result ("10x faster analysis")
- Partial: Aspiration ("better decisions")
- Missing: No outcome stated
- Score: ⬜ Explicit / Partial / Missing

**Q9: Why you vs what I use today?**
- Maps to: Alternative + Approval Criteria decisions
- Explicit: Alternative named + difference clear ("replaces Excel, 10x faster")
- Partial: Difference stated but alternative not named
- Missing: No comparison at all
- Score: ⬜ Explicit / Partial / Missing

---

**VALIDATE (3 questions):**

**Q10: Does it work for real teams?**
- Maps to: Proof type decision
- Explicit: Customer case with metrics ("Acme reduced time by 60%")
- Partial: Customer logo only, no story
- Missing: No proof
- Score: ⬜ Explicit / Partial / Missing

**Q11: Can I trust the decision?**
- Maps to: Proof type + Primary risk decisions
- Explicit: Risk addressed ("enterprise security, SOC 2")
- Partial: Generic trust signal ("trusted by Fortune 500")
- Missing: No trust elements
- Score: ⬜ Explicit / Partial / Missing

**Q12: How much effort is this?**
- Maps to: First value path + Time to value decisions
- Explicit: Timeline clear ("results in 10 minutes, no setup")
- Partial: Effort implied ("easy to use")
- Missing: No effort preview
- Score: ⬜ Explicit / Partial / Missing

---

**COMMIT (3 questions):**

**Q13: How do we start, exactly?**
- Maps to: First step decision
- Explicit: Safe first step clear ("Book 15-min demo, no commitment")
- Partial: CTA exists but unclear ("Request demo")
- Missing: No clear next step
- Score: ⬜ Explicit / Partial / Missing

**Q14: What happens after I book?**
- Maps to: Activation moment + First value path decisions
- Explicit: Post-booking path clear ("We'll show you X, you'll see Y in 10 min")
- Partial: Vague onboarding ("We'll get you started")
- Missing: No activation preview
- Score: ⬜ Explicit / Partial / Missing

**Q15: Does this feel low-risk to try?**
- Maps to: Primary risk + First step decisions
- Explicit: Risk reversal clear ("14-day trial, cancel anytime")
- Partial: Low commitment implied
- Missing: No risk mitigation
- Score: ⬜ Explicit / Partial / Missing

---

### **Homepage Audit Scoring**

**Count by status:**
- Explicit: __/15 (question answered clearly on page)
- Partial: __/15 (question answered but requires inference)
- Missing: __/15 (question not answered at all)

**Thresholds:**
- 🟢 Green: 12+ explicit, <3 missing
- 🟡 Yellow: 8-11 explicit, 3-7 missing
- 🔴 Red: <8 explicit, >7 missing

**Example from diagnostic:**
- Explicit: 2/15
- Partial: 11/15
- Missing: 2/15
- **Status: 🔴 RED**

---

### **Decision Inference from Homepage Audit**

**Based on homepage gaps, infer which decisions are fuzzy/missing:**

**Common inference patterns:**

| Homepage Gap | Decision Inference |
|--------------|-------------------|
| Q1-2 partial/missing | Category decision FUZZY or MISSING |
| Q3-4 partial/missing | Outcome + Alternative decisions FUZZY |
| Q5-6 partial/missing | Customer decision FUZZY |
| Q7 partial/missing | Approval Criteria decision FUZZY |
| Q8 partial/missing | Outcome decision FUZZY |
| Q9 missing | Alternative decision MISSING |
| Q10-11 partial/missing | Proof type decision FUZZY |
| Q12 partial/missing | First value path + Time to value FUZZY |
| Q13 partial/missing | First step decision FUZZY |
| Q14 missing | Activation moment MISSING |
| Q15 partial/missing | Primary risk decision FUZZY |

**Example inference:**
```
Homepage scored: 2 explicit, 11 partial, 2 missing

Inference:
- Q1-2 partial → Category: FUZZY
- Q5-6 partial → Customer: FUZZY  
- Q9 missing → Alternative: MISSING
- Q10-11 partial → Proof type: FUZZY
- Q12 partial → First value path: FUZZY
- Q14 missing → Activation moment: MISSING
- Q15 partial → First step: FUZZY

Preliminary Zone 1 score: 2/12 explicit → RED
```

**Then validate this inference with indicators and results.**

---

## Template: Building Surface Jobs Frameworks

**For any new surface, follow this structure:**

### **Step 1: Identify the buyer moment**
When/where does buyer encounter this surface?  
Example: "Buyer opens pitch deck for first time in meeting"

### **Step 2: List buyer questions at this moment**
What must buyer understand to proceed?  
Example: 
- "What is this?" (slide 1)
- "Is this for me?" (slide 2)
- "What's the proof?" (slide 3)

### **Step 3: Map to Zone 1 decisions**
Which decisions answer which questions?  
Example: 
- Q1 "What is this?" → Category decision
- Q2 "Is this for me?" → Customer decision
- Q3 "What's the proof?" → Proof type decision

### **Step 4: Define scoring criteria**
Explicit / Partial / Missing for each question  
Example:
- Explicit: Category name in slide 1 title
- Partial: Category implied but not stated
- Missing: No category frame

### **Step 5: Test in real diagnostics**
Does this framework reveal actual gaps?  
Adjust based on what you learn.

---

### **Priority Surface Frameworks to Build Next**

**After proving homepage framework works:**

**High priority (next to build):**
1. **Pitch deck (first 5 slides)** — 7-10 questions
   - Buyer moment: First time seeing deck in meeting
   - Questions: Category, customer, problem, solution, proof, next step
   
2. **Outbound email (first message)** — 4-5 questions
   - Buyer moment: Inbox, 3-second scan
   - Questions: Trigger relevance, credibility, value hint, safe ask

**Medium priority (build if needed):**
3. **Demo recording (first 3 min)** — 5-7 questions
4. **Sales call script (first 15 min)** — 6-8 questions

**Low priority (build only if triggered):**
5. **One-pager** — 8-10 questions
6. **Champion deck** — 6-8 questions

**Don't build all at once. Build as diagnostics reveal need.**

---

# ZONE 1: BUYABILITY

**Can the right buyer understand and want this in under 90 seconds?**

---

## Zone Job

Make the intended buyer immediately grasp:
- What this is (category)
- Who it's for (customer)
- What it replaces (alternative)
- Why it wins (approval criteria)
- What changes (outcome)
- What happens next (activation preview)

**If this fails, everything downstream is noise.**

---

## Outside-In Buyer Question

> **"What is this — and why should I care?"**

*Listen for: clarity on category, customer, alternative, approval criteria, outcome, proof, first step, and activation preview from BUYER perspective.*

---

## Decisions (Must Be Explicitly Locked)

### **Positioning Decisions (Buyer Mental Model):**

| Decision | What It Locks | Status |
|----------|--------------|--------|
| **Category** | What bucket the buyer places you in — job + context + name | ⬜ LOCKED / FUZZY / MISSING |
| **Customer** | Who this is specifically for (from buyer self-selection view) | ⬜ LOCKED / FUZZY / MISSING |
| **Alternative** | What buyer uses today + why it fails for the job | ⬜ LOCKED / FUZZY / MISSING |
| **Approval Criteria** | Why buyer chooses THIS over alternative (buyer's decision criteria, not internal mechanism) | ⬜ LOCKED / FUZZY / MISSING |
| **Outcome** | What the buyer can NOW do that they couldn't before | ⬜ LOCKED / FUZZY / MISSING |

### **Trust Decisions (Buyer Belief):**

| Decision | What It Locks | Status |
|----------|--------------|--------|
| **Proof type** | What evidence makes this believable to THIS buyer | ⬜ LOCKED / FUZZY / MISSING |
| **Proof moments** | What buyer must see in 90 seconds to believe | ⬜ LOCKED / FUZZY / MISSING |
| **Primary risk** | What feels unsafe about committing (from buyer view) | ⬜ LOCKED / FUZZY / MISSING |

### **Movement Decisions (Buyer Action):**

| Decision | What It Locks | Status |
|----------|--------------|--------|
| **First step** | Smallest move that feels safe TO buyer (decision de-risking, not "try product") | ⬜ LOCKED / FUZZY / MISSING |

### **Activation Projection (Buyer Needs to Visualize "What Happens Next"):**

| Decision | What It Locks | Status |
|----------|--------------|--------|
| **Activation moment** | What buyer sees as "aha" when they first use this | ⬜ LOCKED / FUZZY / MISSING |
| **First value path** | What buyer does to get first value (steps 1-3) | ⬜ LOCKED / FUZZY / MISSING |
| **Time to value** | How fast buyer sees results (hours/days/weeks) | ⬜ LOCKED / FUZZY / MISSING |

**Why Activation in Zone 1 (not Zone 6):**

Buyer won't commit unless they can visualize what happens after "yes." These aren't full Using Engine decisions (which come later in Zone 6 for actual activation), but **projections** that must be visible in buying materials. Buyer needs to see the path before walking it.

**Example signals:**
- ✅ Clear: "After signup, you'll import your data (5 min), run your first analysis (click one button), and see results in 10 minutes."
- ❌ Fuzzy: "We'll onboard you" (no concrete path)
- ❌ Missing: No mention of what happens after purchase

**Decision Score:** ___/12 decisions locked

---

## Proof Architecture (Required)

**Every core claim must have:**
- **Claim** — What you assert
- **Proof** — What supports it
- **Source** — Where it comes from
- **Verification time** — Can buyer confirm in 5 minutes / 5 days / 5 weeks?

**Proof Type Classification:**
- Numbers (metrics, statistics)
- Case (customer story, before/after)
- Demo (show don't tell, trial, sandbox)
- Benchmark (industry comparison)
- Authority (analyst, expert endorsement)
- Reference (referenceable customer)
- Social (reviews, testimonials, G2)
- Visual (screenshots, before/after images)

**Common friction:**
> "We have proof — but it's slow, private, unverifiable, or not credible to this buyer."

**Proof Validation Checklist:**
- [ ] Proof exists for each of 5 positioning claims
- [ ] Verification time is explicit (5 min / 5 day / 5 week)
- [ ] Proof is appropriate to buyer type (technical vs. business)
- [ ] Proof is accessible (not gated, not NDA'd)

---

## Surfaces (Where Decisions Must Visibly Appear)

| Surface | Role | Status |
|---------|------|--------|
| **Homepage hero + first scroll** | Primary self-select surface — answers 15 buyer questions | ⬜ EXISTS / WEAK / ABSENT |
| **Pitch opening (first 3-5 slides)** | Founder tells same story every time | ⬜ EXISTS / WEAK / ABSENT |
| **First outbound message** | Trigger + wedge, sparks right question | ⬜ EXISTS / WEAK / ABSENT |
| **LinkedIn profile** | Warms buyer before contact, primes category | ⬜ EXISTS / WEAK / ABSENT |
| **Demo/walkthrough opening (first 3 min)** | First experience answers "what is this" | ⬜ EXISTS / WEAK / ABSENT |
| **One-pager / overview slide** | Standalone clarity, works without voiceover | ⬜ EXISTS / WEAK / ABSENT |

**Surface Score:** ___/6 surfaces exist and are strong

---

## Qualitative Indicators (Observe in Calls/Emails)

### **POSITIVE SIGNALS (What Good Looks Like):**

✅ **Immediate Recognition:**
- Buyer can repeat back value proposition without correction
- Buyer places you in correct category unprompted
- Buyer names the right alternative ("Oh, you replace [X]")

✅ **Early Engagement:**
- Buyer asks "how does this work for us?" instead of "what is this?"
- Buyer shares link/deck internally within 48 hours
- Buyer references language they saw on site/pitch

✅ **Proof Validation:**
- Buyer confirms proof credibility ("I checked your case study")
- Buyer verification time matches expectation
- Buyer asks for additional proof type they trust

✅ **Self-Selection:**
- Qualified meetings self-select in ("this sounds exactly like us")
- Wrong-fit buyers self-select out before call
- Buyer starts call referencing what they saw

✅ **Activation Understanding:**
- Buyer asks about implementation details early
- Buyer references "what happens after we sign" unprompted
- Buyer calculates time to value in their context

### **NEGATIVE SIGNALS (What Bad Looks Like):**

❌ **Confusion Persists:**
- Buyer asks "what is this?" 10+ minutes into conversation
- Buyer names wrong category ("Oh, you're like [unrelated tool]")
- Buyer mentions 3+ alternatives (unclear mental model)
- Buyer can't explain to colleague without you present

❌ **Proof Skepticism:**
- Buyer questions proof validity ("How do I know this is real?")
- Buyer asks for proof you don't have
- Buyer says "I'll need to validate this" but no verification path

❌ **Delayed Engagement:**
- Materials shared but no internal forwarding
- "Let me think about it" without specific next step
- Buyer needs repeated explanations

❌ **Activation Uncertainty:**
- Buyer surprised by implementation scope ("I didn't know we'd need to...")
- "What happens after we buy?" asked late in process
- Buyer unclear on what Week 1 looks like

### **TIMING EXPECTATIONS:**

⏱️ **Strong Timing:**
- Category recognition: Within first 90 seconds
- Value repetition accuracy: By end of first call
- Internal sharing: Within 48 hours of first call
- Activation questions: Week 1-2 (not Week 8)

⏱️ **Weak Timing:**
- Still asking "what is this?" after 10+ minutes
- Takes multiple calls to grasp value proposition
- Internal sharing only after repeated prompts
- Activation discussion delayed until proposal stage

**How to Track:** Call recordings (Gong/Chorus) OR simple checklist in CRM notes after each call

---

## Quantitative Indicators (Track Systematically)

### **Website Analytics**

**Tool:** PostHog (free tier: 1M events/month)  
**Setup Time:** 15 minutes  
**Setup Steps:**
1. Add PostHog snippet to homepage
2. Enable autocapture (pageviews, clicks, scrolls)
3. Create custom events: CTA clicks, pricing page visits

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **Bounce rate** (homepage) | <50% | 50-70% | >70% | Weekly |
| **Avg. time on page** (homepage) | >90 sec | 45-90 sec | <45 sec | Weekly |
| **Scroll depth** (% reach 75%) | >60% | 40-60% | <40% | Weekly |
| **CTA click rate** | >15% | 8-15% | <8% | Weekly |
| **Pricing page visit rate** | >30% | 15-30% | <15% | Weekly |

**PostHog Dashboard Setup:**
```
Create Insight → Trends
- Event: $pageview, Filter: URL contains "/home"
- Breakdown: None
- Add metric: Bounce rate (exits / pageviews)
- Add metric: Avg session duration
- Add metric: Scroll depth (custom event)
```

**Action if Red:** Homepage doesn't answer 15 buyer questions, run homepage audit

---

### **Pitch Deck Analytics**

**Tool:** DocSend ($10/mo) OR Pitch.com (free tier) OR Notion with analytics  
**Setup Time:** 5 minutes  
**Setup Steps:**
1. Upload deck to platform
2. Share trackable link (not PDF attachment)
3. Monitor: views, time per slide, completion rate

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **Deck completion rate** | >70% | 50-70% | <50% | Per deal |
| **Avg. time viewing** | >5 min | 3-5 min | <3 min | Per deal |
| **Slide 1-3 drop-off** | <20% | 20-40% | >40% | Per deal |
| **Forwarding rate** | >40% | 20-40% | <20% | Per deal |

**Action if Red:** Deck doesn't work standalone, needs voiceover

---

### **LinkedIn Profile Analytics**

**Tool:** LinkedIn native analytics (free)  
**Setup Time:** 0 minutes  
**Setup Steps:** Already built-in, just check weekly

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **Profile views/week** | Trending up | Flat | Trending down | Weekly |
| **Search appearances** | >50/week | 25-50/week | <25/week | Weekly |
| **Post engagement rate** | >5% | 2-5% | <2% | Per post |

**Action if Red:** Category unclear in profile, not showing up in searches

---

### **Email Tracking**

**Tool:** Mixmax ($29/mo) OR Mailtrack (free Chrome extension) OR Streak ($49/mo)  
**Setup Time:** 10 minutes  
**Setup Steps:**
1. Install browser extension
2. Enable tracking on outbound emails
3. Monitor: opens, clicks, forwards

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **First email open rate** | >60% | 40-60% | <40% | Per campaign (24-48 hrs) |
| **Link click rate** | >30% | 15-30% | <15% | Per campaign |
| **Forward/share rate** | >20% | 10-20% | <10% | Per campaign |

**Action if Red:** Subject line/preview doesn't create interest

---

## Zone 1 Scoring

**Calculation:**
```
Zone 1 Score = (Decisions × 0.4) + (Qualitative × 0.3) + (Quantitative × 0.3)

Where:
- Decisions = (locked / 12) × 15
- Qualitative = (positive % - negative %) × 15
- Quantitative = avg threshold performance × 15
```

**🟢 GREEN (12-15 points):** Decisions 10-12/12, Qualitative 70%+, Quantitative meet thresholds  
**🟡 YELLOW (8-11 points):** Decisions 7-9/12, Qualitative 40-70%, Quantitative below but improving  
**🔴 RED (0-7 points):** Decisions <7/12, Qualitative <40%, Quantitative far below

---

## Probe Questions If Fuzzy

- "Show me your homepage — let's walk through what a buyer sees"
- "Who specifically — what role, what kind of company?"
- "What are they using today instead of this?"
- "Why do they choose you over that alternative? What's their criteria?"
- "What proof do they need to believe this works?"
- "Walk me through what happens in the first 10 minutes after they sign up"
- "How long until they see results?"
- "What's the first safe step you offer them?"
- "Walk me through your last 3 deals — what happened in first call?"

---

# ZONE 2: VIABILITY

**Does this make economic sense for both buyer AND seller?**

---

## Zone Job

Make it economically believable that:
- Buyer can afford and justify this
- Seller can deliver profitably at scale
- Both sides win

**Buyer economics FIRST. Seller viability SECOND.**

---

## Outside-In Buyer Question

> **"Does this make financial sense for the buyer — and can we deliver it viably?"**

*Listen for: what buyer pays today, what buyer can/will pay, how buyer justifies spend, what delivery costs us, what breaks at scale.*

---

## Decisions (Must Be Explicitly Locked)

### **Buyer Economics (Outside-In — PRIMARY):**

| Decision | What It Locks | Status |
|----------|--------------|--------|
| **Cost of alternative** | What buyer pays today (tool + labor + opportunity cost) | ⬜ LOCKED / FUZZY / MISSING |
| **Buyer budget/WTP** | What buyer can/will pay for this category | ⬜ LOCKED / FUZZY / MISSING |
| **Buyer ROI framework** | How buyer justifies spend internally (formula, benchmarks) | ⬜ LOCKED / FUZZY / MISSING |
| **Payment preference** | How buyer prefers to pay (monthly/annual/upfront) | ⬜ LOCKED / FUZZY / MISSING |
| **Procurement requirements** | Buyer's approval/PO process, finance involvement | ⬜ LOCKED / FUZZY / MISSING |

### **Seller Viability (Inside-Out — SECONDARY):**

| Decision | What It Locks | Status |
|----------|--------------|--------|
| **Price point** | What you charge (aligned with buyer WTP) | ⬜ LOCKED / FUZZY / MISSING |
| **Gross margin floor** | Minimum viable margin to deliver profitably | ⬜ LOCKED / FUZZY / MISSING |
| **Segment size** | Enough buyers exist at this price point | ⬜ LOCKED / FUZZY / MISSING |
| **Capacity constraint** | What breaks first at 10x scale | ⬜ LOCKED / FUZZY / MISSING |

**Decision Score:** ___/9 decisions locked

---

## Required Artifact (Hard Requirement)

**One-Page Unit Economics Sketch:**

Must include:
- **Buyer side:** Cost of alternative, typical budget, ROI calculation
- **Seller side:** Target ACV, gross margin assumption, delivery cost
- **Scale test:** What breaks first if this scales to 50 buyers

**Rough is fine. Missing is not.**

**Template:**
```
BUYER ECONOMICS
Alternative cost: €__/year (tool + labor + opportunity)
Buyer budget range: €__ - €__
ROI framework: [How buyer calculates value]
Payment preference: Monthly / Annual / Upfront

SELLER VIABILITY
Price point: €__
Gross margin: __%
Delivery cost per customer: €__
Capacity constraint: [What breaks at 10x]

SEGMENT
Total addressable buyers: __
At this price point: __
```

---

## Surfaces (Where Decisions Must Visibly Appear)

| Surface | Role | Status |
|---------|------|--------|
| **Pricing page** | Public pricing (if applicable) or pricing philosophy | ⬜ EXISTS / WEAK / ABSENT |
| **ROI calculator / value tool** | Buyer personalizes economics | ⬜ EXISTS / WEAK / ABSENT |
| **Proposal / commercial slide** | Deal economics spelled out | ⬜ EXISTS / WEAK / ABSENT |
| **FAQ / objections section** | "Why does this cost $X?" answered from buyer ROI | ⬜ EXISTS / WEAK / ABSENT |
| **Unit economics doc** | Internal model (for founder/investor) | ⬜ EXISTS / WEAK / ABSENT |

**Surface Score:** ___/5 surfaces exist and are strong

---

## Qualitative Indicators (Observe in Calls/Emails)

### **POSITIVE SIGNALS:**

✅ **Price Engagement:**
- Buyer asks pricing-related questions early (Call 1-2)
- Buyer discusses budget ownership ("This comes from my budget")
- Buyer frames internal ROI conversation proactively
- Buyer brings procurement/finance into loop early

✅ **Value Recognition:**
- Buyer calculates value in their own terms
- Buyer compares to alternative's pricing favorably
- "This makes sense financially" explicit statement
- Buyer references cost of alternative unprompted

✅ **Process Understanding:**
- Buyer understands payment structure
- Buyer asks about contract terms appropriately
- Buyer discusses renewal/expansion path

### **NEGATIVE SIGNALS:**

❌ **Price Shock:**
- Buyer surprised by price ("I thought this was cheaper")
- "We'll figure out pricing later" avoidance pattern
- "Our budget is $X" when X is <20% of your price
- Multiple discount requests without value discussion

❌ **Value Confusion:**
- Buyer doesn't understand what they're paying for
- "What exactly am I buying?" confusion
- Value metric doesn't resonate with buyer economics
- Buyer compares to wrong alternatives on price

❌ **Economic Misalignment:**
- Deal size too small for sales effort required
- Buyer wants monthly when you need annual
- Gross margin assumptions broken by scope creep
- Discount needed to close every deal

### **TIMING EXPECTATIONS:**

⏱️ **Strong:** Pricing discussed by Call 2, budget ownership clear by Call 3  
⏱️ **Weak:** Pricing avoided until late stage, budget ownership unclear at proposal

**How to Track:** Call recordings + CRM deal notes (pricing discussion timing)

---

## Quantitative Indicators (Track Systematically)

### **Pricing Page Analytics**

**Tool:** PostHog  
**Setup Time:** 5 minutes  
**Setup:** Create segment for pricing page visitors, track time and exits

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **Pricing page visit rate** (from homepage) | >30% | 15-30% | <15% | Weekly |
| **Time on pricing page** | >2 min | 1-2 min | <1 min | Weekly |
| **Exit rate** (pricing page) | <60% | 60-80% | >80% | Weekly |
| **Calculator interaction rate** (if exists) | >40% | 20-40% | <20% | Weekly |

**Action if Red:** Pricing unclear, no self-serve economics understanding

---

### **Proposal Analytics**

**Tool:** DocSend OR PandaDoc (free tier)  
**Setup Time:** 5 minutes  
**Setup:** Upload proposal template, track per deal

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **Proposal view rate** | >90% | 70-90% | <70% | Per deal |
| **Time on commercial terms section** | >3 min | 1-3 min | <1 min | Per deal |
| **Section re-visit rate** (pricing) | >50% | 30-50% | <30% | Per deal |

**Action if Red:** Pricing not engaging, buyer not internalizing economics

---

### **CRM Deal Data**

**Tool:** Pipedrive ($14/mo) OR Attio ($29/mo) OR Notion (free)  
**Setup Time:** 0 minutes (already in CRM)  
**Setup:** Track custom fields: ACV, discount %, close date

| Metric | Green 🟢 | Yellow 🟡 | Red 🔴 | Check Frequency |
|--------|----------|-----------|--------|-----------------|
| **ACV variance** (from target) | <20% | 20-40% | >40% | Monthly |
| **Discount rate** (% off list) | <10% | 10-25% | >25% | Monthly |
| **Custom pricing requests** | <20% | 20-40% | >40% | Monthly |
| **Price objection rate** | <30% of deals | 30-60% | >60% | Monthly |

**Action if Red:** Pricing model doesn't match buyer reality

---

## Zone 2 Scoring

**🟢 GREEN (12-15 points):** Buyer economics clear, seller viability proven, metrics on target  
**🟡 YELLOW (8-11 points):** Some buyer economics known, viability uncertain, metrics below target  
**🔴 RED (0-7 points):** Buyer economics unknown, pricing feels random, metrics broken

---

## Probe Questions If Fuzzy

- "What does the buyer pay today for the alternative?"
- "What's the total cost to the buyer (tool + labor + opportunity)?"
- "How does the buyer justify this spend internally?"
- "What's a typical budget for this category in their company?"
- "How do they prefer to pay — monthly, annual, upfront?"
- "What does it cost you to deliver one deal?"
- "At what scale does your model break?"
- "Show me your unit economics assumptions"

---

# [ZONES 3-5 CONTINUE WITH SAME STRUCTURE FROM V3.1]

[Due to length constraints, Zones 3-5 follow the exact same structure as v3.1:
- Zone 3: Travelability (8 decisions, buyer org movement)
- Zone 4: Reachability (9 decisions, buyer discovery FIRST)
- Zone 5: Closability (9 decisions, buyer approval process)

Each includes:
- Outside-in decisions
- Surfaces
- Qualitative + Quantitative indicators
- Scoring criteria
- All implementation details from v3.1]

---

# DIAGNOSTIC SESSION STRUCTURE

## 60-90 Min Outside-In Assessment (Surface-First Flow)

### **OPENING — Situation Recognition (5 min)**

> *"Before we dig in — which of these situations sounds closest to where you are right now?"*

**Show 6-8 common situations:**
- "We built a prototype, but no first customers sign"
- "Our whole story is a mess — homepage, deck, calls all say different things"
- "Some wins, but I can't build a consistent pipeline"
- "My sales calls are messy — I demo features, then prospects ghost"
- "About to hire first sales rep — terrified they'll fail without me"
- "We have customers, but no clue how to package or price this"

**Founder self-selects situation**

---

### **STEP 1: Surface Audit (30 min)**

> *"Show me your homepage. Let's walk through what a buyer sees."*

**Priority: Homepage First (15 min)**

1. **Pull up the actual homepage**
   - Share screen, view live site
   - Don't rely on founder description

2. **Apply 15-question framework**
   - Walk through each question
   - For each: Explicit / Partial / Missing?
   - Don't editorialize, just score

3. **Count the scores**
   ```
   Explicit: __/15
   Partial: __/15
   Missing: __/15
   Status: 🟢 / 🟡 / 🔴
   ```

4. **Note specific gaps**
   ```
   Q1-2 partial → buyer has to infer category
   Q5-6 partial → ICP too broad
   Q9 missing → no alternative mentioned
   Q12 partial → no effort preview
   Q14 missing → no activation preview
   Q15 partial → no risk reversal
   ```

**If Time Permits: Secondary Surfaces (15 min total)**

**Pitch deck (first 5 slides):** 10 min
- Apply similar framework (fewer questions)
- Score: __/7 explicit

**Outbound email (first message):** 5 min
- Apply similar framework
- Score: __/4 explicit

**Note:** If time limited, defer secondary surfaces to follow-up

---

### **STEP 2: Decision Inference (15 min)**

> *"Based on what we saw, here are the decisions that seem fuzzy or missing..."*

**Map surface gaps to decision gaps:**

```
FROM HOMEPAGE AUDIT:

Surface Gaps                  → Decision Inference
─────────────────────────────────────────────────────
Q1-2 partial (category)      → Category: FUZZY
Q5-6 partial (ICP)            → Customer: FUZZY
Q9 missing (alternative)      → Alternative: MISSING
Q7-8 partial (how/what)       → Approval Criteria: FUZZY
                              → Outcome: FUZZY
Q10-11 partial (proof/trust)  → Proof type: FUZZY
Q12 partial (effort)          → First value path: FUZZY
                              → Time to value: FUZZY
Q14 missing (what's next)     → Activation moment: MISSING
Q13,15 partial (start/risk)   → First step: FUZZY
                              → Primary risk: FUZZY
```

**Mark in decision ledger:**
```
Zone 1 Decision Status:
1. Category: ⬜ FUZZY
2. Customer: ⬜ FUZZY
3. Alternative: ⬜ MISSING
4. Approval Criteria: ⬜ FUZZY
5. Outcome: ⬜ FUZZY
6. Proof type: ⬜ FUZZY
7. Proof moments: ⬜ FUZZY
8. Primary risk: ⬜ FUZZY
9. First step: ⬜ FUZZY
10. Activation moment: ⬜ MISSING
11. First value path: ⬜ FUZZY
12. Time to value: ⬜ FUZZY

Preliminary Score: 0/12 locked → 🔴 RED
```

---

### **STEP 3: Indicator Validation (20 min)**

> *"Let's confirm this with behaviors and metrics..."*

**Check if indicators confirm surface + decision gaps:**

**A. Quantitative (if tracking exists):**

```
WEBSITE (PostHog):
Bounce rate: 72% (target <50%) → ✅ Confirms homepage doesn't land
Time on page: 23 sec (target >90) → ✅ Confirms confusion
Scroll depth: 31% (target >60%) → ✅ Confirms disengagement
Pricing visit: 8% (target >30%) → ✅ Confirms no progression

Inference: Homepage failing Q1-2 (category) CONFIRMED by metrics
```

**B. Qualitative (ask about call patterns):**

**Probe:**
> "In sales calls, how often do buyers ask 'what is this?'"

**Answer:** "8 out of 10 calls, even 10 minutes in"
→ ✅ Confirms category FUZZY

**Probe:**
> "Do buyers mention the right alternative or wrong ones?"

**Answer:** "They usually compare us to [completely wrong tool]"
→ ✅ Confirms alternative MISSING

**Probe:**
> "Can buyers repeat back your value proposition?"

**Answer:** "Not really, they get confused or use vague terms"
→ ✅ Confirms outcome FUZZY

**Probe:**
> "Do buyers ask about implementation early or late?"

**Answer:** "Usually surprises them at proposal stage"
→ ✅ Confirms activation moment MISSING

**Validation Summary:**
```
✅ Surface gaps (homepage 2/15) CONFIRMED by metrics
✅ Decision gaps (0/12 locked) CONFIRMED by behavior
✅ Zone 1 is genuinely RED, not just surface issue
```

---

### **STEP 4: Results Reality Check (10 min)**

> *"And here's what this costs you in outcomes..."*

**Show business impact:**

```
CURRENT STATE:
Win rate: 12% (benchmark: 25%+)
Sales cycle: 24 weeks (target: <8 weeks)
Pre-qualification: 23% (target: >70%)
Founder in every call: 100% (target: <30%)
Homepage bounce: 72% (target: <50%)

ROOT CAUSE:
Zone 1 (Buyability) is RED → Everything downstream suffers
```

**Cascade Impact:**
```
Zone 1 RED →
  ├─ Can't self-qualify → wrong buyers book calls
  ├─ Materials don't travel → founder dependency
  ├─ No systematic pipeline → network-only deals
  └─ Deals stall → long cycles, low win rate
```

**Cost Analysis:**
```
Each deal at 24 weeks = 3x target cycle
Each wrong-fit call = 60 min wasted (founder + team)
Win rate 12% vs 25% = 52% fewer closed deals

Annual cost of Zone 1 being red:
- 200 wasted hours on wrong-fit calls
- €XXX,000 in lost revenue (deals that should close)
- Founder stuck in delivery, can't build company
```

---

### **SYNTHESIS (10 min)**

**Scorecard summary:**
```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ZONE 1 — BUYABILITY: 🔴 RED [0/12 decisions locked]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SURFACE AUDIT:
Homepage: 2/15 explicit, 11/15 partial, 2/15 missing → RED

DECISION GAPS:
• Category: FUZZY (Q1-2 partial on homepage)
• Customer: FUZZY (Q5-6 partial on homepage)
• Alternative: MISSING (Q9 missing)
• Activation moment: MISSING (Q14 missing)
• First step: FUZZY (Q13 partial)
[All 12 decisions fuzzy or missing]

INDICATOR CONFIRMATION:
Quantitative:
• Bounce rate 72% (target <50%)
• Time on page 23sec (target >90)
• Scroll depth 31% (target >60%)

Qualitative:
• "What is this?" asked in 8/10 calls
• Wrong alternatives mentioned
• Can't repeat value back
• Implementation surprises at proposal

RESULTS IMPACT:
• Win rate 12% vs 25% target (-52% deals)
• Sales cycle 24 weeks vs 8 week target (3x)
• 200 wasted hours on wrong-fit calls

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Fix-First Recommendation:**

```
PRIMARY CONSTRAINED ZONE: Zone 1 (Buyability)

ROOT CAUSE: 
All 12 positioning decisions are fuzzy or missing
→ Homepage answers 2/15 buyer questions
→ Buyers can't self-select, can't progress, can't commit

CONCRETE FIX:
Lock Zone 1 decisions through Buyability Sprint

INTERVENTION:
Duration: 2-4 weeks
Investment: €9-12K
Deliverables:
• 12 decisions locked (decision ledger)
• Homepage rebuilt (answers 15 buyer questions)
• Pitch deck rebuilt (answers 7 buyer questions)
• Outbound template rebuilt
• Playbook (how team uses locked decisions)

CASCADE UNLOCK:
Zone 1 locked →
  ├─ Zone 3 unlocks (materials can now travel)
  ├─ Zone 4 unlocks (can target systematically)
  └─ Zone 8 unlocks (investor thesis clears)

MEASURE SUCCESS:
Leading indicators (Week 2-3):
• Homepage: 12+/15 explicit
• "What is this?" drops to <2/10 calls
• Buyers repeat value back accurately

Quantitative (Week 4-6):
• Bounce rate <50%
• Time on page >90sec
• Pre-qualification >50%

Lagging (Month 2-3):
• Win rate trending toward 20%+
• Sales cycle trending toward 12 weeks
• Founder in <50% of calls
```

---

# IMPLEMENTATION SETUP GUIDE

## Week 1: Foundation Setup (2 Hours Total)

### **Monday (30 min) — Analytics Foundation**
- [ ] Create PostHog account (free tier)
- [ ] Add PostHog snippet to homepage
- [ ] Enable autocapture (pageviews, clicks, scrolls)
- [ ] Create custom events: CTA clicks, pricing page visits

### **Tuesday (30 min) — Document Tracking**
- [ ] Create DocSend account OR set up Notion share tracking
- [ ] Upload pitch deck to platform
- [ ] Create shareable deck link (not PDF attachment)
- [ ] Upload champion deck template

### **Wednesday (30 min) — Email & Outbound**
- [ ] Install Mixmax ($29/mo) OR Mailtrack (free)
- [ ] Enable email tracking
- [ ] Set up outbound campaign tracking
- [ ] Enable LinkedIn analytics (already built-in)

### **Thursday (30 min) — CRM & Dashboards**
- [ ] Set up Pipedrive ($14) OR Attio ($29) OR Notion (free)
- [ ] Create custom fields: ACV, discount %, source
- [ ] Create Zone 1-5 tracking dashboards (templates provided)
- [ ] Document baseline metrics

**Total Investment:**
- Time: 2 hours
- Cost: $0-43/month (PostHog free, Mailtrack free, Pipedrive $14, Mixmax $29)

---

## Tool Stack Recommendations

### **Minimal Stack (Free/Low-Cost)**

**Analytics:**
- PostHog (free: 1M events/month)

**Email Tracking:**
- Mailtrack (free Chrome extension)

**Document Tracking:**
- Notion share tracking (free/included)

**CRM:**
- Notion (free-$10/mo) OR Pipedrive ($14/mo)

**Demo Recording:**
- Loom (free: 25 videos)

**Total: $0-24/month**

---

### **Full Stack (Comprehensive)**

**Analytics:**
- PostHog Pro ($9/mo for extra features)

**Email & Outbound:**
- Mixmax ($29/mo) OR Lemlist ($59/mo)

**Document Tracking:**
- DocSend ($10/mo)

**CRM:**
- Pipedrive ($14/mo) OR Attio ($29/mo)

**Demo Recording:**
- Loom Business ($12.50/mo)

**Total: $75-120/month**

---

## Weekly Tracking Dashboards

[COMPLETE DASHBOARD TEMPLATES FROM V3.1 - ALL 5 ZONES]

[Including:
- Zone 1: Buyability Dashboard
- Zone 2: Viability Dashboard
- Zone 3: Travelability Dashboard
- Zone 4: Reachability Dashboard
- Zone 5: Closability Dashboard]

---

## Weekly Rhythm (30 Min Every Monday)

### **Monday 9am — Weekly Review**

**1. Pull Metrics (15 min):**
- PostHog: bounce, time, scroll, CTAs
- DocSend: deck stats, proposals
- Mixmax/Mailtrack: email tracking
- CRM: deal data, stage velocity
- LinkedIn: profile views, post engagement

**2. Update Dashboards (10 min):**
- Fill in Zone 1-5 templates
- Flag red zones (below thresholds)
- Note trends (up/down/flat)

**3. Fix-First Decision (5 min):**
```
WEEKLY PRIORITIES — [Date]

RED ZONES: [List zones with 🔴 status]

FIX-FIRST THIS WEEK:
Zone __: [Specific red metric]
Root cause: [Missing decision or failing surface]
Action: [Specific fix to test]
Measure: [Indicator to watch]

LAST WEEK'S FIX:
Action taken: __
Result: 🟢 improved / 🟡 unchanged / 🔴 worsened
Evidence: [Specific metric movement]
```

---

# SCORECARD DELIVERY FORMAT

```
BUYING PATH DIAGNOSTIC SCORECARD

Company: ___
Date: ___
Assessed by: ___

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ZONE 1 — BUYABILITY: 🟢 / 🟡 / 🔴  [Score: __/15]

Surface Audit:
• Homepage: __/15 explicit, __/15 partial, __/15 missing

Decisions: __/12 locked
  - Category: LOCKED / FUZZY / MISSING
  - Customer: LOCKED / FUZZY / MISSING
  - Alternative: LOCKED / FUZZY / MISSING
  - Approval Criteria: LOCKED / FUZZY / MISSING
  - Outcome: LOCKED / FUZZY / MISSING
  - Proof type: LOCKED / FUZZY / MISSING
  - Proof moments: LOCKED / FUZZY / MISSING
  - Primary risk: LOCKED / FUZZY / MISSING
  - First step: LOCKED / FUZZY / MISSING
  - Activation moment: LOCKED / FUZZY / MISSING
  - First value path: LOCKED / FUZZY / MISSING
  - Time to value: LOCKED / FUZZY / MISSING

Surfaces: __/6 exist and strong

Leading (qual): __% positive, __% negative
Leading (quant): Bounce __%, Time __sec, Scroll __%

Lagging: Win rate __%, Cycle __weeks

One-sentence diagnosis:
___

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ZONES 2-5 FOLLOW SAME FORMAT]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

OVERALL SCORE: __/75 (__%)

FIX-FIRST RECOMMENDATION:

Primary constrained zone: Zone __
Root cause: [Missing decision(s)]
Failing surface(s): [Specific surfaces]
Cascade impact: [What unlocks downstream]

CONCRETE FIX:
[Specific intervention with timeline]

MEASURE PROGRESS:
Leading indicators to watch: [Specific signals]
Expected improvement: [Threshold targets]
Timeline: [When to see movement]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Summary Constraint Test

**A valid diagnostic must produce:**

1. ✅ Surface audit showing specific gaps (homepage __/15 questions answered)
2. ✅ Decision inference from surface gaps (Category FUZZY because Q1-2 partial)
3. ✅ Indicator validation confirming gaps (Bounce 72% confirms homepage doesn't land)
4. ✅ Results proof showing business impact (Win rate 12% vs 25% target)
5. ✅ Fix-first recommendation with leading indicators to track

**If not all 5 are clear → you don't have a diagnosis yet.**

---

**Version 3.2 — February 2026**  
**Product.Zone — Surface-First Outside-In Diagnostic System**  
**With Activation Projection & Proven Homepage Framework**

---

**The framework is only useful if you can implement it.**  
**Start with what you can SEE, not what founder SAYS.**  
**Now you can.**
