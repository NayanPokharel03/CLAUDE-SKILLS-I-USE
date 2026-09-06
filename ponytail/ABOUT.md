# Ponytail

**Source repository:** https://github.com/DietrichGebert/ponytail
**Original author:** Dietrich Gebert (`DietrichGebert`)
**License:** MIT (Copyright (c) 2026 DietrichGebert)
**Version at time of download:** 4.9.0
**Downloaded as:** `ponytail-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to the original author. This folder is just the upstream `skills/` directory, copied so the skills can be installed directly.

## What it is

"Lazy senior dev mode." Forces the simplest, shortest solution that actually works: YAGNI, standard library before custom code, native platform features before dependencies, one line before fifty. Stays active across responses until turned off.

Intensity levels: `lite`, `full` (default), `ultra` — switched with `/ponytail lite|full|ultra`.

## Skills in this folder (6)

| Skill | What it does |
|---|---|
| `ponytail` | The main persistent mode — biases every coding response toward the minimal solution |
| `ponytail-review` | Code review that only hunts over-engineering: what to delete, what stdlib replaces it |
| `ponytail-audit` | Same as review but repo-wide instead of on a diff — ranked list of what to cut |
| `ponytail-debt` | Collects every `ponytail:` shortcut comment in the codebase into a debt ledger |
| `ponytail-gain` | One-shot scoreboard of ponytail's measured benchmark impact |
| `ponytail-help` | Quick-reference card for all modes, skills and commands |

## Notes

- Each skill is a single self-contained `SKILL.md` — no scripts or supporting files needed.
- The upstream repo also ships the same rules for ~20 other agents (Cursor, Cline, Kiro, OpenCode, Copilot, Codex, Devin, Grok, OpenClaw…), plus hooks, an npm CLI and benchmarks. None of that was copied — see the source repo.
