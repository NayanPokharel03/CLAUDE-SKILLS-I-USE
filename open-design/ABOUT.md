# OpenDesign

**Source repository:** https://github.com/nexu-io/open-design
**Website:** https://open-design.ai
**Original author:** nexu-io (OpenDesign)
**License:** Apache-2.0 (individual skills may carry their own `LICENSE` — see the upstream `README.md` kept in this folder)
**Downloaded as:** `open-design-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to the original authors. This folder is the upstream `skills/` directory only.

## What it is

OpenDesign is an open-source, local-first design app that exposes itself to coding agents over MCP. This folder is **just its skill library** — 162 functional skills for design, media generation, front-end work and content production.

## What was and wasn't copied

**Copied:** `skills/` — 162 skills (~3.9 MB), plus the upstream `README.md` and `AGENTS.md` that describe the folder's conventions.

**Not copied:** everything else in a 265 MB / 14,041-file monorepo — the desktop app (`apps/`), `figma-plugin/`, `packages/`, `design-systems/`, `e2e/`, `deploy/`, `charts/`, and `design-templates/` (115 more `SKILL.md` files, which upstream classifies as *rendering templates* rather than functional skills — deliberately left out to avoid duplication).

## The skills, by group

| Group | Skills |
|---|---|
| **Design direction & critique** | `creative-director`, `design-brief`, `design-consultation`, `design-review`, `plan-design-review`, `taste-skill`, `taste-skill-v1`, `gpt-tasteskill`, `impeccable-design-polish`, `soft-skill`, `color-expert`, `apple-hig`, `web-design-guidelines`, `platform-design`, `reference-design-contract` |
| **Branding** | `brandkit`, `brand-extract`, `brand-guidelines`, `theme-factory`, `domain-name-brainstormer` |
| **Front-end & UI** | `frontend-design`, `frontend-dev`, `frontend-skill`, `ui-skills`, `ui-ux-pro-max`, `shadcn-ui`, `swiftui-design`, `flutter-animating-apps`, `image-to-code-skill`, `web-clone`, `redesign-skill`, `login-flow`, `faq-page`, `artifacts-builder`, `web-artifacts-builder`, `design-md` |
| **Motion & animation** | `gsap-core`, `gsap-timeline`, `gsap-scrolltrigger`, `gsap-plugins`, `gsap-react`, `gsap-frameworks`, `gsap-performance`, `gsap-utils`, `emilkowalski-motion`, `emil-design-eng`, `review-animations`, `remotion`, `shader-dev`, `threejs`, `chat-motion-overlay`, `vfx-text-cursor` |
| **Figma** | `figma-use`, `figma-generate-design`, `figma-implement-design`, `figma-generate-library`, `figma-create-new-file`, `figma-code-connect-components`, `figma-create-design-system-rules` |
| **AI image / video / audio (fal.ai)** | `fal-generate`, `fal-image-edit`, `fal-vision`, `fal-upscale`, `fal-restore`, `fal-train`, `fal-tryon`, `fal-3d`, `fal-realtime`, `fal-video-edit`, `fal-lip-sync`, `fal-kling-o3` |
| **AI media (other providers)** | `imagegen`, `imagegen-frontend-web`, `imagegen-frontend-mobile`, `imagen`, `nanobanana-ppt`, `replicate`, `sora`, `speech`, `venice-image-generate`, `venice-image-edit`, `venice-video`, `venice-audio-music`, `venice-audio-speech`, `minimax-docx`, `minimax-pdf`, `pixelbin-media`, `stitch-skill`, `stitch-loop`, `image-enhancer`, `ai-music-album` |
| **Decks & documents** | `slides`, `frontend-slides`, `ppt-keynote`, `pptx`, `pptx-generator`, `pptx-html-fidelity-audit`, `deck-guizang-editorial`, `deck-open-slide-canvas`, `deck-swiss-international`, `html-ppt-retro-quarterly-review`, `doc`, `docx`, `pdf`, `doc-kami-parchment`, `data-report`, `release-notes-one-pager`, `resume-modern` |
| **Social & marketing** | `ad-creative`, `competitive-ads-extractor`, `copywriting`, `marketing-psychology`, `paywall-upgrade-cro`, `card-twitter`, `card-xiaohongshu`, `social-x-post-card`, `social-reddit-card`, `social-spotify-card`, `poster-hero`, `screenshots-marketing`, `ecommerce-image-workflow`, `gif-sticker-maker`, `slack-gif-creator` |
| **Data & diagrams** | `d3-visualization`, `frame-data-chart-nyt`, `frame-flowchart-sticky`, `hand-drawn-diagrams`, `canvas-design`, `algorithmic-art`, `article-magazine` |
| **Video frames & templates** | `frame-glitch-title`, `frame-light-leak-cinema`, `frame-liquid-bg-hero`, `frame-logo-outro`, `frame-macos-notification`, `mockup-device-3d`, `video-hyperframes`, `8-bit-orbit-video-template`, `weread-year-in-review-video-template`, `swiss-user-research-video-template`, `swiss-creative-mode-template`, `after-hours-editorial-template`, `editorial-burgundy-principles-template`, `field-notes-editorial-template`, `digits-fintech-swiss-template`, `brutalist-skill`, `minimalist-skill`, `wpds` |
| **Utilities & workflow** | `agent-browser`, `screenshot`, `full-page-screenshot`, `video-downloader`, `youtube-clipper`, `enhance-prompt`, `brainstorming`, `research-decision-room`, `library-curator`, `output-skill`, `writing-guidelines`, `export-download-debugging`, `pr-feedback-quality-gate`, `hatch-pet` |

## Things to know before installing

- **Name collisions.** Three skills here share a folder name with skills already in this library: `ui-ux-pro-max` (vs. the nextlevelbuilder one), `slides` (vs. the nextlevelbuilder one), and `brainstorming` (vs. superpowers). If you install everything flat into `~/.claude/skills/`, one will overwrite the other — rename or pick one before installing.
- **Many skills need API keys.** Everything under the fal.ai, Venice, Replicate, Sora, Imagen, MiniMax and Pixelbin groups calls a paid external service and will not work without your own credentials.
- **`web-clone/`** is adapted from https://github.com/Jane-xiaoer/claude-skill-web-clone — credit to that author.
- Some skills use `od.mode` frontmatter, which is an OpenDesign-specific field. It's harmless elsewhere, but those skills may assume the OpenDesign daemon is present.
