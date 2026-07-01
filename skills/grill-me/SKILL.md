---
name: grill-me
description: Interviews the user relentlessly about a subject — most often a plan, design, or decision before building, but also their own profile — asking one question at a time until there is shared understanding. Use when the user says "grill me", wants to stress-test a plan or design, wants unstated assumptions surfaced, or wants to be interviewed to fill in the about-me profile.
---

# Grill Me

Interrogate the user about a subject until you both actually understand it. The
default subject is a plan, design, or decision the user is about to act on; a
secondary use is onboarding — grilling the user about themselves to fill the
**about-me** profile.

## When to run
- The user says "grill me", or asks you to stress-test or pressure-test a plan.
- A plan, design, or requirement has unresolved decisions or unstated assumptions.
- The user asks you to get to know them, or the `../about-me/profile.md` has
  _(unknown)_ fields relevant to the work at hand.
- You keep lacking context you could have pinned down by asking.

## How to grill

- Ask **one question at a time**, and wait for the answer before the next. A wall
  of questions at once is bewildering.
- **Offer a recommended answer** with each question, so the user can confirm or
  correct rather than compose from scratch.
- **Don't ask what you can already determine.** If the repo, the plan, the
  profile, or earlier conversation answers a question, resolve it yourself and
  confirm — don't make the user recite it.
- Walk down each branch of the subject, resolving **dependencies one by one**: an
  answer usually opens the next question. Follow the branch before switching.
- Surface **unstated assumptions** and make them explicit.
- Ask natural follow-ups when an answer is vague, surprising, or incomplete.
- Say why you're asking when the reason isn't obvious.
- Never invent answers. If the user skips or declines something, leave it open and
  move on. Respect privacy.

## Where the conclusions go — route by subject

- **Grilling a plan / design / decision (default).** The payoff is shared
  understanding, not a file. Stop when the open branches are resolved. Write a
  short decisions/assumptions summary **only if the user asks**; otherwise carry
  the understanding straight into the work.
- **Grilling for the profile (onboarding).** Route durable answers into
  `../about-me/profile.md`. Use [question-bank.md](question-bank.md) for questions
  grouped by profile topic. Replace each _(unknown)_ you learn with a concise,
  durable entry; do not store one-off task trivia.

## Workflow

Copy this checklist and track progress:

```
Grilling Progress:
- [ ] 1. Identify the subject and scope (a plan/decision, or the profile)
- [ ] 2. Read the relevant context first (repo, plan, ../about-me/profile.md)
- [ ] 3. Grill one question at a time, each with a recommended answer
- [ ] 4. Play back the resolved understanding; let the user correct it
- [ ] 5. Route conclusions (profile → profile.md; plan → summary only if asked)
```

1. **Scope it.** Confirm what you're grilling and how deep to go.
2. **Read context first** so you never ask what you could determine.
3. **Grill** down the branches, one question at a time.
4. **Play it back.** Summarize the resolved understanding and let the user correct
   it before you rely on it or save anything.
5. **Route conclusions** per the section above.

## After grilling
Tell the user what got resolved. For profile grilling, say what you saved and
which fields are still _(unknown)_. For plan grilling, state the shared
understanding you're proceeding on (and offer to write it down if useful).
