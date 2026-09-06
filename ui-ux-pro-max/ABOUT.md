# UI UX Pro Max

**Source repository:** https://github.com/nextlevelbuilder/ui-ux-pro-max-skill
**Website:** https://uupm.cc
**Original author:** Next Level Builder (`nextlevelbuilder`)
**License:** MIT (Copyright (c) 2024 Next Level Builder)
**Version at time of download:** 2.13.0
**Downloaded as:** `ui-ux-pro-max-skill-main.zip` (deleted after extraction — re-download from the repo above)

All credit goes to the original author. This folder is the upstream `.claude/skills/` directory, copied so the skills can be installed directly.

## What it is

Design intelligence for AI coding assistants — a searchable **local** database plus reasoning rules for building professional UI/UX. Ships 79 searchable UI styles (50 active), 192 product palettes, 74 font pairings, 119 UX guidelines, 105 icons, 17 GSAP presets, 25 chart types, and 22 stack guides (React, Next.js, Vue, Nuxt, Svelte, Astro, SwiftUI, React Native, Flutter, Tailwind, shadcn/ui, Jetpack Compose, Angular, Laravel, JavaFX, WPF, WinUI, Avalonia, Uno, UWP, Three.js).

## Skills in this folder (7)

| Skill | What it does |
|---|---|
| `ui-ux-pro-max` | The main skill — design intelligence for web/mobile/desktop, with the searchable style/palette/typography/chart/stack database (~3.6 MB) |
| `ui-styling` | Building interfaces with shadcn/ui (Radix + Tailwind), Tailwind styling, themes, dark mode, accessible components (~5.8 MB) |
| `design` | Umbrella design skill: logos (55 styles), corporate identity programs, mockups, HTML presentations, banners, icons, social photos |
| `design-system` | Three-layer token architecture (primitive → semantic → component), CSS variables, spacing/type scales, component specs, slide generation |
| `brand` | Brand voice, visual identity, messaging frameworks, asset management, consistency checks |
| `banner-design` | Banners for social, ads, web heroes and print across 13 styles and all major platform sizes |
| `slides` | Strategic HTML presentations with Chart.js, design tokens and copywriting formulas |

## Notes

- These are the largest skills here (~10 MB total) because of the bundled CSV/JSON databases and reference material.
- Some skills include Python and Node scripts (`scripts/`) that they call locally — kept as-is.
- The upstream repo also ships a CLI (`ui-ux-pro-max-cli` on npm), a website, galleries and screenshots — not copied.
- Some skills (e.g. logo/icon generation) can optionally call external AI image APIs (Gemini, Atlas Cloud, MuAPI). Those paths need your own API keys and only run if you ask for them.
