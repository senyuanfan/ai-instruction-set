# ai-instruction-set

A personal set of [Agent Skills](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
that teach an AI assistant how to **learn about me, work with me, and work for me**.

Each skill follows Anthropic's
[skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices):
a `SKILL.md` with `name` + `description` frontmatter, a concise body under 500
lines, and detail pushed into one-level-deep reference files (progressive
disclosure).

## Skills

| Skill | What it does |
| --- | --- |
| [`about-me`](skills/about-me/) | Serves the user's profile of record — identity, working style, preferences, environment, and goals — so the assistant can tailor its work. |
| [`grill-me`](skills/grill-me/) | Interrogates the user one question at a time to reach shared understanding — stress-testing a plan or design, or (as one mode) filling in the `about-me` profile. |

In profile mode, the two work together: **`grill-me` gathers** the information that **`about-me` serves**.

## Layout

```
skills/
├── about-me/
│   ├── SKILL.md        # overview + how to apply the profile
│   └── profile.md      # the profile of record (edit me / filled by grill-me)
└── grill-me/
    ├── SKILL.md        # interview workflow
    └── question-bank.md # questions grouped by topic
```

## Install

Skills are discovered in a `skills/` directory under a Claude settings folder.
To use these personally across all projects, link or copy each skill into your
user skills directory:

```bash
mkdir -p ~/.claude/skills
ln -s "$(pwd)/skills/about-me" ~/.claude/skills/about-me
ln -s "$(pwd)/skills/grill-me" ~/.claude/skills/grill-me
```

To scope them to a single project instead, place them under that project's
`.claude/skills/`.

## Getting started

1. Install the skills (above).
2. Ask the assistant to "grill me about myself" — it runs `grill-me` and fills in
   `skills/about-me/profile.md`.
3. From then on, the assistant reads `about-me` to work the way you prefer.

## Adding more skills

New skills go in their own folder under `skills/`, each with a `SKILL.md`. Keep
the body concise, write the `description` in the third person stating **what** the
skill does and **when** to use it, and move long detail into reference files
linked one level deep from `SKILL.md`.
