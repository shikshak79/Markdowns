---
name: linkedin-content-extractor
description: Extract LinkedIn post candidates from a conversation. Use this skill at the end of any conversation when the user wants to identify content worth publishing on LinkedIn, asks "what could I post about this?", "any post ideas?", "extract content", or wants to build in public from their conversations. Always trigger when the user signals they want to capture shareable insights before closing a conversation.
---

# LinkedIn Content Extractor

Scans a conversation and surfaces 2–5 post candidates worth developing into LinkedIn posts. The goal is NOT to write posts — it's to identify the raw material and give just enough scaffolding so the user can write the post themselves in under 10 minutes.

## Three Content Filters

Apply these three filters when scanning the conversation. Ignore anything that's pure information exchange with no personal angle, opinion, or practical specificity.

**1. Personal experience / thought**
Something the user went through, decided, or observed firsthand. The signal is a specific situation, not a lesson. Posts in this category earn trust because they're lived, not theorized.

**2. Contrarian view**
A position that contradicts common advice or conventional thinking. Only flag this if the position has at least one concrete example or data point behind it — pure opinion without grounding gets ignored on LinkedIn.

**3. Tactical / practical guidance**
Something someone could immediately apply. Specificity is the test: if it could describe anyone's experience, it's too vague. Numbers, named steps, or named frameworks make it pass.

## Output Format per Candidate

For each candidate, output exactly this structure — nothing more:

```
## [Post #N] [Content type: Personal / Contrarian / Tactical]

**Core message** (1 sentence — what you actually said, in plain language)

**Hook** (1 sentence — the first line that would stop the scroll)

**Why it's worth posting** (1 sentence — what makes it credible / surprising / useful)

**Format hint** (Story arc / Single insight expanded / Short how-to)
```

## Ranking

Order candidates by posting urgency:
- Top: time-sensitive, tied to something current (a launch, a decision just made, a conversation just had)
- Middle: evergreen but sharp
- Bottom: needs more development before it would land

## What to Ignore

- Pure factual or technical exchanges with no personal stake
- Ideas the user was just exploring with no actual experience behind them
- Anything that would require explaining context for 3+ sentences before the actual insight
- Generic takes that could have been written by anyone

## Closing Note

After the candidates, add one line:

> *"Strongest one to post today: [Post #N] — [one-phrase reason]"*

That's it. No full drafts. No elaborate breakdowns. Just the skeleton.
