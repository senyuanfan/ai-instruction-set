# Compression Schema

The seven fields every item is compressed into, with definitions and a copyable
template. Keep entries short — this is a compressor, not notes.

## Contents
- Field definitions
- Output template
- Worked example

## Field definitions

- **Core claim** — the single thing the author is actually arguing, in one
  sentence. Quote the source if you can. If there are several claims, list the
  main one and note the rest under Open questions. Strip hedging and marketing.
- **Evidence** — the concrete support: data, experiments, citations, lived
  reports, benchmarks. Note the *type* and *strength* (a controlled study ≠ an
  anecdote ≠ a vibe). If the claim rests on no evidence, say so plainly.
- **Novelty** — what is genuinely new relative to what's already known or already
  in the log. Be strict: "none — restates prior work" is a valid and common
  answer. This is the anti-noise field.
- **Confidence** — High / Medium / Low that the core claim is true, with a short
  *why* (evidence quality, source track record, independent corroboration).
  Confidence is about truth, not about how confidently the author asserts it.
- **Incentives** — biases or motivations that could shape the framing: who funded
  or benefits, what the author is selling, ideological priors, audience they're
  performing for. Not an accusation — a discount factor.
- **Actionability** — is there anything worth doing or changing? Be concrete
  ("switch X to Y", "watch for Z"), or state "none" honestly.
- **Open questions** — what remains uncertain, untested, or unexplained; what you'd
  need to resolve confidence; any predictions to score later.

## Output template

```
Source: <title / url / who-and-where>   Type: <article|paper|video|thread|meeting|notes>

Core claim:    <one sentence, quoted where possible>
Evidence:      <what supports it, and how strong>
Novelty:       <what's new vs. known — or "none" and why>
Confidence:    <High|Medium|Low> — <why>
Incentives:    <biases/motivations that may shape it>
Actionability: <what to do/change — or "none">
Open questions:<what's still uncertain; predictions to revisit>
```

## Worked example

```
Source: "Small models beat large ones for agents" — X thread, @someone   Type: thread

Core claim:    A fine-tuned 7B agent matches a frontier model on their internal tool-use eval.
Evidence:      One private eval, no numbers shown, no baseline described. Weak.
Novelty:       Low — task-specific small models matching big ones is a known result.
Confidence:    Low — single unshared benchmark, author sells a fine-tuning product.
Incentives:    Author runs a fine-tuning startup; thread is lead-gen.
Actionability: None yet; worth watching if they publish the eval.
Open questions:Which tasks? What frontier baseline? Does it hold out of distribution?
```
