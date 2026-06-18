# Contributing a skill

Produck Skills is a collection of **high-quality, user-experience-centered** agent skills. This guide
is the contract for adding one.

## What makes a good skill here

- It improves how a coding agent understands or serves **real user experience** — capturing intent,
  reducing ambiguity, shipping the right thing.
- It is **opinionated and operational**, not a generic explainer. It tells the agent what to do.
- It is **self-contained**: one skill, one folder, one clear job.

## Folder layout

Every skill is one folder under `skills/`, containing a `SKILL.md` entry point:

```
skills/
  <skill-name>/
    SKILL.md            # required — the entry point
    references/         # optional — deeper docs, templates, long checklists
      <topic>.md
    scripts/            # optional — helper scripts the skill references
```

- `<skill-name>` is kebab-case and matches the `name` field in the frontmatter.
- The `skills` CLI discovers a skill by finding its `SKILL.md`.

## Required frontmatter

`SKILL.md` must start with YAML frontmatter. Only `name` and `description` are required.

```yaml
---
name: your-skill-name
description: Use when <trigger>. <What it does and the outcome it produces.> Triggers on <concrete situations>.
license: MIT
metadata:
  author: your-handle
  version: "1.0.0"
---
```

- **`name`** — kebab-case, matches the folder name.
- **`description`** — write it **trigger-first** ("Use when…"). This is what the agent reads to
  decide whether to surface the skill, so describe the situations that should activate it, then the
  outcome. Avoid vague adjectives.

## Keep SKILL.md lean

The agent loads `SKILL.md` into context when the skill activates, so keep the entry point focused on
the operational core. Push long templates, citation lists, and exhaustive checklists into
`references/` and link to them (progressive disclosure). See
[`skills/user-alignment`](skills/user-alignment/SKILL.md) for the pattern — a tight SKILL.md that
links to `references/prd-template.md` and `references/reading-list.md`.

## Test it locally

Install your skill into a real agent before opening a PR:

```bash
npx skills add <your-fork-or-branch-path> --skill <skill-name>
```

Confirm it shows up in your agent (e.g. `.claude/skills/<skill-name>/SKILL.md`) and that the
description triggers it on the situations you intended.

## PR checklist

- [ ] New skill lives in `skills/<skill-name>/SKILL.md`.
- [ ] Frontmatter has `name` (matches folder) and a trigger-first `description`.
- [ ] `SKILL.md` is lean; depth is in `references/`.
- [ ] The skill is UX-centered and operational, not a generic explainer.
- [ ] Added a row to the **Skills catalog** table in `README.md`.
- [ ] Installed and verified the skill locally in at least one agent.
