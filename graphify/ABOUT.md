# Graphify

**Source repository:** https://github.com/Graphify-Labs/graphify
**Website:** https://graphify.com
**Original author:** Safi Shamsi and the Graphify contributors (Graphify Labs)
**License:** Apache-2.0 (earlier contributions remain available under MIT — see `LICENSE-MIT` upstream)
**Downloaded as:** `graphify-8.zip` — the `v8` branch (deleted after extraction — re-download from the repo above)

All credit goes to the original authors.

## ⚠️ This skill needs a separate install to work

Unlike the other skills in this library, Graphify is **not self-contained**. The `SKILL.md` here is a front-end that drives the `graphify` command-line tool. Without the tool installed, the skill will fail.

```bash
pip install graphifyy
```

(Note the package name is `graphifyy` with two y's, not `graphify`.)

## What it is

Turns a folder of files — code, docs, PDFs, images, video — into a persistent, navigable **knowledge graph** you query instead of grepping. Outputs interactive HTML, GraphRAG-ready JSON, and a plain-language `GRAPH_REPORT.md`.

- Code is parsed with tree-sitter AST: deterministic, fully local, no LLM involved.
- Docs, PDFs, images and video use a semantic pass via your assistant's model or a configured API key.
- Every edge is tagged `EXTRACTED` (explicit in the source) or `INFERRED` (resolved by graphify), so you can tell what was read from what was guessed.
- Not a vector index — no embeddings, no vector store. A real graph you traverse, trace paths through, and ask to explain a concept.

## Skills in this folder (1)

| Skill | What it does |
|---|---|
| `graphify` | The `/graphify` command — builds and queries the knowledge graph. Also triggers on any question about a codebase's architecture or file relationships, especially when a `graphify-out/` directory already exists. |

## Notes

- The upstream file is named `skill.md` (lowercase). It was **renamed to `SKILL.md`** here, because that's what Claude Code looks for. The content is unchanged.
- Upstream also ships harness-specific variants (`skill-codex.md`, `skill-copilot.md`, `skill-aider.md`, `skill-windows.md` and ~10 more). Only the generic `skill.md` was taken. If you hit Windows-specific problems, `skill-windows.md` in the source repo is worth a look.
- The rest of the repo is the Python package itself (the tool you install via pip) — not copied.
