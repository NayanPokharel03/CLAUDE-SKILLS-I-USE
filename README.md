# Skill Library

A personal collection of **191 AI agent skills** gathered from six open-source repositories, organised by source and documented with full attribution.

> **Nothing in this repository is my own work.** Every skill here was written by someone else and is redistributed under its original licence. Each source folder contains an `ABOUT.md` naming the original repository, author and licence. If you find something useful here, please star the original repo — links below.

## Contents

| Folder | Skills | Source | Author | Licence |
|---|---:|---|---|---|
| [`open-design/`](open-design/) | 162 | [nexu-io/open-design](https://github.com/nexu-io/open-design) | nexu-io | Apache-2.0 |
| [`superpowers/`](superpowers/) | 14 | [obra/superpowers](https://github.com/obra/superpowers) | Jesse Vincent | MIT |
| [`ui-ux-pro-max/`](ui-ux-pro-max/) | 7 | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Next Level Builder | MIT |
| [`ponytail/`](ponytail/) | 6 | [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) | Dietrich Gebert | MIT |
| [`karpathy-guidelines/`](karpathy-guidelines/) | 1 | [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) | forrestchang | MIT |
| [`graphify/`](graphify/) | 1 | [Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify) | Safi Shamsi & contributors | Apache-2.0 |

## What each one gives you

**[OpenDesign](open-design/)** — 162 functional design skills: creative direction and critique, branding, front-end and UI, GSAP motion, Figma automation, AI image/video/audio generation across a dozen providers, decks and documents, social and marketing assets, data visualisation. The largest part of this library by far. Extracted from OpenDesign's `skills/` directory; the app itself is not included.

**[Superpowers](superpowers/)** — a complete development methodology as composable skills: brainstorm → spec → plan → red/green TDD → code review → verification before completion. Also covers git worktrees, systematic debugging, and writing new skills.

**[UI UX Pro Max](ui-ux-pro-max/)** — design intelligence backed by a searchable local database: 79 UI styles, 192 palettes, 74 font pairings, 119 UX guidelines, 25 chart types and 22 stack guides.

**[Ponytail](ponytail/)** — "lazy senior dev" mode. Forces the simplest solution that actually works: YAGNI, stdlib before custom code, one line before fifty. Includes over-engineering review and audit tools.

**[Karpathy Guidelines](karpathy-guidelines/)** — four behavioural rules to reduce common LLM coding mistakes, derived from Andrej Karpathy's public observations. (Written by `forrestchang`, not by Karpathy.)

**[Graphify](graphify/)** — turns a codebase into a queryable knowledge graph instead of grepping through files. **Requires `pip install graphifyy`** to function.

## Installing

See [`INSTRUCTIONS.md`](INSTRUCTIONS.md) — it covers Claude Code (automatic, via an AI agent given this folder) and claude.ai chat (manual, and more limited).

Short version for Claude Code: copy every skill folder into `~/.claude/skills/`, then restart your session.

## Things to know

- **Three skill names appear twice.** `ui-ux-pro-max`, `slides` and `brainstorming` each exist in two source folders. A flat install would have one silently overwrite the other — see `INSTRUCTIONS.md` for the prefix convention that keeps both.
- **Roughly 30 skills need paid API keys.** Everything in OpenDesign's fal.ai, Venice, Replicate, Sora, Imagen, MiniMax and Pixelbin groups calls an external service.
- **Context cost.** Installing all 191 at user level puts every skill's description into every session — plausibly 15–25k tokens. Consider a project-level install for the design skills if that matters to you.
## Licensing

Every folder carries its original `LICENSE` file, fetched from the source repository, so the licence text travels with the code as MIT and Apache-2.0 both require. `open-design/` additionally has 20 per-skill `LICENSE` files where individual skills came from elsewhere, and `graphify/` keeps its `NOTICE` and `LICENSE-MIT` alongside the Apache-2.0 text.

**One exception:** `karpathy-guidelines/` has no `LICENSE` file. The upstream repo doesn't ship one — MIT is declared in its manifest and skill frontmatter, but the text is absent. No licence file was invented on the author's behalf. If this library ever goes public, that folder needs the author's licence added or should be left out.

Nothing here is relicensed. Each work stays under its own terms, and the `ABOUT.md` files record who wrote what.

## Maintaining this library

When a new skill repo is added:

1. Inspect the archive before extracting — repo downloads usually bundle several skills under one wrapper folder.
2. Copy only the skill folders (those containing `SKILL.md`, plus their supporting files) into a folder named after the project.
3. Write an `ABOUT.md` in it: source URL, author, licence, version, what it does, a table of every sub-skill, and what was deliberately left out.
4. Check for name collisions against the existing skills.
5. Update this table and `INSTRUCTIONS.md`.
