# Karpathy Guidelines

**Source repository:** https://github.com/multica-ai/andrej-karpathy-skills
**Original author:** `forrestchang` — X/Twitter: https://x.com/jiayuan_jy
**License:** MIT — but see the note below
**Version at time of download:** 1.0.0
**Downloaded as:** `andrej-karpathy-skills-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to the original author. This folder is the upstream `skills/karpathy-guidelines/` directory, copied so the skill can be installed directly.

> **Licence note:** this is the one folder here with **no `LICENSE` file**. The upstream repository doesn't ship one — MIT is declared in `.claude-plugin/plugin.json` and in the `SKILL.md` frontmatter, but the licence text itself is absent from the repo (confirmed against both the downloaded archive and the live repo, which returns 404 for `LICENSE`). I haven't written one in, because inventing a licence file on someone's behalf isn't mine to do. If this library is ever made public, ask the author to add one, or leave this folder out.

> **Attribution note:** the archive credits the *ideas* to Andrej Karpathy's public observations on LLM coding pitfalls (https://x.com/karpathy/status/2015883857489522876), but Karpathy is not the author of this skill — `forrestchang` is. The repo name is `andrej-karpathy-skills`, which is easy to misread.

## What it is

A single skill containing four behavioural guidelines meant to reduce common LLM coding mistakes. Applies when writing, reviewing or refactoring code.

| Principle | Addresses |
|---|---|
| **Think Before Coding** | Wrong assumptions, hidden confusion, unsurfaced tradeoffs |
| **Simplicity First** | Overcomplication, bloated abstractions |
| **Surgical Changes** | Touching orthogonal code, removing things it doesn't understand |
| **Goal-Driven Execution** | Tests-first, verifiable success criteria |

## Skills in this folder (1)

| Skill | What it does |
|---|---|
| `karpathy-guidelines` | The guidelines above, as a single self-contained `SKILL.md` |

## Notes

- Self-contained — one `SKILL.md`, no scripts or supporting files.
- The skill itself notes a tradeoff: it biases toward caution over speed, so for trivial tasks use judgment.
- The upstream repo also ships a `CLAUDE.md`, a Cursor rules file, `EXAMPLES.md` and a Chinese README — not copied.
