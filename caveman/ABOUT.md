# Caveman

**Source repository:** https://github.com/juliusbrussee/caveman
**Original author:** Julius Brussee
**License:** MIT for this folder — see the licence note below
**Downloaded as:** `caveman-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to the original author. This folder is the upstream `skills/` directory only.

## ⚠️ Licence note — read before making this public

The Caveman repository is **dual-licensed**. Its root `LICENSE` opens with a scope note: MIT covers the repo *except* the Engine-linked directories (`engine/`, `proxy/`, `rewriter/`, `browse/`, `mcp/`, `shrink/`, the cavemem Go core and `shared/platform/`), which are under **Business Source License 1.1** — a source-available licence, not open source, that forbids offering the work to third parties as a hosted or managed service until its Change Date of **2030-06-21**.

`skills/` is **not** on the BSL list, so everything in this folder is MIT. The BSL parts were never copied here. The `LICENSE` file kept alongside is the upstream root licence, including that scope note, so the split stays visible.

## What it is

Token-cost tooling for coding agents, in two halves:

1. **Compression** — a persistent "caveman mode" that strips output to intent only, cutting token spend while keeping technical accuracy. Levels: `lite`, `full`, `ultra`, plus wenyan variants.
2. **Disciplined workflows** — a set of task-shaped skills that force narrow scope, evidence before edits, and verification before claims.

Several skills talk to **Caveman Cloud**, the author's hosted measurement gateway. Those need an account and setup; the rest work standalone.

## Skills in this folder (20)

### Compression & reporting
| Skill | What it does |
|---|---|
| `caveman` | The main mode — ultra-compressed communication. Triggers on `/caveman`, "caveman mode", "be brief", "less tokens" |
| `caveman-compress` | Compresses a memory file (`CLAUDE.md`, a todo list) into caveman format to cut input tokens |
| `caveman-commit` | Conventional Commits message compressed to intent only |
| `caveman-review` | Compressed code review — one line per finding: location, problem, fix |
| `caveman-stats` | Real token usage and estimated savings for the session, read from the session log |
| `caveman-help` | Quick-reference card for modes, skills and commands |

### Engineering discipline (standalone, no account needed)
| Skill | What it does |
|---|---|
| `investigate-first` | Diagnose ambiguous failures *before* editing — unknown causes, intermittent behaviour |
| `surgical-patch` | Fix bugs at the narrowest responsible layer |
| `safe-refactor` | Restructure while preserving behaviour — extraction, consolidation, ownership moves |
| `lean-build` | Build feature work with high overbuilding risk |
| `migration` | Reversible, compatibility-safe transitions — schema, data, API, protocol, config |
| `verify-and-stop` | Prove work meets acceptance conditions without expanding scope |
| `caveman-explore` | Read-only repo explorer for cold-start orientation and cross-file localization |
| `cavecrew` | Delegation rules — when to hand off to the investigator, builder or reviewer subagent |

### Caveman Cloud (needs an account)
| Skill | What it does |
|---|---|
| `caveman-setup` | Wire a repo through the Cloud gateway so LLM requests are measured |
| `caveman-discover` | Find and label every LLM workflow in the repo so spend groups by workflow |
| `caveman-learn` | Act on a learn report — apply cost-lowering fixes to ranked token sinks |
| `caveman-optimize` | Turn an optimization observation into a candidate with a paired baseline evaluation |
| `caveman-evidence-review` | Read-only review of cost, Cave Score, workflows, traces, latency, errors, routing |
| `caveman-manage` | Inspect experiment lifecycle and block unsafe execution |

## Notes

- Upstream ships four of these duplicated under `plugins/caveman/skills/` — only the `skills/` copies were taken.
- Build tooling that shipped in `skills/` (`compile.mjs`, `verbs-gate.mjs`, `registry.json`, `engine-mcp-tools.json`, `native-core.md`) was dropped after confirming no `SKILL.md` references it. `generated/` held per-harness variants for aider, codex, gemini, hermes and opencode — the Claude versions are the ones kept here.
- No name collisions with anything else in this library.
