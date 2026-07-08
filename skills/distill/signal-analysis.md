# Signal Analysis (Layer 2)

Techniques for finding signal *across* items, plus how to persist distillations so
this works over time. Layer 1 compresses one item; Layer 2 is where the leverage
is.

## Contents
- Signal techniques
- Analyst questions
- Persistence
- Claim tracking
- Connecting to prior knowledge
- Future extension: knowledge base

## Signal techniques

- **Repetition across independent sources.** An idea repeated by sources that
  reached it independently is signal; the same idea echoed because each is quoting
  the same origin is one data point wearing many hats. Always check independence
  before counting repetition as corroboration.
- **Disagreement — surface it, don't average it.** When sources conflict, name each
  side and what each rests on. The disagreement itself is information; a blended
  "experts are split, the truth is probably in the middle" throws it away. Say who
  is likely right and why, or say it's genuinely open.
- **Facts vs. opinions vs. predictions.** Tag every notable statement as one of the
  three. Facts can be checked now; opinions reveal incentives; predictions get
  logged and scored later. Most noise is opinion and prediction dressed as fact.
- **Consensus without evidence.** Flag claims "everyone knows" that trace back to no
  primary evidence — repeated assertion is not support.

## Analyst questions

When the user wants a verdict, not a capture, answer directly and lead with the
answer:
- What is genuinely new here?
- What would an expert notice immediately — or dismiss out of hand?
- What is everyone repeating without evidence?
- Which few ideas deserve an hour of real attention, and why those over the rest?

## Persistence

Append each distillation to a `distilled/` directory so cross-source detection and
claim tracking have memory. Default layout (create it in the working project, or a
path the user names):

```
distilled/
├── index.md                       # one line per item: date · topic · source · confidence
└── <topic>/<short-slug>.md        # the full seven-field schema for that item
```

- One file per item, grouped by topic folder, so a topic's sources sit together.
- `index.md` is the scan layer — date, topic, source, core-claim gist, confidence.
- Date entries at capture time (the assistant knows the date when the skill runs).
- Before distilling a new item, skim the relevant topic folder and `index.md` so
  Layer 2 compares against what's already there.

## Claim tracking

Predictions and load-bearing claims get a status so they can be scored later:

```
Claim: <the prediction>   Source: <slug>   Made: <date>
Status: open | confirmed | refuted   Resolved: <date + what settled it>
```

Keep these in the item file under Open questions, and list open ones in `index.md`.
When later evidence settles a claim, update its status — this is how the log learns
which sources were actually right.

## Connecting to prior knowledge

Never store an item in isolation. For each new distillation, state its relation to
what's already known:
- **Confirms** <prior item/belief> — adds weight.
- **Contradicts** <prior item/belief> — trigger a disagreement analysis.
- **Extends** <prior item/belief> — new angle on a known idea.
- **Unrelated** — genuinely new thread; note the topic so future items can link.

Prefer linking to specific logged slugs over vague "as we discussed."

## Future extension: knowledge base

The `distilled/` log is intentionally plain Markdown so it stays portable. A later
version can sync it to a knowledge base (e.g. Notion) — mapping the index to a
database and each item to a page — without changing the schema. Not required for
the skill to work; keep the local log as the source of truth until then.
