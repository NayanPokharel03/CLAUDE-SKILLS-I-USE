# Instructions

How to get the 191 skills in this folder working. Two very different targets — pick the section you need.

---

# Part 1 — Claude Code

**Give this section to a Claude Code agent along with this folder. It can do the whole thing itself.**

## What to do

Install every skill into the user-level skills directory so they're available in every session, in every project.

**Target:**
- Windows: `C:\Users\<you>\.claude\skills\`
- macOS / Linux: `~/.claude/skills/`

(Use a project-level `.claude/skills/` inside a single project instead if you only want them there.)

## The structure you're reading from

This folder groups skills **by source repository**:

```
open-design/          162 skill folders + ABOUT.md
superpowers/           14 skill folders + ABOUT.md
ui-ux-pro-max/          7 skill folders + ABOUT.md
ponytail/               6 skill folders + ABOUT.md
karpathy-guidelines/    SKILL.md + ABOUT.md      <- itself a skill
graphify/               SKILL.md + ABOUT.md      <- itself a skill
```

The install target is **flat** — every skill sits directly in `skills/`, with no grouping. So you're flattening one level, with two exceptions:

- `karpathy-guidelines/` and `graphify/` contain a `SKILL.md` directly. Copy the folder itself.
- Every other folder is a *group*. Copy its subfolders, not the folder.

## Handle the name collisions

Three skill names exist in two places. A flat copy makes one overwrite the other silently. Install OpenDesign's copies under a prefix so both survive:

| From `open-design/` | Install as |
|---|---|
| `ui-ux-pro-max` | `od-ui-ux-pro-max` |
| `slides` | `od-slides` |
| `brainstorming` | `od-brainstorming` |

The non-prefixed names go to the dedicated repos' versions: `ui-ux-pro-max` and `slides` from UI UX Pro Max, `brainstorming` from Superpowers.

## Script

Bash / Git Bash / WSL — run from inside this folder:

```bash
S="$HOME/.claude/skills"; mkdir -p "$S"
for r in superpowers ponytail ui-ux-pro-max karpathy-guidelines graphify; do
  if [ -f "$r/SKILL.md" ]; then cp -r "$r" "$S/$r"
  else for s in "$r"/*/; do cp -r "$s" "$S/$(basename "$s")"; done; fi
done
for s in open-design/*/; do b=$(basename "$s")
  case "$b" in ui-ux-pro-max|slides|brainstorming) t="od-$b";; *) t="$b";; esac
  cp -r "$s" "$S/$t"
done
```

## Verify

Every installed folder must contain a `SKILL.md`, and the count should be 191:

```bash
S="$HOME/.claude/skills"
echo "folders: $(ls -d "$S"/*/ | wc -l)"
for d in "$S"/*/; do [ -f "$d/SKILL.md" ] || echo "MISSING SKILL.md: $d"; done
```

## Then tell the user

- **Restart the session.** Claude Code reads the skills list at startup, so the current session won't see them.
- **`graphify` needs `pip install graphifyy`** (two y's) or it will fail — it's a front-end for a CLI, not self-contained.
- **~30 OpenDesign skills need paid API keys** (fal.ai, Venice, Replicate, Sora, Imagen, MiniMax, Pixelbin).
- **Context cost:** all 191 descriptions load into every session — plausibly 15–25k tokens. If that's unwelcome, install only `superpowers`, `ponytail`, `karpathy-guidelines` and `graphify` at user level, and put `open-design` and `ui-ux-pro-max` in a project-level `.claude/skills/` where design work happens.

## Notes

- `ABOUT.md` files get copied along with the skills. Harmless — Claude Code ignores anything that isn't `SKILL.md`.
- Don't rename or edit any `SKILL.md`. The frontmatter `description` is what triggers the skill.
- Skills are *invoked*, not always-on. Their descriptions determine when they fire; a skill can always be named directly.

---

# Part 2 — claude.ai (chat)

**Read this before trying: claude.ai cannot install these automatically.** Uploading this folder to a conversation or Project does **not** install anything. Claude has no filesystem access and cannot turn uploaded files into installed Skills — that's a settings action only you can perform.

You have two options, and they work differently.

## Option A — Install properly as claude.ai Skills (manual, one at a time)

The real thing: the skill loads on demand, the way it does in Claude Code.

1. Zip a **single** skill folder, with its `SKILL.md` at the top level of the zip. Example — `ponytail/ponytail/` zipped so the archive contains `SKILL.md`, not `ponytail/SKILL.md`.
2. In claude.ai, go to **Settings → Capabilities → Skills**.
3. Upload the zip.
4. Repeat for each skill you want.

**Caveats:**
- One skill per upload. There is no bulk import — 191 uploads is not realistic, so pick the handful you actually use.
- Skills with large bundled data may exceed upload limits. `ui-ux-pro-max` (3.6 MB) and `ui-styling` (5.8 MB) are the likely problems.
- Skills that shell out to scripts or CLIs (`graphify`, the fal.ai/Venice/Replicate group, anything calling `.py` or `.sh`) will **not** work in chat. They need a local machine. Only prose-and-reference skills transfer cleanly.

**Good candidates:** `ponytail`, `karpathy-guidelines`, `brainstorming`, `writing-plans`, `test-driven-development`, `systematic-debugging`, `copywriting`, `color-expert`, `apple-hig`, `web-design-guidelines`.

## Option B — Upload as reference material (fast, informal)

Attach the `SKILL.md` files to a conversation or add them to a Project's knowledge, then instruct Claude to follow them. Not a real Skill install — Claude treats them as instructions for that conversation — but it works and takes seconds.

Paste this along with the files:

> I've given you skill files from my library. Each `SKILL.md` is an instruction set, and its frontmatter `description` says when it applies.
>
> Treat them as active instructions, not documents. When a task matches one, follow its steps and tell me which skill you're applying. If two conflict, say so and let me choose. If a skill references a script, data file or reference doc I haven't given you, tell me rather than guessing at its contents.
>
> You can't read my computer — I have to upload files. If you need a skill I haven't attached, ask for it by name.

**Caveats:**
- Applies only to that conversation (or Project). Nothing persists elsewhere.
- Uses context on every message, so attach a few relevant skills, not the whole library.
- Weaker than a real install: skills won't auto-trigger, you'll often need to point at them.

## Which to use

Use **Option A** for the few skills you rely on constantly and want to just work. Use **Option B** for one-off tasks, or to try a skill before committing to installing it.
