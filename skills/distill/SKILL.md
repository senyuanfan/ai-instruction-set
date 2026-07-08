---
name: distill
description: Compresses any piece of content — article, paper, video, podcast, Reddit/X thread, meeting, or notes — into one small consistent schema (core claim, evidence, novelty, confidence, incentives, actionability, open questions), then hunts for signal across sources rather than summarizing. Use when the user shares content to analyze, asks "what's genuinely new here", "what would an expert notice", or "what is everyone repeating without evidence", wants facts separated from opinion and prediction, or wants several sources cross-referenced.
---

# Distill

An information **compressor**, not a summarizer. A summary shortens; a compressor
transforms content into a fixed schema so signal is directly comparable across
everything the user reads. It sits between raw information and long-term memory to
cut reading time and decision fatigue.

Honor the user's style: concise, quotes/facts first, no padding, hot takes welcome,
push back on weak claims. Lead with the schema — don't narrate around it.

## When to use
- The user shares an article, paper, video, podcast, thread, meeting, or notes and
  wants it analyzed or captured.
- The user asks analyst questions: "what's genuinely new here?", "what would an
  expert notice immediately?", "what is everyone repeating without evidence?",
  "which few ideas deserve real attention?".
- The user wants facts separated from opinions and predictions.
- The user wants multiple sources on a topic cross-referenced.

## Two layers

**Layer 1 — compress each item** into the schema below.
**Layer 2 — hunt for signal** across items (repetition, disagreement, fact vs.
opinion, claim tracking, links to prior knowledge).

## Layer 1: the compression schema

Every item becomes these seven fields. Full definitions and the copyable template
are in [schema.md](schema.md).

| Field | Purpose |
| --- | --- |
| Core claim | What is the author actually saying? (one sentence) |
| Evidence | What facts, data, or experiments support it? |
| Novelty | What is genuinely new relative to what's already known? |
| Confidence | High / Medium / Low — and why |
| Incentives | What biases or motivations might shape this? |
| Actionability | Is there anything worth doing or changing? |
| Open questions | What remains uncertain? |

Rules: keep each field to a line or two; quote the source for the core claim and
key evidence; if a field is empty, say so ("Novelty: none — restates known work")
rather than padding it.

## Layer 2: signal hunting

Apply across items, not within one. Detail and techniques in
[signal-analysis.md](signal-analysis.md).

- **Detect repetition across *independent* sources** — and check they're actually
  independent (not citing each other).
- **Highlight disagreements; never average them away.** Name who claims what.
- **Separate facts from opinions from predictions.** Label each.
- **Track claims over time** — record predictions so they can later be marked
  right or wrong.
- **Connect to existing knowledge**, don't store isolated notes: what does this
  confirm, contradict, or extend?

## Analyst mode

When asked for a verdict rather than a capture, answer the question directly using
the schema as evidence. Default high-value questions:
- What is genuinely new here?
- What would an expert notice immediately (or dismiss)?
- What is everyone repeating without evidence?
- Which few ideas deserve an hour of real attention, and why those?

## Persistence

To make Layer 2 work over time, append each distillation to a `distilled/` log.
Format, index, and claim-tracking convention are in
[signal-analysis.md](signal-analysis.md#persistence). Connecting the log to a
knowledge base (e.g. Notion) is a documented future extension, not required.

## Workflow

```
Distill Progress:
- [ ] 1. Identify the item(s) and the user's intent (capture vs. verdict)
- [ ] 2. Compress each item into the seven-field schema
- [ ] 3. Run Layer 2 across items and any prior distillations
- [ ] 4. Answer the analyst question if one was asked
- [ ] 5. Append to distilled/ if persistence is wanted
```

1. **Scope it.** One item or several? Does the user want a capture, or a judgment?
2. **Compress** each item; quote sources; leave thin fields honestly thin.
3. **Cross-reference** against the other items and the existing log.
4. **Answer** the analyst question directly, using the schema as evidence.
5. **Persist** if wanted, and note what to revisit (predictions to score later).
