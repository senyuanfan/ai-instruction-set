---
name: distill
description: On explicit request, compresses content the user provides (text, a fetchable webpage, notes, a paper) into a signal-first readout — a verdict on whether it's worth their time, then the relevant fields among core claim, evidence, novelty, confidence, incentives, actionability, and open questions — judged against what they are currently working on, and hunts for signal across multiple sources. Use when the user says "distill this", shares content asking what's genuinely new or worth their attention, or wants several sources cross-referenced. Not a summarizer, and it does not auto-fire on shared links.
---

# Distill

An information **compressor** and personal research analyst — not a summarizer. It
turns content into signal measured against what the user is actually working on, to
cut reading time and decision fatigue.

Runs on **explicit request only**: "distill this", or content shared with a
question like "is this worth my time?" / "what's new here?". It never auto-fires on
a pasted link, and never logs or edits anything unless invoked.

Honor the user's style: lead with the verdict, stay concise, quotes and facts
first, no padding, hot takes welcome, push back on weak claims.

## What it does

1. **Anchor to the user.** Read the [about-me](../about-me/profile.md) profile —
   especially Current focus — so relevance is judged against what they're actually
   doing, not in the abstract.
2. **Ingest honestly.** Work from the text provided or a fetchable webpage. Run a
   web search *only* to corroborate a load-bearing claim or fill a gap needed for
   the verdict — not as a default step. Never fabricate content it couldn't
   actually read (an un-fetchable video, a paywalled piece); say what it couldn't
   ingest.
3. **Compress to signal.** Give a verdict, then the fields that carry signal.
4. **Hunt across sources** when there's more than one (Layer 2).

## Output: verdict first, loose fields

Lead with a one-line verdict tied to their current focus:

> **Worth your hour / Skim / Skip** — <why, relative to what they're working on>

Then surface only the fields below that carry signal for this item. They are a
**lens, not a form** — use what's relevant, drop the rest, never pad an empty
field. A golf tip and an RL paper should not wear the same shape.

| Field | Purpose |
| --- | --- |
| Core claim | What is the author actually saying? (one sentence) |
| Evidence | What facts, data, or experiments support it, and how strong? |
| Novelty | What is genuinely new relative to what's already known? |
| Confidence | High / Medium / Low that it's true — and why |
| Incentives | What biases or motivations might shape it? |
| Actionability | Anything worth doing or changing, given the user's work? |
| Open questions | What remains uncertain? Predictions to revisit? |

Full definitions and worked examples: [schema.md](schema.md).

## Layer 2: signal across sources

Apply across items, not within one. Techniques in
[signal-analysis.md](signal-analysis.md).

- **Repetition across *independent* sources** — verify independence before counting
  it as corroboration.
- **Disagreement — surface it, don't average it.** Name who claims what.
- **Facts vs. opinions vs. predictions** — label each.
- **Connect to prior knowledge** — what does this confirm, contradict, or extend?

## Analyst mode

When the user wants a verdict rather than a capture, answer directly and lead with
the answer:
- What is genuinely new here?
- What would an expert notice immediately — or dismiss?
- What is everyone repeating without evidence?
- Which few ideas deserve an hour of real attention, and why those?

## Memory (opt-in)

- **Logging is off by default.** Compress and answer live; write nothing. Only when
  the user says "log this" append to a `distilled/` log — see
  [signal-analysis.md](signal-analysis.md#persistence). The log powers cross-source
  patterns over time and claim tracking.
- **Enrich the profile.** When distilling surfaces a durable fact or interest about
  the user, add it to the [about-me](../about-me/profile.md) profile (durable facts
  only, same bar as about-me's keep-current rule) and tell them — don't ask first.

## Workflow

```
Distill Progress:
- [ ] 1. Read about-me/Current focus to anchor relevance
- [ ] 2. Ingest the item(s) honestly; web-search only if needed
- [ ] 3. Verdict first, then the fields that carry signal
- [ ] 4. Run Layer 2 across items if there's more than one
- [ ] 5. Only if asked: log it; enrich about-me if a durable fact surfaced
```
