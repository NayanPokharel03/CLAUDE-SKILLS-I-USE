# OpenDesign

**Source repository:** https://github.com/nexu-io/open-design
**Website:** https://open-design.ai
**Original author:** nexu-io (OpenDesign)
**License:** Apache-2.0 (individual skills may carry their own `LICENSE` — see the upstream `README.md` kept in this folder)
**Downloaded as:** `open-design-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to the original authors. This folder is the upstream `skills/` directory only.

## What it is

OpenDesign is an open-source, local-first design app that exposes itself to coding agents over MCP. This folder holds **77 of its skills** — design, media, front-end and content production.

## Why 77 and not 162

Upstream's `skills/` directory has 162 entries, but **85 of them are catalogue pointers, not skills**. Each is a ~1.2 KB `SKILL.md` carrying a description, an upstream link, and boilerplate telling you to go install the real thing yourself — no assets, no scripts, no working instructions. OpenDesign ships them so its own agent knows those skills *exist* during planning.

Installed, they're worse than absent: they consume description tokens in every session and, when triggered, can only tell you the capability isn't available. All 85 were removed. The 77 that remain have real content.

If you want any of them for real, install from the source — several are worth it (GSAP, Figma, fal.ai, the Anthropic skills):

| Upstream repo | Entries dropped |
|---|---|
| [fal-ai-community/skills](https://github.com/fal-ai-community/skills) | `fal-3d`, `fal-generate`, `fal-image-edit`, `fal-kling-o3`, `fal-lip-sync`, `fal-realtime`, `fal-restore`, `fal-train`, `fal-tryon`, `fal-upscale`, `fal-video-edit`, `fal-vision` |
| [figma/skills](https://github.com/figma/skills) | `figma-code-connect-components`, `figma-create-design-system-rules`, `figma-create-new-file`, `figma-generate-design`, `figma-generate-library`, `figma-implement-design`, `figma-use` |
| [openai/skills](https://github.com/openai/skills) | `doc`, `frontend-skill`, `imagegen`, `screenshot`, `slides`, `sora`, `speech` |
| [MiniMax-AI/skills](https://github.com/MiniMax-AI/skills) | `frontend-dev`, `gif-sticker-maker`, `minimax-docx`, `minimax-pdf`, `pptx-generator`, `shader-dev` |
| [veniceai/skills](https://github.com/veniceai/skills) | `venice-audio-music`, `venice-audio-speech`, `venice-image-edit`, `venice-image-generate`, `venice-video` |
| [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | `ad-creative`, `copywriting`, `marketing-psychology`, `paywall-upgrade-cro` |
| [google-labs-code/skills](https://github.com/google-labs-code/skills) | `design-md`, `enhance-prompt`, `shadcn-ui`, `stitch-loop` |
| [garrytan/gstack](https://github.com/garrytan/gstack) | `design-consultation`, `design-review`, `plan-design-review` |
| [CloudAI-X/threejs-skills](https://github.com/CloudAI-X/threejs-skills) | `threejs` |
| [ComposioHQ/awesome-claude-skills/tree/master/artifacts-builder](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/artifacts-builder) | `artifacts-builder` |
| [ComposioHQ/awesome-claude-skills/tree/master/competitive-ads-extractor](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/competitive-ads-extractor) | `competitive-ads-extractor` |
| [ComposioHQ/awesome-claude-skills/tree/master/domain-name-brainstormer](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/domain-name-brainstormer) | `domain-name-brainstormer` |
| [ComposioHQ/awesome-claude-skills/tree/master/image-enhancer](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/image-enhancer) | `image-enhancer` |
| [ComposioHQ/awesome-claude-skills/tree/master/video-downloader](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/video-downloader) | `video-downloader` |
| [LewisLiu007/full-page-screenshot](https://github.com/LewisLiu007/full-page-screenshot) | `full-page-screenshot` |
| [Shpigford/screenshots](https://github.com/Shpigford/screenshots) | `screenshots-marketing` |
| [WordPress/skills](https://github.com/WordPress/skills) | `wpds` |
| [anthropics/skills/tree/main/skills/algorithmic-art](https://github.com/anthropics/skills/tree/main/skills/algorithmic-art) | `algorithmic-art` |
| [anthropics/skills/tree/main/skills/brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines) | `brand-guidelines` |
| [anthropics/skills/tree/main/skills/canvas-design](https://github.com/anthropics/skills/tree/main/skills/canvas-design) | `canvas-design` |
| [anthropics/skills/tree/main/skills/docx](https://github.com/anthropics/skills/tree/main/skills/docx) | `docx` |
| [anthropics/skills/tree/main/skills/pdf](https://github.com/anthropics/skills/tree/main/skills/pdf) | `pdf` |
| [anthropics/skills/tree/main/skills/pptx](https://github.com/anthropics/skills/tree/main/skills/pptx) | `pptx` |
| [anthropics/skills/tree/main/skills/slack-gif-creator](https://github.com/anthropics/skills/tree/main/skills/slack-gif-creator) | `slack-gif-creator` |
| [anthropics/skills/tree/main/skills/theme-factory](https://github.com/anthropics/skills/tree/main/skills/theme-factory) | `theme-factory` |
| [anthropics/skills/tree/main/skills/web-artifacts-builder](https://github.com/anthropics/skills/tree/main/skills/web-artifacts-builder) | `web-artifacts-builder` |
| [bitwize-music-studio/claude-ai-music-skills](https://github.com/bitwize-music-studio/claude-ai-music-skills) | `ai-music-album` |
| [ehmo/platform-design-skills](https://github.com/ehmo/platform-design-skills) | `platform-design` |
| [flutter/skills](https://github.com/flutter/skills) | `flutter-animating-apps` |
| [ibelick/ui-skills](https://github.com/ibelick/ui-skills) | `ui-skills` |
| [jiannanya/snow-d3/](https://github.com/jiannanya/snow-d3/) | `d3-visualization` |
| [meodai/skill.color-expert](https://github.com/meodai/skill.color-expert) | `color-expert` |
| [muthuishere/hand-drawn-diagrams](https://github.com/muthuishere/hand-drawn-diagrams) | `hand-drawn-diagrams` |
| [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | `ui-ux-pro-max` |
| [obra/superpowers](https://github.com/obra/superpowers) | `brainstorming` |
| [op7418/NanoBanana-PPT-Skills](https://github.com/op7418/NanoBanana-PPT-Skills) | `nanobanana-ppt` |
| [op7418/Youtube-clipper-skill](https://github.com/op7418/Youtube-clipper-skill) | `youtube-clipper` |
| [pixelbin-dev/skills](https://github.com/pixelbin-dev/skills) | `pixelbin-media` |
| [raintree-technology/apple-hig-skills](https://github.com/raintree-technology/apple-hig-skills) | `apple-hig` |
| [remotion-dev/remotion](https://github.com/remotion-dev/remotion) | `remotion` |
| [replicate/skills](https://github.com/replicate/skills) | `replicate` |
| [sanjay3290/imagen](https://github.com/sanjay3290/imagen) | `imagen` |
| [smixs/creative-director-skill](https://github.com/smixs/creative-director-skill) | `creative-director` |
| [wholiver/swiftui-design-skill](https://github.com/wholiver/swiftui-design-skill) | `swiftui-design` |
| [zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides) | `frontend-slides` |


## What was and wasn't copied

**Copied:** the 77 substantive skills from `skills/` (~3.6 MB), plus the upstream `README.md` and `AGENTS.md` describing the folder's conventions.

**Not copied:** everything else in a 265 MB / 14,041-file monorepo — the desktop app (`apps/`), `figma-plugin/`, `packages/`, `design-systems/`, `e2e/`, `deploy/`, `charts/`, and `design-templates/` (115 more `SKILL.md` files, which upstream classifies as *rendering templates* rather than functional skills — deliberately left out to avoid duplication).

## The skills, by group

| Group | Skills |
|---|---|
| **Motion & animation** (14) | `gsap-core`, `gsap-timeline`, `gsap-scrolltrigger`, `gsap-plugins`, `gsap-react`, `gsap-frameworks`, `gsap-performance`, `gsap-utils`, `emilkowalski-motion`, `emil-design-eng`, `review-animations`, `chat-motion-overlay`, `vfx-text-cursor`, `video-hyperframes` |
| **Creative direction & taste** (11) | `taste-skill`, `taste-skill-v1`, `gpt-tasteskill`, `impeccable-design-polish`, `brutalist-skill`, `minimalist-skill`, `soft-skill`, `redesign-skill`, `design-brief`, `reference-design-contract`, `web-design-guidelines` |
| **Decks & documents** (11) | `deck-guizang-editorial`, `deck-open-slide-canvas`, `deck-swiss-international`, `ppt-keynote`, `pptx-html-fidelity-audit`, `html-ppt-retro-quarterly-review`, `doc-kami-parchment`, `article-magazine`, `data-report`, `release-notes-one-pager`, `resume-modern` |
| **Social & brand assets** (10) | `brandkit`, `brand-extract`, `card-twitter`, `card-xiaohongshu`, `social-x-post-card`, `social-reddit-card`, `social-spotify-card`, `ecommerce-image-workflow`, `imagegen-frontend-web`, `imagegen-frontend-mobile` |
| **Frames & visual set-pieces** (9) | `frame-data-chart-nyt`, `frame-flowchart-sticky`, `frame-glitch-title`, `frame-light-leak-cinema`, `frame-liquid-bg-hero`, `frame-logo-outro`, `frame-macos-notification`, `mockup-device-3d`, `poster-hero` |
| **Editorial & video templates** (8) | `8-bit-orbit-video-template`, `after-hours-editorial-template`, `editorial-burgundy-principles-template`, `field-notes-editorial-template`, `digits-fintech-swiss-template`, `swiss-creative-mode-template`, `swiss-user-research-video-template`, `weread-year-in-review-video-template` |
| **Front-end & UI** (7) | `frontend-design`, `image-to-code-skill`, `web-clone`, `stitch-skill`, `export-download-debugging`, `faq-page`, `login-flow` |
| **Utilities & workflow** (7) | `agent-browser`, `library-curator`, `output-skill`, `writing-guidelines`, `pr-feedback-quality-gate`, `research-decision-room`, `hatch-pet` |

## Things to know before installing

- **No name collisions any more.** The three that used to clash — `ui-ux-pro-max`, `slides`, `brainstorming` — were all pointer entries and are gone. The real versions live in `ui-ux-pro-max/` and `superpowers/`.
- **API keys.** The paid-service pointers (fal.ai, Venice, Replicate, Sora, Imagen, MiniMax, Pixelbin) were all in the removed set, so nothing here needs credentials except where a skill's own `SKILL.md` says so.
- **`web-clone/`** is adapted from https://github.com/Jane-xiaoer/claude-skill-web-clone — credit to that author.
- Some skills use `od.mode` frontmatter, which is an OpenDesign-specific field. It's harmless elsewhere, but those skills may assume the OpenDesign daemon is present.
