# Security Audit

**Source repository:** https://github.com/cloudflare/security-audit-skill
**Original author:** Cloudflare, Inc.
**License:** MIT (Copyright (c) 2025-2026 Cloudflare, Inc.)
**Downloaded as:** `security-audit-skill-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to Cloudflare. This folder is the upstream `skills/security-audit/` directory plus the repo's `LICENSE`.

## What it is

Turns a coding agent into a security auditor. It orchestrates isolated sub-agents through a six-phase audit and produces structured, verifiable findings rather than a prose opinion.

This is the skill that seeded Cloudflare's own vulnerability-discovery harness, described in [Build your own vulnerability harness](https://blog.cloudflare.com/build-your-own-vulnerability-harness). Their production system grew into a fleet-wide multi-stage pipeline; this is the single-repo starting point it evolved from.

### The six phases

1. **Reconnaissance** — map architecture, trust boundaries, input surfaces and prior evidence into `architecture.md` and `coverage-ledger.json`
2. **Coverage-led hunting** — assign isolated hunters from ledger units, record their checks, use coverage critics to find gaps
3. **Candidate validation** — hand every unique candidate to a fresh verifier that tries to *disprove* it
4. **Structured output** — write `confirmed` / `needs_validation` / `rejected` records to `findings.json`, validated against `report-schema.json`
5. **Independent record verification** — fresh agents verify final source claims; material replacements get another independent verifier
6. **Target-neutral reporting** — derive `REPORT.md`, `FINDINGS-DETAIL.md` and `NEEDS-VALIDATION.md` from verified records

Verdicts are deliberately distinct: `confirmed` requires a complete source trace and a bounded observed result; `needs_validation` names an exact unresolved fact and carries no severity; `rejected` records a disproved candidate. Runs against the same repo are additive — prior ledgers target gaps and revalidate changed source instead of treating stale work as covered.

## Skills in this folder (1)

| Skill | What it does |
|---|---|
| `security-audit` | The full orchestrated audit above |

It's one skill, but a large one — 15 reference documents covering attack classes, reconnaissance, hunting methodology, validation and reporting, plus domain guides for web/auth, client-side, cloud, memory safety, supply chain, protocols and RPC, desktop/mobile/IPC, data isolation, resource exhaustion, and AI/LLM-specific attacks.

## Requirements

- **Node.js** — the skill runs `validate-coverage-ledger.cjs` and `validate-findings.cjs` to check its own output. Without Node these validation steps fail.
- **Sub-agent capability** — the methodology depends on dispatching isolated agents for hunting and verification. It degrades without that.

## Notes

- Self-contained apart from Node; no API keys or external services.
- Test files (`*.test.cjs`) ship alongside the validators and were kept — they're how you confirm the validators work.
- Intended for auditing code you own or are authorised to test.
