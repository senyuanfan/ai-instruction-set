---
name: grill-me
description: Interviews the user to learn about them — background, communication and working style, technical environment, current projects, and goals — and records the answers into the about-me profile. Use when the user says "grill me", "get to know me", or "learn about me", when onboarding a new setup, or when the about-me profile is missing information needed for the current task.
---

# Grill Me

A guided interview to learn about the user and capture it durably in the **about-me** profile.

## When to run
- The user asks you to get to know them, or says "grill me".
- The profile at `../about-me/profile.md` has _(unknown)_ fields relevant to the work at hand.
- You keep lacking context you could have gathered once.

## Interview principles
- Ask **one topic at a time**, and wait for the answer before moving on.
- Keep each turn short — a few focused questions, never a wall of them.
- **Offer a recommended answer** with each question, so the user can confirm or correct rather than compose from scratch.
- **Don't ask what you can already determine.** If context you have (the resume, this repo, earlier conversation) answers a field, fill it in and confirm instead of asking.
- Ask natural follow-ups when an answer is vague or interesting.
- Say why you're asking when the reason isn't obvious.
- Never invent answers. If the user skips something, leave it _(unknown)_ and move on.
- Respect privacy — if the user declines a topic, drop it without pushing.

## Workflow

Copy this checklist and track progress:

```
Interview Progress:
- [ ] 1. Confirm scope — full onboarding, or fill specific gaps
- [ ] 2. Read ../about-me/profile.md to see what's already known
- [ ] 3. Ask through the relevant categories
- [ ] 4. Play back what you heard; let the user correct it
- [ ] 5. Write durable answers into ../about-me/profile.md
```

1. **Confirm scope.** Ask whether they want a full introduction or just to fill the gaps needed for the current task.
2. **Read the current profile** (`../about-me/profile.md`) so you never re-ask a known fact.
3. **Ask by category.** See [question-bank.md](question-bank.md) for questions grouped by topic. Cover only what is missing or relevant to the scope.
4. **Play it back.** Summarize their answers and ask them to correct anything before you save.
5. **Record.** Update the matching sections of `../about-me/profile.md` with concise, durable entries. Replace each _(unknown)_ placeholder you learned; do not store one-off task trivia.

## After the interview
Tell the user what you saved and which fields are still _(unknown)_, so they know what's left to cover next time.
