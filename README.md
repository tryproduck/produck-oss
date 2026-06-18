# 🦆 Produck Skills

**High-quality, user-experience-centered skills for your coding agents.**

[![Star on GitHub](https://img.shields.io/github/stars/tryproduck/produck-oss?style=social)](https://github.com/tryproduck/produck-oss)

> ⭐ **If these skills are useful, [star the repo](https://github.com/tryproduck/produck-oss)** — it helps other builders find it.

An open-source, documentation-driven collection of [agent skills](https://code.claude.com/docs/en/skills).
Each skill is a folder of markdown that teaches a coding agent (Claude Code, Cursor, Codex, Copilot,
and others) how to do one thing well — starting with turning messy user requests into context-rich
PRDs your agents can actually execute.

The whole project is centered on **user experience**: getting from what a user actually wants to
shipped, aligned work without the agent guessing.

---

## Install

One line installs every skill in this repo into your coding agent:

```bash
npx skills add tryproduck/produck-oss
```

That's it. It uses the open [`skills`](https://github.com/vercel-labs/skills) CLI (no global install,
just `npx`) and works across 70+ agents — Claude Code, Cursor, Codex, Copilot, and more. The skills
are available the next time your agent starts.

---

## Skills catalog

| Skill | What it does |
| --- | --- |
| [`user-alignment`](skills/user-alignment/SKILL.md) | Turn vague or messy user requests into aligned, agent-executable PRDs — with scope, bounded phases, testable acceptance criteria, and explicit do-not-do boundaries. |

More user-experience skills are on the way.

---

## Contributing

Want to add a skill? See [CONTRIBUTING.md](CONTRIBUTING.md) for the skill-authoring contract
(folder layout, required frontmatter, and the PR checklist). The bar is high-quality, UX-centered
skills only.

---

## About Produck

These skills come from the team building [Produck](https://tryproduck.com) — **your users talk, your
fixes ship.** Produck turns user feedback into shipped code: users report issues in context, and
coding agents reproduce, fix, and open the PR. The same obsession with capturing real user intent
powers this skills collection.

- 🌐 Website: [tryproduck.com](https://tryproduck.com)
- 📚 Docs: [docs.tryproduck.com](https://docs.tryproduck.com)

## License

[MIT](LICENSE)
