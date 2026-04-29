# Changelog

All notable changes to the `html-design-styles` plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.0] — 2026-04-29

### Added

- Initial release of the `html-design-styles` skill
- `/html-design-styles [style] [optional project description]` slash command — explicit invocation that pre-fills the chosen style and optional project context, skipping the picker
- **`AskUserQuestion` picker preference** — when the input is ambiguous (no style, category word, or generic term matching multiple catalog entries), the skill instructs Claude to prefer the `AskUserQuestion` tool over plain-text questions so users get keyboard-navigable multi-choice selection with one-line per option, falling back to plain text only when the tool is unavailable in the runtime
- Catalog of 53 fully-specified design styles, each in its own reference file under `references/styles/`:
  - **Minimalist:** Swiss, Scandinavian, Japanese, Soft Modern
  - **Brutalist:** Pure Brutalist, Neobrutalist, Acid Brutalist, Monolith
  - **Retro:** Y2K, Vaporwave, Memphis, Pixel, Retro Terminal, Groovy
  - **Dark / atmospheric:** Dark Cinema, Dark Cosmic, Dark Action, Dark Neon, Dark Mono, Dark SaaS, Cyberpunk, Sci-Fi HUD
  - **Warm / organic:** Cottagecore, Organic, Tropical, Aurora
  - **Editorial:** Newspaper, Longform, Enterprise Editorial, Luxury, Corporate
  - **Playful:** Kawaii, Manga, Pop Art, Maximalist, Memphis
  - **Tech / UI:** Bento, Glassmorphism, Neumorphism, Dashboard, Blueprint, Dot Grid
  - **Other:** Clay, Pink Neo, Skeuomorphic, Utility Terminal, Art Deco, Isometric, Zine, Gothic, Handwritten, Grunge, Athletic, Psychedelic
- Lean `SKILL.md` entrypoint with workflow, initialization gate, and a 53-row style picker table mapping display name → slug → one-line description
- Cross-cutting `references/common.md` for shared patterns (font loading, container/padding conventions, focus rings, marquees, custom scrollbars, accessibility patterns)
- On-demand reference loading: only the chosen style's reference file is read into context, not the whole catalog
- Self-contained style files — no cross-references between styles to follow
