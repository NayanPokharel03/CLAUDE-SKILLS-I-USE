# Superpowers

**Source repository:** https://github.com/obra/superpowers
**Original author:** Jesse Vincent (`obra`) — jesse@fsck.com
**License:** MIT (Copyright (c) 2025 Jesse Vincent)
**Version at time of download:** 6.3.0
**Downloaded as:** `superpowers-main.zip` (deleted after extraction — re-download from the repo above)

All credit for these skills goes to the original author. Nothing here was written by me — this folder only contains the `skills/` directory lifted out of the upstream repository so the skills can be installed directly.

## What it is

A complete software-development methodology for coding agents, delivered as a set of composable skills: spec first, then a plan, then strict red/green TDD, YAGNI and DRY throughout, with verification before anything is called done.

## Skills in this folder (14)

| Skill | What it does |
|---|---|
| `using-superpowers` | Entry point — establishes how to find and use the other skills; expects a skill to be invoked before any response |
| `brainstorming` | Required before any creative work — explores intent, requirements and design before implementation |
| `writing-plans` | Turns a spec into a step-by-step implementation plan |
| `executing-plans` | Executes a written plan in a separate session with review checkpoints |
| `subagent-driven-development` | Executes plans with independent tasks via subagents in the current session |
| `dispatching-parallel-agents` | For 2+ independent tasks with no shared state or ordering |
| `test-driven-development` | Red/green TDD before writing implementation code |
| `systematic-debugging` | Structured approach to any bug or test failure, before proposing fixes |
| `requesting-code-review` | Requests review on completed work before merging |
| `receiving-code-review` | How to handle review feedback with technical rigor, not blind agreement |
| `verification-before-completion` | Requires evidence (actual command output) before claiming anything works |
| `using-git-worktrees` | Isolated workspace for feature work |
| `finishing-a-development-branch` | Deciding how to integrate finished work |
| `writing-skills` | Creating, editing and verifying new skills |

## Notes

- Several skills ship supporting files (`scripts/`, prompt `.md` files, examples) alongside `SKILL.md` — these were kept.
- The rest of the upstream repo (docs, plans, specs, release notes, multi-harness plugin manifests for Codex/Cursor/Devin/Kimi/OpenCode/Pi/Hermes) was not copied. Get it from the source repo above if needed.
