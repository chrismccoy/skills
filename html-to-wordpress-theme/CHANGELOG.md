# Changelog

All notable changes to the `html-to-wordpress-theme` plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.0] — 2026-04-29

### Added

- Initial release of the `html-to-wordpress-theme` skill
- `/html-to-wordpress-theme [theme name]` slash command — explicit invocation that kicks off the workflow with optional theme-name argument
- **Source HTML → WordPress Template Mapping convention** — explicit filename-to-template mapping presented at the Initialization Gate. Users can drive specific WordPress templates with their own designs by naming source files predictably (`archive.html` → `archive.php`, `category.html` → `category.php`, `404.html` → `404.php`, etc.) instead of letting Claude derive everything from `index.html`. Documented override hierarchy (`category.html` beats `archive.html` for category archive) and unrecognized names automatically become custom page templates under `template-pages/`.
- **Optional WordPress features prompt** at the Initialization Gate — explicit opt-in list covering Customizer settings (with sanitization), transient caching with invalidation hooks, reading time, related posts, Schema.org JSON-LD, social share buttons (no third-party JS), author bio box, last-updated date with diff threshold, AJAX comments/pagination with non-JS fallback, custom shortcodes, and plugin integrations (ACF / Yoast / WPForms / WP Rocket / etc.). Each opted-in feature is wired through ⑨ Decision Log, ⑪ File Manifest, Phase 2 implementation patterns, and the Phase 3 audit (rows 80–90). Features not explicitly opted in are omitted entirely — no unrequested helpers added.
- Phased conversion workflow with mandatory user approval gates between phases:
  - **Initialization Gate** — confirm theme name and defaults
  - **Phase 1A — Critical Analysis** — HTML validation, source-quality grading, structured analysis (template mapping, navigation, content mapping, design tokens, decision log, ambiguities, file manifest)
  - **Phase 1B — Extended Analysis** — sidebar/widget regions, interactive behavior, image handling, comments specification, theme.json recommendation
  - **Phase 2 — Implementation** — chunked file generation with per-chunk approval
  - **Phase 3 — Self-Audit** — 79-item evidence-cited checklist
- Always-active rules covering escaping, sanitization, internationalization, PHP coding standards, asset pipeline, accessibility (WCAG 2.1 AA), error recovery, pattern abstraction, child-theme compatibility, and source HTML JavaScript handling
- Tailwind CSS v3 CLI build pipeline — no CDN, no PostCSS, no Webpack
- Child-theme-friendly architecture: overridable template tags wrapped in `function_exists()`, named hook callbacks, parent-theme path resolution
- Auto-generated `README.md` for produced themes including setup commands, testing checklist, and child-theme override docs
- Helper-vs-template escape boundary rule (`{prefix}_get_*()` returns raw, `{prefix}_*()` echoes pre-escaped)
- Audit `see #N` evidence-sharing shortcut
- `comment_form()` field-ordering guidance (cookies opt-in must follow `url`)
