# chrismccoy-skills

A Claude Code plugin marketplace by Chris McCoy.

## Available plugins

- [`html-to-wordpress-theme`](#html-to-wordpress-theme) — Converts static HTML/Tailwind files into installable WordPress themes
- [`html-design-styles`](#html-design-styles) — 53 named design styles with full color palettes, typography, and component patterns
- [`code-application-blueprint`](#code-application-blueprint) — Complete 10-section technical project specification ready for implementation
- [`wordpress-plugin`](#wordpress-plugin) — Production-ready, enterprise-grade WordPress plugin from scratch with seven-question multiple-choice intake — full directory tree, security guards, i18n, readme.txt, and uninstall.php

## Quick start

In any Claude Code session, run:

```
/plugin marketplace add github:chrismccoy/skills
/plugin install html-to-wordpress-theme@chrismccoy-skills
/plugin install html-design-styles@chrismccoy-skills
/plugin install code-application-blueprint@chrismccoy-skills
/plugin install wordpress-plugin@chrismccoy-skills
```

The first command adds the marketplace; the rest install each plugin. Skip whichever plugins you don't need — each is independent. Full descriptions of what each one does are below.

---

### `html-to-wordpress-theme`

Converts static HTML files into production-quality, installable WordPress themes.

```
/plugin install html-to-wordpress-theme@chrismccoy-skills
```

Ever had a beautiful static HTML design built with Tailwind CSS and wished you could just drop it into WordPress? That's exactly what this plugin solves.

The `html-to-wordpress-theme` skill takes your static Tailwind CSS HTML files and converts them into a fully installable, WordPress-compliant theme. No more manually rewriting markup into PHP templates or guessing how WordPress expects things to be structured — the skill handles it all for you through a guided, step-by-step workflow.

What makes it different from a quick copy-paste job? It actually cares about quality. Your converted theme comes out with proper accessibility baked in, secure code that follows WordPress coding standards, and a real Tailwind CSS build pipeline — no CDN links or shortcuts. There's even a 79-point checklist that runs before anything is delivered to make sure nothing slipped through the cracks.

Whether you're a designer who wants to bring a prototype to life in WordPress or a developer looking to speed up your theme-building process, this tool meets you where you are. It asks for your approval at every major step, so you're always in control — no surprises, no guesswork.

#### 📋 Technical Overview

A production-grade AI instruction specification that converts static Tailwind CSS HTML files into fully installable, WordPress Theme Review Team-compliant themes.

Built around a phased workflow with mandatory approval gates, it enforces WordPress PHP coding standards, WCAG 2.1 AA accessibility, Tailwind CSS v3 CLI build pipelines, comprehensive escaping and security rules, and a 79-point self-audit with cited evidence requirements.

Designed to eliminate silent assumptions, prevent runaway generation, and handle real-world edge cases like poor source HTML quality, context window limits, and multi-session continuity.

#### ✨ Features

- 🏗️ Phased workflow with mandatory approval gates — no code ships without user sign-off
- 🔒 Exhaustive escaping and sanitization rules for every output context
- ♿ WCAG 2.1 AA accessibility baked into every phase and template
- 🎨 Tailwind CSS v3 CLI build pipeline — zero CDN references, zero frameworks
- 🔍 79-point self-audit table requiring cited file-and-line evidence for every check
- 🚦 Graduated failure modes — abort, degraded, or proceed based on source quality
- 🌍 Full internationalization with enforced translator comments and text domains
- 🧩 Smart template abstraction rules for repeated markup patterns
- 👶 Child theme compatibility with overridable functions and removable hooks
- 📦 Automatic chunk planning with size estimation to prevent truncation
- 🔄 Session continuity protocol for multi-conversation conversions
- 📋 Pre-output self-check silently validates every file before delivery
- ⚖️ Decision tiebreaker hierarchy when multiple valid approaches exist
- 🛡️ Nonce enforcement and input sanitization for all custom forms
- 📱 Mobile-first responsive design with keyboard and touch target requirements
- 🏷️ Strict naming conventions derived from a single confirmed theme name
- 📝 Auto-generated README with setup instructions, testing checklist, and documentation
- ⚡ Image performance rules — lazy loading, fetch priority, and registered custom sizes
- 🧪 Testing checklist covering core functionality, accessibility, and build system
- 📐 Content width single source of truth synced across PHP, JSON, and Tailwind config

#### 🔄 How it works

Hand it an `index.html` (and optionally a `single.html`, plus any other page mockups) and it walks you through a four-phase conversion:

1. **Initialization** — confirm theme name and defaults
2. **Phase 1 — Analysis** (1A critical, 1B extended) — HTML validation, source-quality grading, design-token extraction, file manifest, decision log
3. **Phase 2 — Implementation** — generates every theme file in user-approved chunks
4. **Phase 3 — Self-Audit** — a 79-item checklist with cited file-and-line evidence before delivery

You approve each phase before the next one starts, so nothing runs away from you.

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/html-to-wordpress-theme              ← starts the workflow
/html-to-wordpress-theme Brewline     ← pre-fills the theme name
```

**Natural language** (auto-triggers):

> *"I have an index.html and a single.html in my Downloads folder — convert them into a WordPress theme called 'Brewline'."*

Either way, confirm the theme name and defaults at the initialization gate, then approve each phase as it completes. Theme files land in a folder named after your theme slug.

The full skill instructions live at [`html-to-wordpress-theme/skills/html-to-wordpress-theme/SKILL.md`](html-to-wordpress-theme/skills/html-to-wordpress-theme/SKILL.md), with deep references in the adjacent [`references/`](html-to-wordpress-theme/skills/html-to-wordpress-theme/references/) folder.

#### 🤖 AI Analysis Verdict

> The skill's source instruction set was independently analyzed by Claude Opus 4.6. Below are the evaluation results.

| Aspect | Description | Rating | Score |
|--------|-------------|--------|-------|
| Completeness | Covers every edge case from abort criteria to degraded mode, with zero gaps in the conversion workflow | ★★★★★ | 10/10 |
| Structure | Phase gates, numbered sections, cross-references, and a document map make navigation effortless even at 2000+ lines | ★★★★★ | 10/10 |
| Clarity | Every rule includes ✅/❌ examples, anti-patterns, and decision trees — leaves no room for misinterpretation | ★★★★★ | 10/10 |
| Maintainability | Versioned with changelog, modular sections, and a priority hierarchy that makes updates safe and predictable | ★★★★★ | 10/10 |
| Practical Effectiveness | Evidence-based self-audit, context window management, and session continuity ensure reliable output across real-world usage | ★★★★★ | 10/10 |
| Error Handling | Graduated failure modes (abort → degraded → proceed) with explicit user checkpoints prevent silent failures | ★★★★★ | 10/10 |
| Security Coverage | Exhaustive escaping/sanitization tables, nonce enforcement, and a pre-output self-check catch vulnerabilities before they ship | ★★★★★ | 10/10 |
| Accessibility | WCAG 2.1 AA baked into every phase — contrast ratios, keyboard nav, ARIA, skip links, and reduced motion are non-negotiable | ★★★★★ | 10/10 |
| **Overall** | **A production-grade AI engineering specification that rivals internal runbooks at mature development organizations** | **★★★★★** | **10/10** |

---

### `html-design-styles`

A curated catalog of 53 named design styles for frontend interfaces.

```
/plugin install html-design-styles@chrismccoy-skills
```

Tired of AI-generated frontends that all look like the same generic SaaS landing page? This skill ships specs for 53 distinct design aesthetics — each one a complete, opinionated system with its own color palette, typography stack, component patterns, and signature visual mechanics. Pick a style by name and the output actually *looks* like that style.

When the skill triggers, it knows exactly how to implement any style — fonts, colors, shadows, layout patterns, components, animations, and more — producing production-ready HTML in a single output.

#### 🎨 Available styles

##### Minimal & Clean
- 🍎 **Bento Style** — Apple/macOS-inspired bento grid, clean and minimal
- 🌿 **Soft Modern Style** — White bg, blurred orb accents, rounded, friendly and accessible
- ❄️ **Scandinavian Style** — Cold whites, extreme negative space, hygge minimalism, quiet luxury
- 🏢 **Corporate Style** — Conservative trust blues, structured grid, buttoned-up B2B professionalism
- 📐 **Swiss Style** — Helvetica-inspired, rigid typographic grid, black/red only, zero decoration

##### Dark & Atmospheric
- 🌌 **Dark Cosmic Style** — Dark slate, glowing indigo/cyan, radial dot grid, glassmorphism
- 🎬 **Dark Action Style** — Dark gradient bg, yellow/gold accents, Oswald font, cinematic energy
- 🚀 **Dark SaaS Style** — Slate-950, sky blue accent, stagger animations, clean SaaS
- 🎭 **Dark Cinema Style** — Near-black, red glow, Bebas Neue, noise overlay, floating labels
- 💾 **Dark Mono Style** — Dark zinc surfaces, cyan + pink accents, monospace, scanline texture
- 🌠 **Dark Neon Style** — Black background, multiple vivid neon glow colors, bleed and bloom effects
- 🌌 **Vaporwave Style** — Purple/teal gradients, retro grid floors, synthwave glow and glitch effects

##### Brutalist & Bold
- ⬛ **Pure Brutalist Style** — Monochrome black/white, hard shadows, monospace, no color
- ⚡ **Neobrutalist Style** — Hard black shadows with vivid neon color accents
- ☢️ **Acid Brutalist Style** — Pure black, acid yellow + red, Anton/Bebas fonts, noise grain
- 🔧 **Utility Terminal Style** — White bg, strict 1px borders, monospace, no rounding, grid texture
- 🏗️ **Monolith Style** — White bg, dark navy shadows, thick top border accent, monospace brutalism

##### Retro & Nostalgic
- 📺 **Retro Terminal Style** — Green-on-black CRT monitor aesthetic with phosphor glow effects
- 🕹️ **Pixel Style** — 8-bit pixelated fonts, game UI, sprite aesthetic, retro game feel
- 🖥️ **Y2K Style** — Windows 95 beveled gray UI, system fonts, chunky pixel buttons, early internet
- 🌊 **Groovy Style** — Warm oranges/browns, 70s swirls, rounded retro lettering, psychedelic curves
- 🎨 **Memphis Style** — 80s/90s geometric shapes, bright pastels, squiggles and confetti
- 🌴 **Tropical Style** — Coral, turquoise, warm vacation energy, Miami/resort vibes

##### Artistic & Expressive
- 🎪 **Pop Art Style** — Cyan/pink/yellow on loud background, floating bordered container
- 🍭 **Kawaii Style** — Super cute pastel, bubble rounded, character illustration accents
- 💥 **Manga Style** — Speed lines, bold ink outlines, dramatic panel layouts, high contrast
- 🌈 **Psychedelic Style** — Acid swirls, melting text, rainbow overflow, mind-bending distortion
- 🗞️ **Zine Style** — Photocopied DIY aesthetic, cut-and-paste collage, raw indie energy
- 🔆 **Aurora Style** — Flowing multi-color gradient backgrounds, silk light effect, soft and dreamy

##### Elegant & Luxury
- 👑 **Luxury Style** — Cream/off-white, serif display font, gold accents, generous whitespace
- 🌸 **Art Deco Style** — Geometric gold ornaments, symmetry, 1920s glamour and opulence
- 🌺 **Cottagecore Style** — Floral patterns, watercolor washes, storybook softness and whimsy
- 🌙 **Gothic Style** — Dark greens/blacks, ornate serif, candle-wax drips, moody atmosphere
- ✒️ **Japanese Style** — Wabi-sabi imperfection, ink brush strokes, kanji-inspired negative space

##### Technical & Structured
- 🔷 **Blueprint Style** — Deep blueprint blue, white grid lines, Courier Prime, technical drawing aesthetic
- 🔴 **Dot Grid Style** — Gray dotted background, Archivo Black + Space Mono, hot pink accent, hard shadows
- 🟣 **Pink Neo Style** — Hot pink dotted background, Archivo Black + Space Mono, pink/yellow/blue palette
- 📊 **Dashboard Style** — Chart-forward, dense metrics, sidebar navigation, admin/analytics feel
- 🤖 **Sci-Fi HUD Style** — Heads-up display, corner brackets, data readouts, radar and targeting UI
- ⚠️ **Cyberpunk Style** — Yellow/black warning stripes, HUD overlays, neon on dark, danger aesthetics

##### Specialty & Immersive
- 💎 **Glassmorphism Style** — Frosted glass cards on gradient mesh backgrounds, soft blurs and translucency
- 🏛️ **Neumorphism Style** — Soft same-color shadows creating pushed/extruded soft UI on light gray
- 📦 **Clay Style** — Clay morphism, chunky rounded cards with physical depth
- 🖨️ **Newspaper Style** — Black ink on newsprint, serif fonts, editorial column layouts
- 📖 **Longform Style** — Full-bleed hero images, pull quotes, drop caps, rich magazine editorial flow
- 🎵 **Skeuomorphic Style** — Realistic material textures, depth and shadows mimicking physical objects
- 🌸 **Organic Style** — Earthy tones, rounded organic shapes, warm and natural hand-crafted feel
- ✍️ **Handwritten Style** — Hand-drawn borders, pencil textures, imperfect sketch-like lines

##### Energy & Motion
- 🏆 **Athletic Style** — Diagonal cuts, bold color blocks, high-impact sport energy
- 🌍 **Grunge Style** — Worn textures, splatter marks, distressed rough torn edges
- 🔮 **Isometric Style** — 3D isometric grid illustrations, flat-color depth and layered objects
- 🎭 **Maximalist Style** — Everything layered, dense pattern-on-pattern, opulent visual chaos
- 🔣 **Enterprise Editorial Style** — White/dark alternating sections, indigo, large rounded app cards

#### 📦 What each style spec includes

Every style definition covers:

- 🔤 **Typography** — Font families, weights, sizes, letter-spacing
- 🎨 **Color palette** — All CSS custom properties with exact values
- 🪞 **Shadow system** — Named shadow levels used across components
- 🃏 **Card variants** — Background, border, hover states
- 🔘 **Button variants** — Primary, secondary, ghost, active/pressed states
- 📐 **Layout patterns** — Grid structures, hero layouts, section flows
- 🧩 **Components** — Pills, badges, stat cards, nav, marquee, footer
- ✨ **Animations** — Transitions, keyframes, scroll effects where applicable
- ⚙️ **Implementation notes** — CDN links, font imports, special CSS tricks

#### 💻 Output format

The skill generates a **single self-contained HTML file** with:

- Inline CSS (no external stylesheet needed)
- Tailwind CSS via CDN
- Google Fonts via CDN
- Font Awesome 6 via CDN (when icons are needed)
- Vanilla JS for any interactions

No build step. Open the file in a browser and it works.

#### 🔄 How it works

1. **Identify the style** — match the user's request against the 53-item catalog (or ask them to pick if ambiguous)
2. **Get project context** — full page, single component, restyling existing markup, what content goes in
3. **Load references** — `common.md` once per session for cross-cutting patterns, then `styles/<slug>.md` for the chosen style's complete spec
4. **Apply faithfully** — use the exact color values, typography stack, shadow recipes, and component patterns from the spec, with no "similar" substitutions

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/html-design-styles                              ← asks you to pick a style
/html-design-styles brutalist                    ← starts straight into Brutalist
/html-design-styles brutalist landing page for my SaaS
                                                 ← pre-fills both style + project
```

**Natural language** (auto-triggers on style names) — describe what you want:

**From scratch — describe your product inline:**

```
Build a landing page using bento style.

Product: Pinpoint
A time-tracking app for freelancers. Automatically tracks time across apps
and projects, generates invoices, and syncs with Stripe.

Features:
- Automatic time tracking across Mac apps
- Project and client tagging
- One-click invoice generation
- Stripe integration for payments
- Weekly summary reports

CTA: "Start Free Trial"
```

**From a feature list in your own README — point Claude at it and it pulls product name, features, and copy automatically:**

```
Read README.md. Build a landing page using neobrutalist style based on
the features and descriptions in README.md. Keep copy tight — headline,
subheadline, feature grid, and a single CTA.
```

**Restyle an existing landing page — pass in your HTML and Claude rebuilds it in a new style while preserving content and structure:**

```
Read landingpage.html. Rebuild the landing page using dark cinema style.
Keep all existing sections, copy, and CTAs — only change the visual design.
```

That's it. The skill handles the rest — typography, color palette, layout grid, components, and interactions — all consistent with the named style spec.

The full skill instructions live at [`html-design-styles/skills/html-design-styles/SKILL.md`](html-design-styles/skills/html-design-styles/SKILL.md), the cross-cutting patterns at [`references/common.md`](html-design-styles/skills/html-design-styles/references/common.md), and each style's complete spec under [`references/styles/`](html-design-styles/skills/html-design-styles/references/styles/).

---

### `code-application-blueprint`

Generates a complete technical project specification ready for direct implementation.

```
/plugin install code-application-blueprint@chrismccoy-skills
```

Starting a new project without a clear spec leads to scope creep, architectural regrets, and implementation gaps that only surface mid-build. The `code-application-blueprint` skill acts as a principal architect — it takes five inputs and produces a 10-section specification that serves as the single source of truth for the entire project: every component, every file contract, every data schema, every risk, and a full setup guide.

The output is precise enough that a developer (or an AI coding assistant) can open it and start building immediately without follow-up questions. Scale-aware: an MVP spec stays lean and focused, while an Enterprise spec covers observability, security hardening, and multi-environment strategy.

#### ✨ Features

- 📋 10-section specification: Project Overview, Scope Contract, Architecture Overview, Dependency Map, Directory Structure, File Contracts, Data Models, Risk and Failure Map, Testing Strategy, Setup and Run
- 🔗 Enforced cross-section consistency — every file in the directory structure gets a file contract, every architecture decision traces to specific files
- ⚖️ Scale-aware depth — MVP stays lean, Enterprise covers observability and security
- 🚫 Zero TBD, zero placeholders, zero unresolved items in the output
- ⚠️ Conflict detection — flags contradictions between inputs and proposes resolutions before generating
- 🛠️ Stack-aware — adapts patterns to the chosen technology stack; only suggests alternatives if the stack has a blocking gap

#### 🔄 How it works

1. **Initialization Gate** — five required questions via `AskUserQuestion`:
   - Project description (free text)
   - Tech stack (multiple choice: Node/Express, Next.js, FastAPI, Django, Go, Rails, Laravel, React+Node, Vue+Node, custom)
   - Interfaces (multiple choice: REST, GraphQL, Web UI, CLI, WebSocket, gRPC, combinations, custom)
   - Scale (multiple choice: MVP, Startup, Enterprise)
   - Constraints (free text — budget, timeline, regulatory, performance targets, or "none")
2. **Conflict check** — if inputs contradict each other, flags it and resolves before proceeding
3. **Generation** — all 10 sections in order, fully consistent, no gaps
4. **Delivery** — single markdown document

#### 🚀 How to use it

```
/code-application-blueprint                              ← walks through all five questions
/code-application-blueprint "A time-tracking SaaS app"  ← pre-fills the project description
```

Or natural language: *"create a project blueprint for a REST API"*, *"generate a technical spec for my app"*, *"architect a new project"*.

---

### `wordpress-plugin`

Generates complete, enterprise-grade WordPress plugins from scratch — the kind you could submit to the WordPress.org repository today.

```
/plugin install wordpress-plugin@chrismccoy-skills
```

Most AI-generated WordPress plugins fail the same way: missing nonces, raw `$_POST` values, string-interpolated SQL, no text domain, no `uninstall.php`, and a `Plugin Name` header that's the only metadata it bothered to fill in. The `wordpress-plugin` skill takes a different approach. Seven structured intake answers in — full directory tree out, with WordPress Coding Standards compliance, complete security guardrails, internationalization, conditional asset enqueueing, custom tables via `dbDelta()` with proper indexes, and a real uninstall script that removes every artefact the plugin creates.

Five of the seven intake questions are **multiple choice** via `AskUserQuestion` — pick the WordPress mechanisms the plugin uses, the target audience, the admin UI components, the frontend display surfaces, and the third-party integrations. Two are free-text — the plugin name and a 2–4 sentence description of what the plugin actually does. No ambiguous answers, no follow-up clarification rounds.

#### ✨ Features

- 📋 Seven-question intake — five multi-choice via `AskUserQuestion` plus two free-text — every variable in the about-me section is a picker, not a fill-in-the-blank
- 🏗️ Modular OOP structure — singleton main plugin class wires Admin, Frontend, Database, AJAX, REST, Cron, CLI, Roles, CPT, Meta-box, List-table, Dashboard-widget, Notices, and Integration components
- 🔒 Security baked in — `defined( 'ABSPATH' ) || exit;` on every file, nonces on every mutation, capability checks before every privileged action, sanitization on every input, escaping on every output, `$wpdb->prepare()` on every query
- 🧰 WordPress mechanisms covered: Custom Post Types & Taxonomies, Settings API, Gutenberg blocks, shortcodes, REST endpoints, WP-CLI commands, cron, custom tables, roles & capabilities, email notifications, frontend forms, dashboard widgets, import/export, activity logging, custom user meta
- 🎯 Audience-aware code generation — pick "Multisite network administrators" and the activator/deactivator/uninstaller all loop `get_sites()`; pick "Developers" and you get a `docs/` folder with documented hooks
- 🧩 Frontend surfaces — shortcodes, Gutenberg blocks, classic widgets, template tags, `the_content` injection with opt-out, REST-driven SPA, custom page templates
- 🔌 Integration scaffolds — WooCommerce, BuddyPress/bbPress, ACF, Elementor, external REST APIs, Stripe/PayPal, Mailchimp/ConvertKit/SendGrid, Google Analytics, OAuth providers, incoming and outgoing webhooks (with HMAC verification and Action Scheduler fallback)
- 🌍 Internationalization — every user-facing string wrapped in i18n functions with the correct text domain, plus a populated `.pot` file in `languages/`
- 📚 Complete documentation — `readme.txt` in WordPress.org format (Contributors, Tags, Requires at least, Tested up to, Stable tag, License, Description, Installation, FAQ, Screenshots, Changelog, Upgrade Notice), `readme.md` GitHub-friendly mirror, PHPDoc on every class and public method
- 🗑️ Complete uninstall — drops every custom table, deletes every option/transient/user-meta/post-meta, clears scheduled events, removes registered roles and capabilities, with the proper `WP_UNINSTALL_PLUGIN` guard
- ⚡ Conditional asset enqueueing — `get_current_screen()` checks so admin assets never leak onto the frontend and public assets don't load on every admin page
- 🗃️ Custom-table best practices — `$wpdb->get_charset_collate()`, `dbDelta()`, indexes on every queried column, schema version stored in an option for migrations
- 🚫 Zero placeholders — no `TODO`, no `TBD`, no `{name}`, no `Coming soon` in any generated file

#### 🔄 How it works

1. **Seven-question intake** — five multi-choice via `AskUserQuestion`, two free-text:
   - Plugin name (free text)
   - Functionality categories (multi-select: CPTs, Settings page, Blocks, Shortcodes, REST, WP-CLI, Cron, Custom Tables, Roles, Email, Forms, Dashboard Widget, Import/Export, Logging, User Meta)
   - Specific feature detail (free text — 2–4 sentences)
   - Target users (single-select: Site admins / Editors / Frontend visitors / Developers / Multisite admins / Mixed)
   - Admin interface components (multi-select: Top-level menu / Settings submenu / Tools submenu / Meta boxes / List tables / Dashboard widget / Admin notices / Help tabs / None)
   - Frontend display surfaces (multi-select: Shortcodes / Blocks / Widgets / Template tags / `the_content` filter / REST SPA / Custom page templates / None)
   - Third-party integrations (multi-select: WooCommerce / BuddyPress / ACF / Elementor / External REST API / Stripe or PayPal / Mailchimp etc / GA / OAuth / Incoming webhooks / Outgoing webhooks / None)
2. **Inference** — slug, text domain, constant prefix, PHP namespace, main file name, and singleton class name are all derived from the plugin name. "Acme Bookings" → slug `acme-bookings`, text domain `acme-bookings`, constants `ACME_BOOKINGS_*`, namespace `AcmeBookings`.
3. **Conditional generation** — each component file is generated only if the corresponding multi-choice option was picked. No empty `blocks/` folder when Gutenberg blocks weren't requested.
4. **Quality checklist** — runs before delivery: ABSPATH guard on every PHP file, nonce on every mutation, capability check before every privileged action, sanitizer on every input, escape on every output, prepared statement on every query, i18n on every string, full `readme.txt`, complete `uninstall.php`, zero placeholders.
5. **Delivery** — writes the full tree to `./{plugin-slug}/` (or `./{plugin-slug}-new/` if the first exists).

#### 🚀 How to use it

```
/wordpress-plugin                            ← walks through all seven questions
/wordpress-plugin "Acme Bookings"            ← pre-fills the plugin name
```

Or natural language: *"build me a WordPress plugin for time-slot bookings"*, *"scaffold a WP plugin with a settings page and a REST endpoint"*, *"create a custom post type plugin for testimonials"*, *"I need a Gutenberg block plugin for newsletter signups"*, *"make me a WooCommerce extension that adds gift wrapping"*.

The full skill instructions live at [`wordpress-plugin/skills/wordpress-plugin/SKILL.md`](wordpress-plugin/skills/wordpress-plugin/SKILL.md).

---

## Repo layout

```
.
├── .claude-plugin/
│   └── marketplace.json                       ← marketplace manifest
├── html-to-wordpress-theme/                   ← plugin
│   ├── commands/
│   │   └── html-to-wordpress-theme.md         ← /html-to-wordpress-theme slash command
│   └── skills/
│       └── html-to-wordpress-theme/
│           ├── SKILL.md
│           └── references/
│               ├── rules.md
│               ├── phase-1-analysis.md
│               ├── phase-2-implementation.md
│               └── phase-3-audit.md           ← 79-item audit
├── html-design-styles/                        ← plugin
│   ├── commands/
│   │   └── html-design-styles.md              ← /html-design-styles slash command
│   └── skills/
│       └── html-design-styles/
│           ├── SKILL.md
│           └── references/
│               ├── common.md
│               └── styles/                    ← one file per style (53 total)
├── code-application-blueprint/                ← plugin
│   ├── commands/
│   │   └── code-application-blueprint.md      ← /code-application-blueprint slash command
│   └── skills/
│       └── code-application-blueprint/
│           ├── SKILL.md
│           └── references/
│               └── blueprint-spec.md          ← 10-section output structure and rules
└── wordpress-plugin/                          ← plugin
    ├── commands/
    │   └── wordpress-plugin.md                ← /wordpress-plugin slash command
    └── skills/
        └── wordpress-plugin/
            └── SKILL.md                       ← seven-question intake + full WP plugin tree generator
```

