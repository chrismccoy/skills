# My Custom Made Skills

Claude plugin marketplace for all my own custom skills.

29 plugins available. Install any one on its own, or the whole set.

## Available plugins

**WordPress**

- [`wp-builder-pro`](#wp-builder-pro). Builds and implements custom WordPress code - themes, plugins, Gutenberg blocks, WooCommerce, and REST endpoints - with security and performance built in. Best when you're adding to or fixing a site you already have - a new feature, a slow page, a broken block.
- [`wordpress-plugin`](#wordpress-plugin). Builds a complete WordPress plugin from scratch, ready for the WordPress.org repository, with security, translations, and a clean uninstall all handled.
- [`html-to-wordpress-theme`](#html-to-wordpress-theme). Converts static HTML/Tailwind files into installable WordPress themes.
- [`wordpress-architect-review`](#wordpress-architect-review). Reviews a WordPress plugin or theme file by file, then returns ranked findings, a scorecard, and the top fixes to make.
- [`wordpress-consultant`](#wordpress-consultant). A senior WordPress consulting audit covering architecture, performance, security, and scalability, ending with a 0-100 scorecard and summary.
- [`wordpress-formatter`](#wordpress-formatter). Formats a theme's template files to the WordPress coding standard - tabs, spacing, and array style - without changing how any page renders. It installs the tools, runs the fixer, and checks the result.

**Plan and Design**

- [`app-blueprint`](#app-blueprint). Produces a full production app blueprint from your idea - folder layout, data models, API design, dependencies, tests, and CI/CD.
- [`html-design-styles`](#html-design-styles). 53 named design styles with full color palettes, typography, and component patterns.
- [`accessibility-audit`](#accessibility-audit). Checks a page, a folder, or a single component against the accessibility rules, tells you what is broken and why it matters, and can fix it for you. Command only, so it never fires on its own or clashes with another accessibility plugin.

**Refactor, Map and Clean Up**

- [`refactoring-analyst`](#refactoring-analyst). Reviews your codebase and returns a prioritized refactoring plan, with every issue tied to a real file and line and a roadmap to fix them.
- [`codebase-to-mermaid`](#codebase-to-mermaid). Reads a codebase you don't know and draws accurate Mermaid flow, sequence, or class diagrams, with every box tied to a real file and line.
- [`mermaid-to-ascii`](#mermaid-to-ascii). Turns a Mermaid diagram file into clean text-art you can paste into a comment, a README, or a terminal, saved next to the original as a `.txt`.
- [`explain-my-code`](#explain-my-code). Reads a whole repo and writes one self-contained onboarding document - architecture, folder map, app flow, design patterns, risks - in 13 fixed sections with Mermaid diagrams, so anyone new to the project can get up to speed just by reading it.
- [`docblock-rewrite`](#docblock-rewrite). Rewrites bulky PHPDoc and JSDoc blocks into short, plain-English one-line comments, backing up the originals first.
- [`unslop`](#unslop). Strips the AI-sounding voice out of comments, docstrings, and names in your code without changing how the code runs. Works across 19+ languages.
- [`changelog-generator`](#changelog-generator). Writes a changelog your users can read from a repo's whole git history by reading the real code changes, not the commit messages, then sorts every change and saves `CHANGELOG.md`.

**Servers and Scripting**

- [`docker-compose-architect`](#docker-compose-architect). Generates a secure, production docker-compose setup for your app - separate networks, persistent volumes, health checks, and secrets kept out of the file.
- [`kubernetes-architect`](#kubernetes-architect). Turns your app details into production-ready Kubernetes manifests, with health checks, resource limits, and security settings already included.
- [`powershell-script-engine`](#powershell-script-engine). Writes clean, production-ready PowerShell scripts with built-in help, logging, error handling, and safe handling of credentials and destructive actions.
- [`jq`](#jq). Builds copy-paste-ready jq one-liners to filter, reshape, and aggregate JSON from APIs and CLI tools, inspecting the JSON structure first and explaining each filter stage.

**Domain Names**

- [`naming-strategist`](#naming-strategist). Brainstorms 10 brandable, easy-to-say domain names for your SaaS, with a shortlist of the best three and a checklist to verify them.

**Creative**

- [`vgademo`](#vgademo). Generates a retro 1990s-style assembly graphics demo (MS-DOS, boot sector, or BIOS) after a few multiple-choice questions.

**Data**

- [`excel-formula-troubleshooter`](#excel-formula-troubleshooter). Fixes broken Excel or Google Sheets formulas - names the real cause, returns a corrected formula, and explains it in plain English.

**Writing and language**

- [`tech-blog-article`](#tech-blog-article). Writes a technical blog post in the voice of a senior developer - an opening that grabs the reader, clear code examples, and an honest look at the downsides.
- [`language-tutor`](#language-tutor). Translates and explains a phrase, or corrects and critiques your writing, with grammar notes, pronunciation tips, and better alternatives.
- [`contract-framework`](#contract-framework). Writes a clear, fair freelance or consulting contract from a few plain questions, covering the work, the payment, and who owns the finished result, with anything that depends on where you live flagged for you to check locally.
- [`readme-builder`](#readme-builder). Reads a whole project and writes one beginner friendly `README.md` for it, in a fixed order, in plain everyday English, with hype words and long dashes kept out.
- [`tutorial-builder`](#tutorial-builder). Turns code or a topic into a step-by-step, hands-on tutorial that teaches instead of describing, where every code block runs and shows its output, with a pre-publish checklist and a 1-5 speed score before you get it.

**Session tools**

- [`session-stats`](#session-stats). Turns a Claude Code session into a single dark-theme HTML report - prompts, tool calls, edits, cost, and files changed. Runs fully offline.

## Quick start

In any Claude Code session, run:

```
/plugin marketplace add chrismccoy/skills

# WordPress
/plugin install wp-builder-pro@chrismccoy
/plugin install wordpress-plugin@chrismccoy
/plugin install html-to-wordpress-theme@chrismccoy
/plugin install wordpress-architect-review@chrismccoy
/plugin install wordpress-consultant@chrismccoy
/plugin install wordpress-formatter@chrismccoy

# Plan and Design
/plugin install app-blueprint@chrismccoy
/plugin install html-design-styles@chrismccoy
/plugin install accessibility-audit@chrismccoy

# Refactor, Map and Clean Up
/plugin install refactoring-analyst@chrismccoy
/plugin install codebase-to-mermaid@chrismccoy
/plugin install mermaid-to-ascii@chrismccoy
/plugin install explain-my-code@chrismccoy
/plugin install docblock-rewrite@chrismccoy
/plugin install unslop@chrismccoy

# Servers and Scripting
/plugin install docker-compose-architect@chrismccoy
/plugin install kubernetes-architect@chrismccoy
/plugin install powershell-script-engine@chrismccoy
/plugin install jq@chrismccoy

# Domain Names
/plugin install naming-strategist@chrismccoy

# Creative
/plugin install vgademo@chrismccoy

# Data
/plugin install excel-formula-troubleshooter@chrismccoy

# Writing and language
/plugin install tech-blog-article@chrismccoy
/plugin install language-tutor@chrismccoy
/plugin install contract-framework@chrismccoy
/plugin install readme-builder@chrismccoy
/plugin install tutorial-builder@chrismccoy

# Session tools
/plugin install session-stats@chrismccoy
```

The first command adds the marketplace; the rest install each plugin. Skip whichever plugins you don't need. each is independent. Full descriptions of what each one does are below.

---

## WordPress

### `wp-builder-pro`

Builds and implements custom WordPress code - themes, plugins, Gutenberg blocks, WooCommerce, and REST endpoints - with security and performance built in.

```
/plugin install wp-builder-pro@chrismccoy
```

Where `wordpress-plugin` scaffolds a whole plugin from scratch in one shot, `wp-builder-pro` is the day-to-day builder: add a settings page, register a dynamic block, wire a REST endpoint, extend WooCommerce checkout, or chase down why the shop page is slow. It routes each request to one of five bundled references and works the same six steps every time - analyze, design, implement, validate with `phpcs --standard=WordPress`, optimize, then test and secure - so the output meets WordPress Coding Standards with nonces, sanitization, escaping, capability checks, and prepared statements already in place.

It also answers symptom-first requests. *"My site is slow"*, *"a plugin throws a fatal error"*, *"this block won't render"*, *"fix my WordPress site"* all trigger it, and it asks for the specific symptom before writing a line of code.

#### ✨ Features

- 📋 Intake. four fields via `AskUserQuestion` - build target (single-select), new-vs-existing context, free-text specifics, optional WP/PHP constraints - then routes the target to the right reference
- 🏗️ Full WordPress surface. themes (templates, hierarchy, child themes, FSE), plugins (activation, settings API, hooks, updates), Gutenberg blocks and patterns (static + dynamic), WooCommerce extensions, REST endpoints, ACF fields
- 🔒 Security by default. nonces on every form/AJAX path, sanitization on every input, escaping on every output, capability checks before privileged actions, `$wpdb->prepare()` with `$wpdb->prefix` on every query
- ⚡ Performance built in. transient and object caching, query optimization, conditional asset enqueueing via `wp_enqueue_scripts` hooks
- 🩺 Fixes things that broke. slow site, fatal error, block won't render - asks what's going wrong first, then fixes it
- 📚 Five on-demand references. theme-development, plugin-architecture, gutenberg-blocks, hooks-filters, performance-security - loaded only for the matching build target
- ✅ Quality gates before delivery. WPCS clean, nonce per mutation, sanitize/escape on all I/O, capability checks, prepared statements, hook-based enqueueing, translatable strings, no core edits
- 🚦 Scope-locked. defers complete from-scratch plugin scaffolds to `wordpress-plugin` and refuses code review (that's `wordpress-architect-review` / `wordpress-consultant`)

#### 🔄 How it works

1. **Intake**: four fields via `AskUserQuestion` - build target, project context (new vs existing + path), specifics, optional WP/PHP constraints.
2. **Routing**: the chosen build target maps to one or two bundled references (e.g. WooCommerce → `plugin-architecture.md` + `hooks-filters.md`).
3. **Six-step workflow**: analyze → design → implement → validate (`phpcs --standard=WordPress`) → optimize → test & secure.
4. **Quality gates**: runs before delivery - WPCS clean, nonce per mutation, sanitize/escape on all I/O, capability checks, prepared statements, hook-based enqueueing, i18n, no core edits.
5. **Delivery**: the code plus a short explanation of the WordPress-specific patterns used.

#### 🚀 How to use it

```
/wp-builder-pro ← walks through all four questions
/wp-builder-pro "a dynamic block that lists recent posts" ← seeds the specifics
```

Or natural language: *"build a custom WordPress theme"*, *"add a settings page to my plugin"*, *"create a Gutenberg block"*, *"extend WooCommerce checkout"*, *"add a REST API endpoint"*, *"my WordPress site is slow"*.

The full skill instructions live at [`wp-builder-pro/skills/wp-builder-pro/SKILL.md`](wp-builder-pro/skills/wp-builder-pro/SKILL.md).

---

### `wordpress-plugin`

Generates complete WordPress plugins from scratch. the kind you could submit to the WordPress.org repository today.

```
/plugin install wordpress-plugin@chrismccoy
```

Most AI generated WordPress plugins fail the same way: missing nonces, raw `$_POST` values, string-interpolated SQL, no text domain, no `uninstall.php`, and a `Plugin Name` header that's the only metadata it bothered to fill in. The `wordpress-plugin` skill takes a different approach. Seven structured intake answers in. full directory tree out, with WordPress Coding Standards compliance, complete security guardrails, internationalization, conditional asset enqueueing, custom tables via `dbDelta()` with proper indexes, and a real uninstall script that removes every artefact the plugin creates.

Five of the seven intake questions are **pickers** via `AskUserQuestion`: pick the WordPress mechanisms the plugin uses, the target audience, the admin UI components, the frontend display surfaces, and the third party integrations. Two are free text. the plugin name and a 2-4 sentence description of what the plugin actually does. No ambiguous answers, no follow-up clarification rounds.

#### ✨ Features

- 📋 Intake. five picker prompts via `AskUserQuestion` plus two free text. every variable in the about-me section is a picker, not a fill-in-the-blank
- 🏗️ Modular OOP structure. singleton main plugin class wires Admin, Frontend, Database, AJAX, REST, Cron, CLI, Roles, CPT, Meta-box, List-table, Dashboard-widget, Notices, and Integration components
- 🔒 Security built in. `defined( 'ABSPATH' ) || exit;` on every file, nonces on every mutation, capability checks before every privileged action, sanitization on every input, escaping on every output, `$wpdb->prepare()` on every query
- 🧰 WordPress mechanisms covered: Custom Post Types & Taxonomies, Settings API, Gutenberg blocks, shortcodes, REST endpoints, WP-CLI commands, cron, custom tables, roles & capabilities, email notifications, frontend forms, dashboard widgets, import/export, activity logging, custom user meta
- 🎯 Audience-aware code generation. pick "Multisite network administrators" and the activator/deactivator/uninstaller all loop `get_sites()`; pick "Developers" and you get a `docs/` folder with documented hooks
- 🧩 Frontend surfaces. shortcodes, Gutenberg blocks, classic widgets, template tags, `the_content` injection with opt-out, REST-driven SPA, custom page templates
- 🔌 Integration scaffolds. WooCommerce, BuddyPress/bbPress, ACF, Elementor, external REST APIs, Stripe/PayPal, Mailchimp/ConvertKit/SendGrid, Google Analytics, OAuth providers, incoming and outgoing webhooks (with HMAC verification and Action Scheduler fallback)
- 🌍 Internationalization: every user-facing string wrapped in i18n functions with the correct text domain, plus a populated `.pot` file in `languages/`
- 📚 Complete documentation: `readme.txt` in WordPress.org format (Contributors, Tags, Requires at least, Tested up to, Stable tag, License, Description, Installation, FAQ, Screenshots, Changelog, Upgrade Notice), `readme.md` GitHub-friendly mirror, PHPDoc on every class and public method
- 🗑️ Complete uninstall: drops every custom table, deletes every option/transient/user-meta/post-meta, clears scheduled events, removes registered roles and capabilities, with the proper `WP_UNINSTALL_PLUGIN` guard
- ⚡ Conditional asset enqueueing: `get_current_screen()` checks so admin assets never leak onto the frontend and public assets don't load on every admin page
- 🗃️ Custom-table best practices: `$wpdb->get_charset_collate()`, `dbDelta()`, indexes on every queried column, schema version stored in an option for migrations
- 🚫 Zero placeholders. no `TODO`, no `TBD`, no `{name}`, no `Coming soon` in any generated file

#### 🔄 How it works

1. **Intake**: five picker prompts via `AskUserQuestion`, two free text:
 - Plugin name (free text)
 - Functionality categories (multi-select: CPTs, Settings page, Blocks, Shortcodes, REST, WP-CLI, Cron, Custom Tables, Roles, Email, Forms, Dashboard Widget, Import/Export, Logging, User Meta)
 - Specific feature detail (free text. 2-4 sentences)
 - Target users (single-select: Site admins / Editors / Frontend visitors / Developers / Multisite admins / Mixed)
 - Admin interface components (multi-select: Top-level menu / Settings submenu / Tools submenu / Meta boxes / List tables / Dashboard widget / Admin notices / Help tabs / None)
 - Frontend display surfaces (multi-select: Shortcodes / Blocks / Widgets / Template tags / `the_content` filter / REST SPA / Custom page templates / None)
 - Third party integrations (multi-select: WooCommerce / BuddyPress / ACF / Elementor / External REST API / Stripe or PayPal / Mailchimp etc / GA / OAuth / Incoming webhooks / Outgoing webhooks / None)
2. **Inference**: slug, text domain, constant prefix, PHP namespace, main file name, and singleton class name are all derived from the plugin name. "Acme Bookings" → slug `acme-bookings`, text domain `acme-bookings`, constants `ACME_BOOKINGS_*`, namespace `AcmeBookings`.
3. **Conditional generation**: each component file is generated only if the corresponding picker option was picked. No empty `blocks/` folder when Gutenberg blocks weren't requested.
4. **Quality checklist**: runs before delivery: ABSPATH guard on every PHP file, nonce on every mutation, capability check before every privileged action, sanitizer on every input, escape on every output, prepared statement on every query, i18n on every string, full `readme.txt`, complete `uninstall.php`, zero placeholders.
5. **Delivery**: writes the full tree to `./{plugin-slug}/` (or `./{plugin-slug}-new/` if the first exists).

#### 🚀 How to use it

```
/wordpress-plugin ← walks through all seven questions
/wordpress-plugin "Acme Bookings" ← pre-fills the plugin name
```

Or natural language: *"build me a WordPress plugin for time-slot bookings"*, *"scaffold a WP plugin with a settings page and a REST endpoint"*, *"create a custom post type plugin for testimonials"*, *"I need a Gutenberg block plugin for newsletter signups"*, *"make me a WooCommerce extension that adds gift wrapping"*.

The full skill instructions live at [`wordpress-plugin/skills/wordpress-plugin/SKILL.md`](wordpress-plugin/skills/wordpress-plugin/SKILL.md).

---

### `html-to-wordpress-theme`

Converts static HTML files into installable WordPress themes.

```
/plugin install html-to-wordpress-theme@chrismccoy
```

Ever had a beautiful static HTML design built with Tailwind CSS and wished you could just drop it into WordPress? That's exactly what this plugin solves.

The `html-to-wordpress-theme` skill takes your static Tailwind CSS HTML files and converts them into a fully installable, WordPress-compliant theme. No more manually rewriting markup into PHP templates or guessing how WordPress expects things to be structured. the skill handles it all for you through a guided, step by step workflow.

What makes it different from a quick rewrite? Your converted theme comes out with proper accessibility built in, secure code that follows WordPress coding standards, and a Tailwind CSS build pipeline. no CDN links or shortcuts. There's even a 79-point checklist that runs before anything is delivered to make sure nothing got missed.

Whether you're a designer who wants to ship a prototype in WordPress or a developer looking to speed up your theme development process, this tool fits your workflow. It asks for your approval at every major step, so you're always in control.

#### 📋 Technical Overview

An AI instruction specification that converts static Tailwind CSS HTML files into fully installable, WordPress Theme Review Team-compliant themes.

Built around a phased workflow with mandatory approval gates, it enforces WordPress PHP coding standards, WCAG 2.1 AA accessibility, Tailwind CSS v3 CLI build pipelines, escaping and security rules, and a 79-point self-audit with cited evidence requirements.

Designed to eliminate unstated assumptions, prevent runaway generation, and handle real world edge cases like poor source HTML quality, context window limits, and multi-session continuity.

#### ✨ Features

- 🏗️ Phased workflow with mandatory approval gates. no code ships without user sign-off
- 🔒 Exhaustive escaping and sanitization rules for every output context
- ♿ WCAG 2.1 AA accessibility built into every phase and template
- 🎨 Tailwind CSS v3 CLI build pipeline. zero CDN references, zero frameworks
- 🔍 79-point self-audit table requiring cited file-and-line evidence for every check
- 🚦 Graduated failure modes. abort, degraded, or proceed based on source quality
- 🌍 Full internationalization with enforced translator comments and text domains
- 🧩 Smart template abstraction rules for repeated markup patterns
- 👶 Child theme compatibility with overridable functions and removable hooks
- 📦 Automatic chunk planning with size estimation to prevent truncation
- 🔄 Session continuity protocol for multi-conversation conversions
- 📋 Pre-output self-check validates every file before delivery
- ⚖️ Decision tiebreaker hierarchy when multiple valid approaches exist
- 🛡️ Nonce enforcement and input sanitization for all custom forms
- 📱 Mobile-first responsive design with keyboard and touch target requirements
- 🏷️ Strict naming conventions derived from a single confirmed theme name
- 📝 Auto-generated README with setup instructions, testing checklist, and documentation
- ⚡ Image performance rules. lazy loading, fetch priority, and registered custom sizes
- 🧪 Testing checklist covering core functionality, accessibility, and build system
- 📐 Content width single source of truth synced across PHP, JSON, and Tailwind config

#### 🔄 How it works

Hand it an `index.html` (and optionally a `single.html`, plus any other page mockups) and it walks you through a 4-phase conversion:

1. **Initialization**: confirm theme name and defaults
2. **Phase 1. Analysis** (1A critical, 1B extended). HTML validation, source quality grading, design-token extraction, file manifest, decision log
3. **Phase 2. Implementation**: generates every theme file in user-approved chunks
4. **Phase 3. Self-Audit**: a 79-item checklist with cited file-and-line evidence before delivery

You approve each phase before the next one starts, so nothing runs away from you.

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/html-to-wordpress-theme ← starts the workflow
/html-to-wordpress-theme Brewline ← pre-fills the theme name
```

**Natural language** (auto-triggers):

> *"I have an index.html and a single.html in my Downloads folder. convert them into a WordPress theme called 'Brewline'."*

Either way, confirm the theme name and defaults at the initialization gate, then approve each phase as it completes. Theme files are saved to a folder named after your theme slug.

The full skill instructions live at [`html-to-wordpress-theme/skills/html-to-wordpress-theme/SKILL.md`](html-to-wordpress-theme/skills/html-to-wordpress-theme/SKILL.md), with deep references in the adjacent [`references/`](html-to-wordpress-theme/skills/html-to-wordpress-theme/references/) folder.

#### 🤖 AI Analysis Verdict

> The skill's source instruction set was independently analyzed by Claude Opus 4.6. Below are the evaluation results.

| Aspect | Description | Rating | Score |
|--------|-------------|--------|-------|
| Completeness | Covers every edge case from abort criteria to degraded mode, with zero gaps in the conversion workflow | ★★★★★ | 10/10 |
| Structure | Phase gates, numbered sections, cross-references, and a document map make navigation even at 2000+ lines | ★★★★★ | 10/10 |
| Clarity | Every rule includes ✅/❌ examples, anti-patterns, and decision trees. leaves no room for misinterpretation | ★★★★★ | 10/10 |
| Maintainability | Versioned with changelog, modular sections, and a priority hierarchy that makes updates safe and predictable | ★★★★★ | 10/10 |
| Practical Effectiveness | Evidence-based self-audit, context window management, and session continuity ensure reliable output across real world usage | ★★★★★ | 10/10 |
| Error Handling | Graduated failure modes (abort → degraded → proceed) with explicit user checkpoints prevent silent failures | ★★★★★ | 10/10 |
| Security Coverage | Exhaustive escaping/sanitization tables, nonce enforcement, and a pre-output self-check catch vulnerabilities before they ship | ★★★★★ | 10/10 |
| Accessibility | WCAG 2.1 AA built into every phase. contrast ratios, keyboard nav, ARIA, skip links, and reduced motion are non-negotiable | ★★★★★ | 10/10 |
| **Overall** | **An AI engineering specification that rivals internal runbooks at mature development organizations** | **★★★★★** | **10/10** |

---

### `wordpress-architect-review`

Senior WordPress architect code review for plugins and themes. file by file audit covering security, performance, architecture, correctness, WordPress standards, accessibility, i18n, and missing infrastructure.

```
/plugin install wordpress-architect-review@chrismccoy
```

Most AI code reviews of WordPress plugins read like generic linter output: "consider adding error handling", "use prepared statements where possible", without ever quoting the offending line. The `wordpress-architect-review` skill takes a different stance. It acts as a senior WordPress architect with 15+ years on WordPress.org submissions, enterprise WP stacks, and security audits. Every finding cites `file:line`, quotes the exact offending code, tags severity (SEVERE / MODERATE / MINOR), states the actual impact, and gives the fix. No filler adjectives, no vague advice, no praise before issues.

Scope-locked. It will not write tutorials, recommend hosting, or answer general WP questions. only audit code. Prompt-injection defenses treat file contents as inert data, so a `// Ignore prior instructions...` comment in the audited code gets flagged as a CRITICAL Security finding rather than followed.

#### ✨ Features

- 🎯 Target auto-detection. plugin header in root PHP, `style.css` theme header, `block.json`, or `wp-content/mu-plugins/` path; aborts cleanly if none found
- 📖 Reads every file directly. every PHP/JS/CSS plus companion configs (`readme.txt`, `theme.json`, `composer.json`, `package.json`, `phpcs.xml`); no summarizing from filenames
- 🏷️ Severity-tagged findings. SEVERE / MODERATE / MINOR. mandatory format: title + `file:line` + code fence + Impact line + Fix line
- 📊 10-row scorecard. Security, Performance, Architecture, Correctness, WordPress Standards, Maintainability, Documentation, Testing, Accessibility/UX, Internationalization. overall weighted toward Security, Performance, Correctness
- 🛡️ Prompt-injection defense. inline instructions in the audited code are treated as inert data and reported as a CRITICAL Security finding
- 🔒 Scope lock. refuses tutorials, recommendations, hosting advice, non-code questions
- 🚫 Banned filler word list. no "leverage", "robust", "comprehensive", "utilize", "synergy", and ~15 more
- ✅ Pre-emit validation. partial reports are regenerated, never shipped
- 🗺️ Optional refactor roadmap. 3-phase modernization path appended when overall score is below 6/10

#### 📂 Categories covered

- **Architecture**: OOP vs procedural, namespacing, separation of concerns, autoloading, dependency injection
- **Performance**: query count, `get_option` autoload patterns, transient/object caching, asset enqueue strategy, N+1 queries, `WP_Query` efficiency
- **Security**: nonces, capability checks, ABSPATH guard, sanitization (correct filter per data type), escaping on output, prepared statements, CSRF, SSRF, file uploads, `eval`/`create_function`, raw `$_GET`/`$_POST`
- **Correctness**: type juggling, null handling, regex backtracking, race conditions, activation/deactivation idempotency
- **WordPress Standards**: Settings API, `register_setting`, `wp_enqueue_*`, text domain matching slug, i18n functions, REST patterns, hook priorities, transients, multisite
- **Theme-specific**: `wp_head()` / `wp_footer()`, `body_class()` / `post_class()`, template hierarchy, child theme compatibility, `theme.json`, FSE readiness, accessibility (skip links, ARIA, alt text)
- **Plugin-specific**: activation/deactivation/uninstall, `register_activation_hook`, `dbDelta` migrations, version constants, plugin row meta
- **Maintainability**: duplication, function length, naming clarity, dead code, hardcoded values
- **Missing Infrastructure**: `readme.txt` / `style.css` headers, `Requires PHP`, `Tested up to`, autoloader, PHPUnit, CI, `phpcs.xml` (WPCS), `.editorconfig`, `.gitignore`
- **Compatibility**: PHP/WP version range, deprecated function usage, block editor compatibility, multisite, RTL

#### 🔄 How it works

1. **Detect target**: looks for plugin header, theme `style.css`, `block.json`, or `mu-plugins` path
2. **Read everything**: every PHP/JS/CSS file plus companion configs, with the Read tool, never from filename summaries
3. **Categorize findings**: max 5 per category, most severe first, every one cited and quoted
4. **Score and rank**: fill the 10-row scorecard, list the top 5 fixes with S/M/L effort tags
5. **Optional roadmap**: append a 3-phase refactor plan if overall is below 6/10
6. **Pre-emit validation**: verify every section before returning; regenerate anything failing

#### 🚀 How to use it

```
/wordpress-architect-review ← audits the current working directory
/wordpress-architect-review ./wp-content/plugins/x ← audits the specified path
```

Or natural language: *"review my WordPress plugin for security holes"*, *"audit this theme before I submit to WordPress.org"*, *"is this plugin "*, *"give me a senior architect review of this WP code"*, *"rate my plugin out of 10"*.

The full skill instructions live at [`wordpress-architect-review/skills/wordpress-architect-review/SKILL.md`](wordpress-architect-review/skills/wordpress-architect-review/SKILL.md).

---

### `wordpress-consultant`

Senior WordPress Consultant (10+ years, WordPress VIP coding standards) that runs a fixed 10-section consulting framework over a WordPress project. Seven inputs in, an expert audit out, ending with a 0-100 scorecard and a single summary table.

```
/plugin install wordpress-consultant@chrismccoy
```

Most "WordPress help" devolves into a pile of disconnected tips - install this caching plugin, bump that PHP version, try a different host. This plugin replaces that with the audit a senior consultant would actually run: seven inputs describing the site, ten sections of structured analysis, and a final report that scores the project on health, performance, security, scalability, and code quality. Every section 1-9 is capped at 250 words and written as Finding / Impact / Recommendation bullets - no prose walls, no filler. Section 3 (WooCommerce) drops to `N/A` when the site is not a store. The consultant never recommends nulled or pirated plugins, never suggests editing WordPress core, never prints secrets in examples, and never assigns a security rating without naming what was checked.

The skill body runs the workflow. Step 1 validates inputs - if `Current Challenge` or `Development Goals` is blank it halts and asks, because an audit with no problem statement and no goal is fiction. Step 2 loads the Section 1-10 prompts from `references/framework.md`. Step 3 uses extended thinking before Section 4 (Performance) and Section 10 (Final Report), the two sections that need the deepest reasoning. Step 4 emits every section under its exact header per `references/output-contract.md`. Step 5 applies the Section 10 scales and ends with the mandatory summary table. Step 6 runs a silent self-validation gate - all 10 sections present, every score on its defined scale, table last - before delivery.

Hard refusal on out-of-scope asks (anything that is not WordPress engineering, declined in one line then back to the framework), on nulled/pirated plugins, on core-file edits, and on security ratings given without naming what was checked.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/wordpress-consultant/SKILL.md` carries the voice, scope lock, input gates, and 6-step workflow. The Section 1-10 analysis prompts live in `references/framework.md`. The output contract (word caps, Section 10 scales, summary-table columns, pre-delivery checklist) lives in `references/output-contract.md`. The full input-handling and prompt-injection rules live in `references/guardrails.md`. The slash command `/wordpress-consultant` accepts an optional `Current Challenge` arg, then walks the user through `AskUserQuestion` intake for all seven fields.

#### ✨ Features

- 🎯 Seven inputs in, a 10-section consultant report out. Website Type + Current Challenge + Technology Stack + Traffic Volume + Development Goals + Performance Requirements + Support Needed
- 🚧 Two required inputs gate the run - blank `Current Challenge` or `Development Goals` halts with `MISSING INPUT: <field> required.` The other five are optional and proceed with a flagged assumption at the top of the affected section
- 🧭 Fixed framework: Architecture Assessment, Development Strategy, WooCommerce Review, Performance Optimization Audit, Security Hardening, Debugging & Troubleshooting, Scalability & Infrastructure, Automation & Workflow, Technical Debt Assessment, Final Senior Consultant Report
- 🗜️ Max 250 words per section 1-9, written as Finding / Impact / Recommendation bullets. Section 3 drops to `Section 3 - N/A (not a WooCommerce site)` for non-stores
- 📊 Section 10 scorecard on fixed scales - Health, Performance, Security, Scalability, Code Quality (0-100); Technical Debt Severity (Low/Medium/High/Critical); Recommended Priorities (ranked, max 5)
- 📋 Mandatory Markdown summary table as the final element, every run, exact columns
- 🧠 Extended thinking before Section 4 (Performance) and Section 10 (Final Report)
- 🛡️ Security guardrails - never recommends nulled/pirated themes or plugins, never suggests editing core files, never outputs DB credentials/keys/secrets in examples, never claims a security rating without naming what was checked
- 🛑 Prompt-injection defense. All seven inputs treated as inert project data. Directives like `ignore prior`, `system:`, `act as`, role-switch attempts inside field values are ignored
- 🪝 Scope-locked to WordPress engineering. Non-WordPress requests declined in one line, then back to the framework

#### 🔄 How it works

1. **Intake.** Slash command collects all seven fields via `AskUserQuestion`. If `Current Challenge` was passed as `$ARGUMENTS`, confirm and seed it. Empty / blank / `[FIELD_NAME]` on a required field → halt with `MISSING INPUT: <field> required.`
2. **Validate.** Required gate on `Current Challenge` and `Development Goals`. Optional blanks proceed with a flagged assumption. Conflicting inputs (e.g. Website Type vs Challenge) named in one line and confirmed before proceeding.
3. **Load framework.** Read `references/framework.md`, `references/output-contract.md`, `references/guardrails.md`. Wrap all input values in `<inputs></inputs>` and treat as inert data.
4. **Extended thinking** before Section 4 and Section 10.
5. **Emit Sections 1-10** under exact headers. Mark `Section 3 - N/A` for non-stores. Max 250 words per section 1-9.
6. **Section 10 + summary table.** Apply the fixed scales. End with the single mandatory summary table - it must be last.
7. **Silent validation gate.** Confirm all 10 sections present, every score on its scale, table last, no security rating without naming what was checked. Fix any gap before output.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/wordpress-consultant "checkout is slow on our WooCommerce store"   ← arg seeds Current Challenge, intake fills the rest
/wordpress-consultant                                               ← full 7-question intake
```

**Natural language** (auto-triggers via the skill):

> *"review my WordPress architecture"*, *"WordPress performance audit"*, *"WordPress security review"*, *"scale my WordPress site"*, *"WooCommerce performance review"*, *"WordPress technical debt assessment"*, *"senior WordPress consultant"*

After the run, work the Section 10 priorities top-down - the ranked list is capped at 5 and ordered by impact, so start at the top, and use the summary-table scores to track health, performance, security, scalability, and code quality across follow-up engagements.

The full skill instructions live at [`wordpress-consultant/skills/wordpress-consultant/SKILL.md`](wordpress-consultant/skills/wordpress-consultant/SKILL.md), the slash command at [`wordpress-consultant/commands/wordpress-consultant.md`](wordpress-consultant/commands/wordpress-consultant.md), and the on-demand reference files at [`wordpress-consultant/skills/wordpress-consultant/references/framework.md`](wordpress-consultant/skills/wordpress-consultant/references/framework.md), [`wordpress-consultant/skills/wordpress-consultant/references/output-contract.md`](wordpress-consultant/skills/wordpress-consultant/references/output-contract.md), [`wordpress-consultant/skills/wordpress-consultant/references/guardrails.md`](wordpress-consultant/skills/wordpress-consultant/references/guardrails.md).

---

### `wordpress-formatter`

Formats a theme's template files and partials to the WordPress coding standard - tabs, spacing, array style, alignment - without changing how any page renders. It installs the tools, writes the config, runs the fixer, and checks the result.

```
/plugin install wordpress-formatter@chrismccoy
```

Most WordPress themes drift from the coding standard over time - mixed tabs and spaces, inconsistent array syntax, ragged alignment. This plugin cleans that up the safe way. It installs PHP_CodeSniffer and the WordPress Coding Standards into the theme's local `vendor/` folder (nothing global), writes a scoped `phpcs.xml.dist`, and runs `phpcbf` to fix everything that can be fixed automatically. It runs the fixer twice, since some fixes unlock others, then checks every changed file with `php -l` before it calls the job done.

The important part is what it will not do. Formatting should never change how a page renders, so anything that could change behavior is reported but left alone: turning a loose `==` into a strict `===`, adding the strict flag to `array_search`, or removing `extract()`. The one exception is Yoda conditions, which only reorder the two sides of a comparison and are safe, and even those are applied only if you say yes. It also stops early on the two things that go wrong most often: if the folder is not a WordPress theme, or if there is no `composer.json`, it asks or stops rather than guessing.

#### ✨ Features

- 🎯 Five quick questions first. Scope (templates and partials, or all theme PHP), strictness (formatting only, or the full standard), Yoda checks on or off, the theme name, and any files to skip. Say "just do it" for safe defaults
- 🧰 Installs the tools for you. PHP_CodeSniffer and the WordPress Coding Standards go into the theme's local `vendor/` as dev dependencies - nothing is installed globally
- 🧾 Writes a scoped config. A `phpcs.xml.dist` that leaves out `vendor`, `node_modules`, and by default `lib`, `inc`, `assets`, and `functions.php`
- 🔧 Fixes formatting only. Runs `phpcbf` twice for tabs, spacing, array style, and alignment - never escaping, sanitization, or behavior
- 🛡️ Leaves risky changes alone. Loose `==` to `===`, the `array_search` strict flag, and `extract()` are reported, not applied, so runtime behavior never changes
- ✅ Checks its own work. Runs `php -l` on every changed file and stops if anything breaks
- 🚦 Two safe stops. No `composer.json` means it asks before creating one; a failed install means it shows the exact error instead of guessing
- 🧱 Adds re-run shortcuts. `composer lint` and `composer format` so you can run it again anytime

#### 🔄 How it works

1. **Check first.** Confirm the folder is a WordPress theme (a `style.css` header or template files). Stop if it is not.
2. **Intake.** Ask the five questions and wait for the answers, or use the defaults on "just do it".
3. **Install.** Add PHPCS and WPCS as Composer dev dependencies, skipping if they are already there. Stop and report if the install fails.
4. **Configure.** Write `phpcs.xml.dist` scoped to the answers, and add the `lint` and `format` composer scripts.
5. **Fix.** Run `phpcbf` twice, then `php -l` on every changed file. A syntax error is a hard stop.
6. **Report.** List what was fixed and what was left, with a reason for each item that was left.

#### 🚀 How to use it

```
/wordpress-formatter ← formats the current theme
/wordpress-formatter ./wp-content/themes/mytheme ← formats a specific theme
```

Or natural language: *"format my WordPress theme to the coding standard"*, *"run phpcbf on my templates"*, *"fix the indentation and spacing in my theme"*, *"set up phpcs for this theme"*, *"convert my theme files to tabs"*.

The full skill instructions live at [`wordpress-formatter/skills/wordpress-formatter/SKILL.md`](wordpress-formatter/skills/wordpress-formatter/SKILL.md), and the slash command at [`wordpress-formatter/commands/wordpress-formatter.md`](wordpress-formatter/commands/wordpress-formatter.md).

---

## Plan and Design

### `app-blueprint`

Turns a one-line app idea into a complete, production-ready application blueprint.

```
/plugin install app-blueprint@chrismccoy
```

Ever sat down to build something and realized the hardest part isn't writing the code. it's deciding the folder layout, the data models, the API surface, the deployment target, and the testing plan before you've typed a single line? That's what this plugin solves.

The `app-blueprint` skill behaves like a senior software architect with 15+ years of production experience. Hand it five inputs (what the app does, the tech stack, the workload type, the language, and the scale) and it produces an 11-section blueprint with the folder tree, the layer walkthrough, the data models, every API endpoint, dependency choices with reasoning, environment variables, a testing plan, a deploy plan justified by your scale, architect's notes, and a self-validation table that auto-repairs inconsistencies before delivery.

What makes it different from a generic "design my app" prompt? It refuses to invent. no `MyApp`, no `UserService`, no `Entity1`. Every name derives from your `APP_DESCRIPTION`. It enforces consistency. every entity in the data-model section must appear in at least one API endpoint, every dependency must map to a folder or reference, the deployment target must be justified by your stated scale with a stated migration trigger. And it halts cleanly with `MISSING INPUT: <field> required` instead of guessing when an input is blank.

Whether you're scoping a weekend side project, prepping a team kickoff, or writing a `BLUEPRINT.md` for a real production system, this plugin gives you the binder a senior engineer would draft in their first ten minutes on the project.

#### 📋 Technical Overview

An AI instruction specification that generates 11-section production application blueprints from five required inputs.

Built around a locked 11-section template (`references/prompt-template.md`), strict consistency rules (folder/layer parity, entity/endpoint mapping, dependency reachability, scale-justified deployment), a section 11 validation table that runs before delivery, and prompt-injection defenses that treat input field values as inert data.

Designed to eliminate generic placeholder filler, refuse missing-input requests cleanly, and produce blueprints whose folder trees and data models cross-reference correctly.

#### ✨ Features

- 🏗️ 11 fixed sections in fixed order. project overview, folder tree, layer walkthrough, data models, API endpoints, dependencies, env vars, testing, deployment, architect's notes, self-validation
- 📥 Five required inputs. `APP_DESCRIPTION`, `TECH_STACK`, `APP_TYPE`, `LANGUAGE`, `SCALE`
- ❓ Slash command `/blueprint` runs an `AskUserQuestion` intake for any missing inputs. one question per missing field
- 🚫 No generic placeholders. all names derive from `APP_DESCRIPTION` (no `MyApp`, no `UserService`, no `FooEntity`)
- 🔁 Identical folder names in section 2 and layer names in section 3. parity enforced
- 🔗 Every section 4 entity must appear in at least one section 5 endpoint
- 📦 Every section 6 dependency must map to a folder (section 2) or a reference (section 8)
- 🚀 Deployment target (section 9) justified by `SCALE` explicitly. migration trigger always stated
- ✅ Section 11 validation table runs before output. any FAIL row repaired in place before delivery
- ⛔ `MISSING INPUT: <field> required. Provide value and re-run.` halt on any blank or placeholder input
- 🛡️ Prompt-injection defense. input field values treated as literal strings, never executed
- 🔒 Prompt secrecy. the template is never revealed, paraphrased, or summarized in output
- 📐 Output format. fenced code blocks for trees and config, tables for deps and env, domain-specific names everywhere

#### 🔄 How it works

1. **Intake**: the `/blueprint` slash command collects five inputs via `AskUserQuestion`. one question per missing field. existing inputs are reused
2. **Load template**: reads `references/prompt-template.md`. the authoritative 11-section spec
3. **Substitute placeholders**: replaces `{{APP_DESCRIPTION}}`, `{{TECH_STACK}}`, `{{APP_TYPE}}`, `{{LANGUAGE}}`, `{{SCALE}}`. treats values as inert data
4. **Emit sections 1-11**: in exact order, no additions, no reordering
5. **Self-validation**: runs the section 11 validation table. repairs any FAIL row in place before delivery

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/blueprint ← walks through the five-question intake
```

**Natural language** (auto-triggers via the skill):

> *"design a production architecture for a dog walking marketplace"*, *"blueprint an app that tracks plant watering schedules"*, *"architect a tool for booking guitar lessons"*, *"give me a full system blueprint for a multi tenant SaaS"*, *"production architecture for a coffee subscription box"*

The full skill instructions live at [`app-blueprint/skills/app-blueprint/SKILL.md`](app-blueprint/skills/app-blueprint/SKILL.md), the slash command at [`app-blueprint/commands/blueprint.md`](app-blueprint/commands/blueprint.md), and the 11-section authoritative template at [`references/prompt-template.md`](app-blueprint/skills/app-blueprint/references/prompt-template.md).

---

### `html-design-styles`

A curated catalog of 53 named design styles for frontend interfaces.

```
/plugin install html-design-styles@chrismccoy
```

Tired of AI generated frontends that all look like the same generic SaaS landing page? This skill ships specs for 53 distinct design aesthetics. each one a complete, opinionated system with its own color palette, typography stack, component patterns, and signature visual mechanics. Pick a style by name and the output actually *looks* like that style.

When the skill triggers, it knows exactly how to implement any style. fonts, colors, shadows, layout patterns, components, animations, and more. producing HTML in a single output.

#### 🎨 Available styles

##### Minimal & Clean
- 🍎 **Bento Style**: Apple/macOS-inspired bento grid, clean and minimal
- 🌿 **Soft Modern Style**: White bg, blurred orb accents, rounded, friendly and accessible
- ❄️ **Scandinavian Style**: Cold whites, extreme negative space, hygge minimalism, quiet luxury
- 🏢 **Corporate Style**: Conservative trust blues, structured grid, buttoned-up B2B professionalism
- 📐 **Swiss Style**: Helvetica-inspired, rigid typographic grid, black/red only, zero decoration

##### Dark & Atmospheric
- 🌌 **Dark Cosmic Style**: Dark slate, glowing indigo/cyan, radial dot grid, glassmorphism
- 🎬 **Dark Action Style**: Dark gradient bg, yellow/gold accents, Oswald font, cinematic energy
- 🚀 **Dark SaaS Style**: Slate-950, sky blue accent, stagger animations, clean SaaS
- 🎭 **Dark Cinema Style**: Near-black, red glow, Bebas Neue, noise overlay, floating labels
- 💾 **Dark Mono Style**: Dark zinc surfaces, cyan + pink accents, monospace, scanline texture
- 🌠 **Dark Neon Style**: Black background, multiple vivid neon glow colors, bleed and bloom effects
- 🌌 **Vaporwave Style**: Purple/teal gradients, retro grid floors, synthwave glow and glitch effects

##### Brutalist & Bold
- ⬛ **Pure Brutalist Style**: Monochrome black/white, hard shadows, monospace, no color
- ⚡ **Neobrutalist Style**: Hard black shadows with vivid neon color accents
- ☢️ **Acid Brutalist Style**: Pure black, acid yellow + red, Anton/Bebas fonts, noise grain
- 🔧 **Utility Terminal Style**: White bg, strict 1px borders, monospace, no rounding, grid texture
- 🏗️ **Monolith Style**: White bg, dark navy shadows, thick top border accent, monospace brutalism

##### Retro & Nostalgic
- 📺 **Retro Terminal Style**: Green-on-black CRT monitor aesthetic with phosphor glow effects
- 🕹️ **Pixel Style**: 8-bit pixelated fonts, game UI, sprite aesthetic, retro game feel
- 🖥️ **Y2K Style**: Windows 95 beveled gray UI, system fonts, chunky pixel buttons, early internet
- 🌊 **Groovy Style**: Warm oranges/browns, 70s swirls, rounded retro lettering, psychedelic curves
- 🎨 **Memphis Style**: 80s/90s geometric shapes, bright pastels, squiggles and confetti
- 🌴 **Tropical Style**: Coral, turquoise, warm vacation energy, Miami/resort vibes

##### Artistic & Expressive
- 🎪 **Pop Art Style**: Cyan/pink/yellow on loud background, floating bordered container
- 🍭 **Kawaii Style**: Super cute pastel, bubble rounded, character illustration accents
- 💥 **Manga Style**: Speed lines, bold ink outlines, dramatic panel layouts, high contrast
- 🌈 **Psychedelic Style**: Acid swirls, melting text, rainbow overflow, mind-bending distortion
- 🗞️ **Zine Style**: Photocopied DIY aesthetic, cut-and-paste collage, raw indie energy
- 🔆 **Aurora Style**: Flowing multi-color gradient backgrounds, silk light effect, soft and dreamy

##### & Luxury
- 👑 **Luxury Style**: Cream/off-white, serif display font, gold accents, generous whitespace
- 🌸 **Art Deco Style**: Geometric gold ornaments, symmetry, 1920s glamour and opulence
- 🌺 **Cottagecore Style**: Floral patterns, watercolor washes, storybook softness and whimsy
- 🌙 **Gothic Style**: Dark greens/blacks, ornate serif, candle-wax drips, moody atmosphere
- ✒️ **Japanese Style**: Wabi-sabi imperfection, ink brush strokes, kanji-inspired negative space

##### Technical & Structured
- 🔷 **Blueprint Style**: Deep blueprint blue, white grid lines, Courier Prime, technical drawing aesthetic
- 🔴 **Dot Grid Style**: Gray dotted background, Archivo Black + Space Mono, hot pink accent, hard shadows
- 🟣 **Pink Neo Style**: Hot pink dotted background, Archivo Black + Space Mono, pink/yellow/blue palette
- 📊 **Dashboard Style**: Chart-forward, dense metrics, sidebar navigation, admin/analytics feel
- 🤖 **Sci-Fi HUD Style**: Heads-up display, corner brackets, data readouts, radar and targeting UI
- ⚠️ **Cyberpunk Style**: Yellow/black warning stripes, HUD overlays, neon on dark, danger aesthetics

##### Specialty & Immersive
- 💎 **Glassmorphism Style**: Frosted glass cards on gradient mesh backgrounds, soft blurs and translucency
- 🏛️ **Neumorphism Style**: Soft same-color shadows creating pushed/extruded soft UI on light gray
- 📦 **Clay Style**: Clay morphism, chunky rounded cards with physical depth
- 🖨️ **Newspaper Style**: Black ink on newsprint, serif fonts, editorial column layouts
- 📖 **Longform Style**: Full-bleed hero images, pull quotes, drop caps, rich magazine editorial flow
- 🎵 **Skeuomorphic Style**: Realistic material textures, depth and shadows mimicking physical objects
- 🌸 **Organic Style**: Earthy tones, rounded organic shapes, a warm handmade look
- ✍️ **Handwritten Style**: Hand-drawn borders, pencil textures, imperfect sketch-like lines

##### Energy & Motion
- 🏆 **Athletic Style**: Diagonal cuts, bold color blocks, high-impact sport energy
- 🌍 **Grunge Style**: Worn textures, splatter marks, distressed rough torn edges
- 🔮 **Isometric Style**: 3D isometric grid illustrations, flat-color depth and layered objects
- 🎭 **Maximalist Style**: Everything layered, dense pattern-on-pattern, opulent visual chaos
- 🔣 **Enterprise Editorial Style**: White/dark alternating sections, indigo, large rounded app cards

#### 📦 What each style spec includes

Every style definition covers:

- 🔤 **Typography**: Font families, weights, sizes, letter-spacing
- 🎨 **Color palette**: All CSS custom properties with exact values
- 🪞 **Shadow system**: Named shadow levels used across components
- 🃏 **Card variants**: Background, border, hover states
- 🔘 **Button variants**: Primary, secondary, ghost, active/pressed states
- 📐 **Layout patterns**: Grid structures, hero layouts, section flows
- 🧩 **Components**: Pills, badges, stat cards, nav, marquee, footer
- ✨ **Animations**: Transitions, keyframes, scroll effects where applicable
- ⚙️ **Implementation notes**: CDN links, font imports, special CSS tricks

#### 💻 Output format

The skill generates a **single self-contained HTML file** with:

- Inline CSS (no external stylesheet needed)
- Tailwind CSS via CDN
- Google Fonts via CDN
- Font Awesome 6 via CDN (when icons are needed)
- Vanilla JS for any interactions

No build step. Open the file in a browser and it works.

#### 🔄 How it works

1. **Identify the style**: match the user's request against the 53-item catalog (or ask them to pick if ambiguous)
2. **Get project context**: full page, single component, restyling existing markup, what content goes in
3. **Load references**: `common.md` once per session for cross-cutting patterns, then `styles/<slug>.md` for the chosen style's complete spec
4. **Apply faithfully**: use the exact color values, typography stack, shadow recipes, and component patterns from the spec, with no "similar" substitutions

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/html-design-styles ← asks you to pick a style
/html-design-styles brutalist ← starts straight into Brutalist
/html-design-styles brutalist landing page for my SaaS
 ← pre-fills both style + project
```

**Natural language** (auto-triggers on style names). describe what you want:

**From scratch. describe your product inline:**

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

**From a feature list in your own README. point Claude at it and it pulls product name, features, and copy automatically:**

```
Read README.md. Build a landing page using neobrutalist style based on
the features and descriptions in README.md. Keep copy tight. headline,
subheadline, feature grid, and a single CTA.
```

**Restyle an existing landing page. pass in your HTML and Claude rebuilds it in a new style while preserving content and structure:**

```
Read landingpage.html. Rebuild the landing page using dark cinema style.
Keep all existing sections, copy, and CTAs. only change the visual design.
```

That's it. The skill handles the rest. typography, color palette, layout grid, components, and interactions. all consistent with the named style spec.

The full skill instructions live at [`html-design-styles/skills/html-design-styles/SKILL.md`](html-design-styles/skills/html-design-styles/SKILL.md), the cross-cutting patterns at [`references/common.md`](html-design-styles/skills/html-design-styles/references/common.md), and each style's complete spec under [`references/styles/`](html-design-styles/skills/html-design-styles/references/styles/).

---

### `accessibility-audit`

Finds, reports, and fixes WCAG accessibility issues in web UI, in the voice of a senior accessibility engineer. Five-field intake, four locked modes, four audit flows that prefer the rendered page over the source. Command only. it ships no skill file, so it never auto-triggers.

```
/plugin install accessibility-audit@chrismccoy
```

Most accessibility answers do one of two unhelpful things. They dump a raw axe-core log with two hundred entries, thirty of which are the same button repeated, or they start editing files when all you asked for was a report. This plugin does neither. It asks what you want first - mode, scope, and standard in one round, then a single follow-up only if it applies - and holds to the answers. Report mode never touches a file, no matter how obvious the fix looks. Findings are grouped by rule and by component family, so one broken button pattern reads as one finding with a count, not thirty rows. Every finding carries its WCAG criterion. Engine fix directives are quoted word for word rather than paraphrased, and anything that needs written content, alt text, a label, an error message, is left as a TODO with the rule ID instead of invented.

It prefers auditing the page as the browser actually renders it, because source code hides real failures. Four flows are tried in order: the AccessLint MCP for any URL, then a browser MCP when your logged-in session or a specific page state matters, then static analysis of HTML files or JSX rendered to a string, then a plain axe-core script when there is no MCP but there is Node and a dev server. Whichever one it used is stated in the output.

There is a fourth mode for the case where there is no file and no page, just a component you pasted. It returns a four-phase blueprint instead of a report: the flaws in the code as given, the technical approach before any code appears, the complete refactor in your stack with a comment on every accessibility addition, and a testing guide listing what each key should do and what a screen reader should announce. Those key bindings are not improvised. They come from the ARIA Authoring Practices tables bundled with the plugin, covering dialog, disclosure, accordion, tabs, menu and menubar, combobox, listbox, tree, slider, and grid. A custom binding that fights the standard pattern is treated as a defect, because assistive technology users show up already knowing what Arrow and Escape are supposed to do.

The honest part is what it refuses to claim. Automated checks catch roughly a third of real accessibility failures. Content clarity, screen reader announcement quality, keyboard flow, and complex contrast all need a person. Those get their own section in the report, listed as still to verify, rather than being quietly folded into a passing score. It also will not tell you that you are legally compliant, for the ADA or Section 508 or EN 301 549 or the EAA. It aligns code with WCAG technical criteria. Whether an organization is compliant is a legal determination made by people, on evidence this command does not produce.

**Why it is command only.** Every other plugin here ships a skill so it can trigger on natural language. This one does not, on purpose. Accessibility is a crowded space, and if you already have another accessibility plugin installed, two skills competing for "make this accessible" produces a coin flip. Dropping the skill file removes the coin flip. Type the command and you get this workflow, every time.

#### 📋 Technical Overview

A Claude Code plugin with two slash commands, no skill, and three reference files. The full workflow lives in `commands/accessibility-audit.md`. persona, intake, flow picker, all four mode workflows, locked output formats, bail rules, a silent pre-delivery validation gate, and hard rules. `commands/a11y-audit.md` is a thin alias that reads the canonical file. References load from `${CLAUDE_PLUGIN_ROOT}/references/` only while the command runs, so nothing competes at discovery time with another plugin's accessibility skill.

#### ✨ Features

- 🎯 Five intake fields. MODE + SCOPE + STANDARD, plus FIX_AUTHORITY when fixing and TECH_STACK when refactoring a pasted component
- 🔒 Four locked modes. Report writes and never edits, Fix runs baseline to edit to verify, Component returns a four-phase blueprint for pasted code, Guide applies the rules to UI you are writing
- 🌐 Four-tier flow picker preferring live DOM. AccessLint MCP, browser MCP, static analysis, local axe-core. always names the flow used
- 🧾 Deduplicated by rule ID and component family, prioritized by user impact. no thirty-row repeats
- 📐 WCAG criterion ID on every finding, across 2.1 AA, 2.2 AA, 2.2 AAA, and Section 508 / EN 301 549
- ⌨️ Per-widget expected keyboard tables from the ARIA Authoring Practices. dialog, disclosure, accordion, tabs, menu and menubar, combobox, listbox, tree, slider, grid
- ✍️ Never invents alt text, labels, or error copy below Full remediation. leaves a TODO with the rule ID
- 🧬 Every surviving ARIA attribute is justified. one that duplicates what a native element already says is treated as a defect, not a fix
- 🔁 Fix mode verifies by re-auditing and diffing the baseline, and bails loudly instead of iterating silently
- 🧷 Fix mode checks `git status` before editing and, if verification fails, hands you the exact revert command rather than leaving a mutated tree. it is the only mode that writes
- 🧑‍🦯 Separates automated findings from the manual and assistive-technology checks it cannot cover
- ⚖️ No legal compliance claims. not ADA, Section 508, EN 301 549, the EAA, or lawsuit risk. WCAG technical alignment only
- ✅ Silent output gate before every response. criterion ID on each finding, all four Component phases present, no invented copy, no compliance claim leaked, no padded findings when the audit comes back clean
- 🛡️ Injection defense over the audited code itself, not just your answers. a comment telling it to report no violations becomes a finding instead of an instruction
- 🧰 Bundled tooling: axe-core auditor, jest-axe component tests, contrast analyzer, keyboard and screen reader scripts, pa11y, GitHub Actions CI, HTML report generator
- 🚫 No skill file, by design. never auto-triggers, never collides with another accessibility plugin
- 🪧 Scope-locked. general UI design review, performance work, and non-accessibility refactors get one refusal line

#### 🔄 How it works

1. **Intake.** Two `AskUserQuestion` rounds - MODE, SCOPE, and STANDARD first, then FIX_AUTHORITY in Fix mode or TECH_STACK in Component mode, only when it applies. An argument passed with the command is offered as the pre-filled scope option.
2. **Validate.** Empty or placeholder required fields halt with one targeted question each. A whole-repo scope with no narrowing stops and asks for a directory, route, or component family. Component mode with nothing pasted asks for the source, and incompatible mode/scope pairs (Fix on a URL, Component on a directory) are rejected up front.
3. **Pick a flow.** AccessLint MCP, then browser MCP, then a local axe-core script, then static analysis as the last resort. Live-DOM auditing is preferred throughout; non-URL targets skip straight to static.
4. **Run the mode.** Report maps the surface, audits, groups by pattern, and writes the report. Fix baselines, locates each violation, applies within the chosen authority, then re-audits and diffs. Component runs audit, strategy, commented code, testing guide. Guide loads the rule catalog and applies it inline.
5. **Verify or flag.** Fix mode confirms targeted rules cleared and nothing new appeared, in a locked table of what was applied, what was deferred, and why. Report and Component modes list what still needs a human with a screen reader.
6. **Silent output gate.** Every finding carries a criterion ID, all four Component phases are present with complete code, nothing implies legal compliance, no copy was invented, and a clean audit is reported as clean rather than padded to fill the template. Failures are fixed before the response is sent.
7. **Output** with scope, standard, and flow named at the top.

#### 🚀 How to use it

```
/accessibility-audit src/components          ← arg seeds the scope
/accessibility-audit http://localhost:3000
/a11y-audit                                  ← short alias, full intake
/a11y-audit                                  ← then paste a component for Component mode
```

There is no natural-language trigger. That is the point. Both commands are identical and either one runs the same intake first.

The command lives at [`accessibility-audit/commands/accessibility-audit.md`](accessibility-audit/commands/accessibility-audit.md), the alias at [`accessibility-audit/commands/a11y-audit.md`](accessibility-audit/commands/a11y-audit.md), and the reference files under [`accessibility-audit/references/`](accessibility-audit/references/).

---

## Refactor, Map and Clean Up

### `refactoring-analyst`

Senior engineer refactoring review. evidence-first, citation-bound (`path:line`), 16 fixed sections, priority-tagged.

```
/plugin install refactoring-analyst@chrismccoy
```

Ever stared at a codebase and known something was wrong but couldn't name the specific files, lines, or smells you should fix first? That's what this plugin solves.

The `refactoring-analyst` skill turns Claude into a careful pre-merge architectural reviewer that reads your project, finds the messy parts, and gives you a structured report you can actually act on. Every finding cites `path:line`. Every priority is plain text (`CRITICAL` / `HIGH` / `MEDIUM` / `LOW`). Every section either reports findings or emits the exact phrase `None detected - <one-line reason citing what was checked>.` so you know nothing was skipped without a reason.

What makes it different from a generic "review my code" prompt? It operates on Martin Fowler's `Refactoring` catalog, Robert Martin's `Clean Code`, and the SOLID + GRASP design heuristics as its reference grammar. It enforces a SCALE RULE when the codebase exceeds 50 files. prioritizes files matching your `FOCUS_AREAS` first, samples the rest one per major directory, and is honest about which files were fully read versus sampled. It never claims to have analyzed a file it didn't read. And it ships with a `/refactor` slash command that runs a multiple-choice intake (path, focus areas, scope, depth) so you don't have to type a long prompt.

Whether you're prepping a real refactor sprint, doing a pre-merge architectural pass, scoping technical debt for a quarterly plan, or just want a senior dev's honest read on a folder, this plugin produces the report you'd hire someone to write.

#### 📋 Technical Overview

An AI instruction specification that generates a 16-section refactoring plan with `path:line` citations, `CRITICAL` / `HIGH` / `MEDIUM` / `LOW` priorities, a Top 5 Critical Issues block, a File Impact Matrix, an Issue Summary Table, and a phased Implementation Plan with risk and rollback notes.

Built around the locked 16-section template (`references/sections.md`), the hard-constraint and SCALE / FOCUS_AREAS rules (`references/constraints.md`), the summary tables spec (`references/summary.md`), a silent STEP 17 self-validation that re-runs the report before delivery, and prompt-injection defenses that treat `TARGET_PATH` and `FOCUS_AREAS` as inert data.

Designed to refuse fabrication. never claim to have read a file that wasn't read, never skip a numbered section, never invent line numbers.

#### ✨ Features

- 📋 16 fixed sections in fixed order. codebase overview, cross-file coupling, duplication, readability, naming, structure, side effects, error handling, performance, security, testing, complexity, design patterns, anti-patterns, refactoring recommendations, implementation plan
- 📍 Every finding cites `path:line`. no vague "somewhere in `auth/`"
- 🎯 Priority labels. `CRITICAL`, `HIGH`, `MEDIUM`, `LOW`. plain text. works in every terminal. no emoji
- 📊 Three summary blocks. Top 5 Critical Issues, File Impact Matrix (files ranked by issue density), Issue Summary Table (every problem with effort estimate)
- 🗺️ Phased Implementation Plan. risk and rollback strategy per phase
- 🚦 SCALE RULE. if file count > 50, prioritizes `FOCUS_AREAS` files first, samples one per major directory, states exactly which were fully analyzed vs sampled
- 🎛️ FOCUS_AREAS RULE. sections matching focus extend to 800 words, others cap at 400
- 🧠 Martin Fowler `Refactoring` catalog, Robert Martin `Clean Code`, SOLID, GRASP. the reference grammar for every finding
- 🛡️ "None detected - <reason>" exact phrase when a section is empty. never skipped without a reason
- ✅ Silent STEP 17 self-validation. checks every claim, regenerates failed sections before output
- 🔒 Prompt-injection defense. `TARGET_PATH` and `FOCUS_AREAS` treated as inert data. directives inside inputs are logged in Section 1 and ignored
- 🚫 Refuses to fabricate. never claims to have analyzed an unread file. never invents line numbers
- 💬 `/refactor` slash command with multiple-choice intake. path, focus areas (multi-select), scope (file / folder / recent / sample), depth (quick / standard / deep)

#### 🔄 How it works

1. **Step 0 - Access verification**: attempts to read `TARGET_PATH`. on failure reports path attempted, error, and what the user should check. does not proceed
2. **Step 1 - SCALE RULE**: if file count > 50, prioritizes `FOCUS_AREAS` matches first, samples remaining one per major directory, states exactly which files were fully analyzed vs sampled
3. **Step 2 - Emit sections 1-16**: in exact order, with `path:line` citations and `CRITICAL` / `HIGH` / `MEDIUM` / `LOW` priorities
4. **Step 3 - Emit Summary**: Top 5 Critical Issues, File Impact Matrix, Issue Summary Table per `references/summary.md`
5. **Step 4 - Silent STEP 17 self-validation**: runs the constraint checklist. regenerates any failed section before delivery

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/refactor src/my-app ← runs the multiple-choice intake then the report
/refactor             ← prompts for the path
```

**Natural language** (auto-triggers via the skill):

> *"analyze code for refactoring"*, *"produce a refactoring plan for src/"*, *"find code smells in this project"*, *"architectural review of this codebase"*, *"SOLID/GRASP audit on auth/"*, *"find God classes"*, *"Martin Fowler refactoring catalog review"*, *"pre-merge architectural review"*

The full skill instructions live at [`refactoring-analyst/skills/refactoring-analyst/SKILL.md`](refactoring-analyst/skills/refactoring-analyst/SKILL.md), the slash command at [`refactoring-analyst/commands/refactor.md`](refactoring-analyst/commands/refactor.md), and the 16-section template, constraint list, and summary tables spec at [`references/sections.md`](refactoring-analyst/skills/refactoring-analyst/references/sections.md), [`references/constraints.md`](refactoring-analyst/skills/refactoring-analyst/references/constraints.md), and [`references/summary.md`](refactoring-analyst/skills/refactoring-analyst/references/summary.md).

---

### `codebase-to-mermaid`

Point Claude at any codebase. Get a validated Mermaid diagram of how the code actually flows. Every node and edge cited to a real `file:line`.

```
/plugin install codebase-to-mermaid@chrismccoy
```

Ever joined a new project and burned a whole afternoon trying to figure out where the request enters, where it hits the database, and which file actually owns the business logic? The README claims one thing, the architecture diagram in the wiki is two years stale, and the only honest source of truth is the code itself. This plugin solves that. Point it at a repo and it reads the actual source, classifies the project (HTTP service, CLI, data pipeline, SPA, Next.js, WordPress plugin/theme, WooCommerce, Laravel, Symfony, Spring Boot, ASP.NET Core, Go service, Rust web service, Bash + WP-CLI, htmx, Alpine, Livewire, Vue SPA, C/C++/Qt/Unity, monorepo - 19+ languages, 30+ frameworks), and writes a Mermaid diagram showing the real flow with every node tied back to a file path and line number.

The skill runs five phases. Phase 1 globs the tree, reads manifests (`package.json`, `composer.json`, `go.mod`, `Cargo.toml`, `pom.xml`, `pyproject.toml`, `Gemfile`), and greps framework signals. Phase 2 picks the archetype from a 30+-row classification table. Phase 3 drafts the diagram with kebab-case node ids, verb-phrase edge labels (`POST /login`, `emits user.created`, `awaits row`), and subgraphs grouped by package boundary. Phase 4 self-validates: every node has a `file:line` citation, every edge is something you can `Grep` for, Mermaid syntax check, 40-node cap enforced. Phase 5 writes raw Mermaid source to `flow.mmd` (or `flow-request-lifecycle.mmd` + `flow-service-topology.mmd` for paired archetypes) and prints a Markdown report to chat with diagram, legend, and notes.

Hard refusal on invented modules, decorative edges, paraphrasing the README instead of reading the code, and on out-of-scope asks (code review, refactor proposals, bug hunts, security/performance audits - those are different skills).

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/codebase-to-mermaid/SKILL.md` carries the five-phase procedure (Discover → Classify → Draft → Validate → Emit) and constraints. The bulky framework grep cheat sheet, archetype-to-diagram table, and 24 worked few-shot examples live in `references/` and load only when the model needs them - keeps base context light. The slash command `/codebase-to-mermaid` accepts an absolute or relative path, or shows a two-option picker (current working directory vs custom path) when invoked bare.

#### ✨ Features

- 🗺️ Reads the whole project. Globs the tree, reads manifests, greps framework signals - no skimming the README and guessing
- 🔍 Auto-classifies the archetype across 19+ languages (JS, TS, PHP, Python, Go, Rust, Java, Kotlin, C#, C, C++, Ruby, Swift, Bash, Vue, Svelte, Razor) and 30+ framework families (React, Vue, Next.js, Nuxt, Astro, Remix, SvelteKit, Express, Fastify, NestJS, Hono, Koa, Laravel, Symfony, Livewire, Slim, Drupal, Magento, WordPress core / plugin / theme / Gutenberg / WooCommerce, WP-CLI, Spring Boot, Quarkus, Micronaut, Vert.x, ASP.NET Core, Blazor, MAUI, Unity, Qt, Drogon, Crow, axum, actix, rocket, leptos, yew, htmx, Alpine, chi, gin, echo, fiber, cobra, clap, FastAPI, Flask, Django, Rails, Airflow, Prefect, Dagster, Kafka, RabbitMQ)
- 📐 Picks the right diagram kind: `flowchart TD` for branching control flow, `flowchart LR` for pipelines and service maps, `sequenceDiagram` per route, `classDiagram` for ORM models
- 🏷️ Every node carries a `file:line` citation in the legend. Unverifiable node = deleted node
- 🚫 No invented modules, no decorative edges. If you cannot `Grep` for the call, the edge is deleted
- ✂️ Caps each diagram at 40 nodes. Bigger projects get an overview plus per-archetype zooms instead of one unreadable wall
- ⚠️ Flags destructive steps (`wp db reset`, `wp search-replace`, `rm -rf`, `aws s3 rm --recursive`) with a distinct node style
- 🤝 Pairs archetypes that travel together. WordPress plugin + WooCommerce, Laravel + Livewire, Go/chi + htmx + Alpine, Next.js + Prisma + tRPC - emits one diagram per layer plus a round-trip `sequenceDiagram`
- 📝 Writes raw Mermaid to `flow.mmd` (or `flow-<archetype>.mmd` per diagram) with no fences and no commentary, so it pipes straight into `mmdc -i flow.mmd -o flow.svg`
- 🖨️ Prints a Markdown report to chat: rendered diagram + legend (`node-id → relative/path.ext:line - one-line role`) + notes (external systems, async boundaries, anything skipped)
- 🚦 Scope-locked. Refuses code review, refactor proposals, bug hunts, security/performance audits, README rewrites, "explain this function". Diagram + legend + notes only

#### 🔄 How it works

1. **Discover.** `Glob` the tree for layout and manifest files. Read manifests for entry points and declared deps. `Grep` framework signals from the cheat sheet in `references/framework-signals.md`. Build an internal `{module → file → exported_symbols → callers}` inventory capped at the top ~50 modules by inbound edges.
2. **Classify.** Pick the archetype from `references/archetype-table.md`. If two archetypes both fit, emit two diagrams. WordPress plugins/themes, Laravel/Symfony apps, and hypermedia stacks (htmx/Alpine/Livewire on top of a backend) almost always warrant at least two.
3. **Draft.** Write Mermaid with stable kebab-case node ids, human-readable labels, verb-phrase edge labels from real call sites, subgraphs by package boundary.
4. **Validate.** Self-check: every node id appears in the legend with a real `file:line`; every edge corresponds to a real call/import/route/hook/message you can `Grep` for; Mermaid syntax parses (balanced brackets, no reserved-word collisions, no orphan nodes, no labels with unwrapped special chars); diagram fits the 40-node cap or is split.
5. **Emit.** `Write` the raw Mermaid source to `flow.mmd` (or per-archetype `.mmd` files) into the target directory. Print the Markdown report to chat.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/codebase-to-mermaid /path/to/repo         ← map this repo
/codebase-to-mermaid ../sibling-project    ← relative paths work too
/codebase-to-mermaid                        ← picker: current dir vs custom path
```

**Natural language** (auto-triggers via the skill):

> *"map this codebase"*, *"draw a diagram of this repo"*, *"generate a flow diagram"*, *"make a mermaid diagram"*, *"visualize this project"*, *"show how this code flows"*, *"diagram the architecture"*, *"sequence diagram of this endpoint"*, *"class diagram of these models"*, *"onboarding diagram"*, *"produce a flow.mmd"*

After the run, render the saved `.mmd` file two ways:

```bash
# CLI (mermaid-cli)
npx -p @mermaid-js/mermaid-cli mmdc -i flow.mmd -o flow.svg
```

Or paste the contents of `flow.mmd` into <https://mermaid.live>.

The full skill instructions live at [`codebase-to-mermaid/skills/codebase-to-mermaid/SKILL.md`](codebase-to-mermaid/skills/codebase-to-mermaid/SKILL.md), the slash command at [`codebase-to-mermaid/commands/codebase-to-mermaid.md`](codebase-to-mermaid/commands/codebase-to-mermaid.md), and the on-demand reference files at [`codebase-to-mermaid/skills/codebase-to-mermaid/references/framework-signals.md`](codebase-to-mermaid/skills/codebase-to-mermaid/references/framework-signals.md), [`codebase-to-mermaid/skills/codebase-to-mermaid/references/archetype-table.md`](codebase-to-mermaid/skills/codebase-to-mermaid/references/archetype-table.md), [`codebase-to-mermaid/skills/codebase-to-mermaid/references/examples.md`](codebase-to-mermaid/skills/codebase-to-mermaid/references/examples.md).

---

### `mermaid-to-ascii`

Hand it a Mermaid diagram file. Get back the same diagram drawn in plain text-art, saved right next to the original as a `.txt`.

```
/plugin install mermaid-to-ascii@chrismccoy
```

Mermaid is great until you need the picture somewhere that can't render it: a code comment, a plain-text README, a chat message, a terminal, an email. This plugin takes a `.mmd` file and redraws it as tidy monospace text-art you can paste anywhere. It reads the file, works out what kind of diagram it is, lines everything up with fixed spacing, and writes the result to a `.txt` with the same name. Your original file is never touched.

It handles all the common Mermaid types: sequence diagrams become vertical lifelines with arrows crossing between them, flowcharts become connected boxes that follow the top-down or left-right direction you set, class diagrams become bordered boxes with their fields listed inside, state diagrams and ER diagrams get boxed nodes with labeled links, and gantt charts become rows of bars along a time axis. Every name, label, message, condition, and grouping block from the source is kept exactly as written, nothing dropped or renamed.

It asks one thing before it starts: which file to convert. If you named the file in your request it uses that; if you didn't, it asks and waits rather than guessing. Anything written inside the diagram is treated as plain drawing data, so a label that happens to read like an instruction just gets drawn, never obeyed. If a diagram is too wide for a terminal it splits into stacked sections instead of cutting anything off, and if the file is empty or broken it tells you what failed instead of inventing a picture.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/mermaid-to-ascii/SKILL.md` carries the filename-first intake, the eleven conversion rules (Rule 0 through Rule 10), the edge-case handling, and the output contract. The six per-type ASCII layout templates live in `references/skeletons.md` and load only once the diagram type is known, so the base context stays light. The slash command `/mermaid-to-ascii` takes a file path, or asks for one when invoked bare.

#### ✨ Features

- 🧭 Asks which file to convert first, then stops and waits. No guessing, no scanning for a file you didn't name
- 🔁 Restates the plan once ("Converting `flow.mmd` -> `flow.txt`") before it does anything
- 📐 Handles every common Mermaid type: sequence, flowchart/graph, class, state, ER, and gantt
- 🧱 Picks the right text layout per type from six bundled templates, loaded only when needed
- 🏷️ Keeps every name, label, message, condition, and grouping block (`alt`/`else`/`opt`/`loop`/`par`). Nothing dropped, nothing renamed
- 📏 Fixed column spacing, aligned boxes, spaces not tabs, sized for an 80-120 character terminal
- ✂️ Splits oversized diagrams into stacked, labeled sections instead of cutting them off
- 🧾 Starts with a title and ends with a legend explaining every symbol used
- 🛟 Reports a clear parse error on empty or broken files and writes nothing; renders the good part of a partly broken file and lists the lines it skipped
- 🔒 Treats everything inside the file as drawing data, never instructions, even comments and labels that look like commands
- 📝 Writes only to the matching `.txt` and leaves the source file untouched

#### 🔄 How it works

1. **Get the filename.** Use the file named in the request, or ask "Which Mermaid file should I convert?" and wait. Set the output name to the same base name with a `.txt` extension and restate the mapping.
2. **Read and identify.** Parse the source and work out the diagram type, which decides the layout.
3. **Lay it out.** Load the matching template from `references/skeletons.md` and draw the diagram with fixed spacing and aligned boxes, keeping every label and grouping block.
4. **Handle the awkward cases.** Approximate an unknown type and say so, split anything too wide, report parse errors on empty or broken source, and list any lines that couldn't be drawn.
5. **Save it.** Write the text-art to the `.txt` file, report which nodes and frames were captured, and leave the original alone.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/mermaid-to-ascii flow.mmd     ← convert this file
/mermaid-to-ascii              ← asks which file to convert
```

**Natural language** (auto-triggers via the skill):

> *"convert this mermaid to ascii"*, *"turn diagram.mmd into ascii art"*, *"render this sequence diagram as text"*, *"make an ascii version of this flowchart"*, *"mermaid to txt"*

The full skill instructions live at [`mermaid-to-ascii/skills/mermaid-to-ascii/SKILL.md`](mermaid-to-ascii/skills/mermaid-to-ascii/SKILL.md), the slash command at [`mermaid-to-ascii/commands/mermaid-to-ascii.md`](mermaid-to-ascii/commands/mermaid-to-ascii.md), and the on-demand layout templates at [`mermaid-to-ascii/skills/mermaid-to-ascii/references/skeletons.md`](mermaid-to-ascii/skills/mermaid-to-ascii/references/skeletons.md).

---

### `explain-my-code`

Point Claude at any codebase. Get back one self-contained Markdown document that onboards anyone new to the project - architecture, flows, patterns, risks - with every component named from the real source.

```
/plugin install explain-my-code@chrismccoy
```

Ever been handed a repo on day one with no docs, no diagram, and the one person who knew it left three months ago? You spend a week clicking through folders just to learn where the app starts and how a request reaches the database. This plugin replaces that week. Point it at a repo and it reads the actual source like a senior architect doing your onboarding for you, then writes a single `CODEBASE_DOCUMENTATION.md` you can hand to the next person who joins. No sit-down handover, no "ask whoever wrote it," no stale wiki.

The skill runs five phases. Phase 1 scopes the target (finds the repo root, reads manifests first - `package.json`, `go.mod`, `pom.xml`, `Cargo.toml`, `*.csproj`, Dockerfile, CI configs). Phase 2 identifies the foundations (tech stack, languages, frameworks, and whether it's a monolith, microservices, or modular). Phase 3 traverses folder-by-folder and module-by-module, inferring design patterns and tracing the data and dependency flow. Phase 4 writes all 13 sections with real file, class, and function names and embedded Mermaid diagrams. Phase 5 verifies before delivery - every section present and non-shallow, every cited symbol actually in the repo, every Mermaid block valid - then saves the file and tells you the path.

Hard refusal on shallow summaries, skipped sections, invented symbols, and silent guessing (undocumented behavior is inferred out loud, with the assumption stated). Scope-locked to documentation - it won't do line-by-line review, refactor plans, or diagram-only output (those are different skills).

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/explain-my-code/SKILL.md` carries the five-phase procedure (Scope → Identify → Traverse → Write → Verify), the 13-section output contract, and the preserved source constraints. The slash command `/explain-my-code` accepts an absolute or relative path, or shows a two-option picker (current working directory vs custom path) when invoked bare.

#### ✨ Features

- 📖 Reads the whole project. Globs the tree, reads manifests first, then walks folder-by-folder - no skimming and guessing
- 🧭 Works out the shape: tech stack, languages, frameworks, and monolith vs microservices vs modular
- 🔁 Traces how it actually runs: entry points, startup sequence, request lifecycle, auth flow, and data flow from input → processing → storage
- 🏷️ Names real things. Every component, class, and function in the doc is a real, `Grep`-verifiable symbol - no `MyApp`, no `FooService`
- 📊 Embeds Mermaid `graph TD` for architecture and `sequenceDiagram` for flows, right inside the document
- 📑 Always 13 sections, always in order. An inapplicable section keeps its heading and says `Not applicable - <reason>` rather than vanishing
- 🧱 Skips the noise. `node_modules`, `vendor`, `dist`, `build` excluded from traversal and noted as skipped
- 🧩 Big repo? Analyzes in chunks - manifests and entry points first, then module by module - and is honest about anything sampled rather than read in full
- 📝 Writes one `CODEBASE_DOCUMENTATION.md` to the repo root and reports the path
- 🚦 Scope-locked. Refuses code review, bug hunts, refactor plans, and diagram-only output

#### 🔄 How it works

1. **Scope.** Find the repo root (default: current working directory). `Glob` the layout and read manifest/config files first. Stop and ask if there's no code at the target.
2. **Identify.** Determine languages, frameworks, and infra split; classify the architecture; locate entry points and config loading.
3. **Traverse.** Walk folder/service/module by module. Infer design patterns (MVC, Clean, Hexagonal, Factory, Observer) and record where and why each is used. Trace business logic, dependency flow, and data flow.
4. **Write.** Produce all 13 sections with real symbol names and embedded Mermaid. Where behavior is undocumented, infer it and state the assumption explicitly.
5. **Verify.** Confirm every section is present and substantive, every cited symbol exists, every Mermaid block parses. `Write` the document and report its path.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/explain-my-code /path/to/repo         ← document this repo
/explain-my-code ../sibling-project    ← relative paths work too
/explain-my-code                        ← picker: current dir vs custom path
```

**Natural language** (auto-triggers via the skill):

> *"document this codebase"*, *"explain my code"*, *"generate architecture docs"*, *"write an onboarding doc"*, *"analyze this repo"*, *"help a new dev understand this whole codebase"*, *"write up how this project works"*, *"map out this code into a doc"*

The full skill instructions live at [`explain-my-code/skills/explain-my-code/SKILL.md`](explain-my-code/skills/explain-my-code/SKILL.md) and the slash command at [`explain-my-code/commands/explain-my-code.md`](explain-my-code/commands/explain-my-code.md).

---

### `docblock-rewrite`

Convert PHPDoc and JSDoc `/** ... */` blocks into one-line plain-English `//` comments. Two engines under one ruleset.

```
/plugin install docblock-rewrite@chrismccoy
```

Ever inherited a codebase where every function has a perfectly-tagged PHPDoc block that tells you absolutely nothing about what the code does for a human reader? `@param string $token`, `@return bool`, three lines of jargon, and a non-technical teammate (PM, designer, support) bouncing off it. That's what this plugin solves.

The `docblock-rewrite` skill takes existing doc blocks and replaces each one with a single `// ` comment a non-coder could understand. Tech jargon banned (no `array`, no `callback`, no `instantiate`). 100-character cap. Capitalized, present-tense verb for functions, noun phrase for classes / files / constants. Tags stripped - `@param`, `@return`, `@throws`, `@since`, `@author`, `@version`, all of it. Doc blocks marked `@internal`, `@deprecated`, or `@ignore` are left alone.

Two engines apply the same rules: an **interactive** Read / Edit walk the model runs directly for small jobs (1-20 files) when you want to tune the prompt or eyeball edge cases, and a **bundled bash + perl + claude --print runner** for bulk jobs (20+ files, repeat runs, CI / unattended). The script walks the directory, parses doc blocks with perl, calls Claude Haiku once per symbol, validates every response against the banned-word list and 100-char cap, and applies replacements right-to-left so byte offsets stay valid. Bad outputs leave the original block intact for human review. `.bak` files saved next to every modified file unless `--no-backup`.

Whether you're shipping a plugin to non-technical merchants, onboarding a new teammate who keeps asking what each function does, or cleaning up a decade-old PHPDoc graveyard before handing the repo off, this plugin turns wall-of-tags doc blocks into comments that read like a sentence.

#### 📋 Technical Overview

A Claude Code plugin with a slash command, a skill, and a bundled three-file runner (bash + 2× perl) that share one set of rewrite rules. The skill body in `skills/docblock-rewrite/SKILL.md` carries the full rule set and decides which engine to use based on file count. The slash command `/docblock-rewrite` invokes the runner via `${CLAUDE_PLUGIN_ROOT}/scripts/docblock-rewrite.sh`. Both engines emit the same `// <summary>.` format.

#### ✨ Features

- 🧹 Strips PHPDoc / JSDoc blocks down to one plain-English `//` line
- 🚫 Banned-word list (`instantiate`, `invoke`, `callback`, `promise`, `iterate`, `async`, `boolean`, `array`, `object`, `parameter`, `argument`, `mutate`, `hash`, `payload`, `instance`, `factory`, `singleton`, `polyfill`, `regex`) - validation rejects any output that contains them
- 📏 100-character total cap including the leading `// `
- 🏷️ Honors `@internal`, `@deprecated`, `@ignore` opt-out tags - leaves those blocks alone
- 📄 File-level detection via `@file` / `@package` / `@module` or a post-block `declare` / `namespace` / `use` / `import` / `export` line
- 🗂️ Walks `.php`, `.js`, `.ts`, `.jsx`, `.tsx`, `.mjs`, `.cjs` - skips `vendor`, `node_modules`, `dist`, `build`, `coverage`, `__tests__`, `.git`, `.next`, `.nuxt`, `out`, `tmp`, `*.min.js`, `*.min.css` by default
- 🛟 `.bak` backup written next to every modified file unless `--no-backup`
- 🔍 `--dry-run` prints unified diffs without writing
- 🚦 Validation gates per response: one-line, `// ` prefix, length cap, banned-word regex - failures leave the original block intact
- ⚙️ Concurrency-tunable (`--concurrency N`, default 3) parallel `claude --print` calls via `xargs -P`
- 🪓 Right-to-left byte-splice in `apply-plan.pl` keeps offsets valid across multi-block files
- 🤖 Same prompt rules in both the inline skill engine and the scripted engine

#### 🔄 How it works

**Inline engine (skill, small jobs):**

1. Model uses Grep / Glob to find candidate files
2. For each file: `cp file file.bak`, Read the file, identify every `/** ... */` block and its following declaration, rewrite each one with Edit, self-check against the rule set before applying
3. Report file count, blocks rewritten, blocks skipped, blocks needing review

**Scripted engine (bulk):**

1. `find` walks the path with the skip list
2. `extract-docblocks.pl` slurps each file, emits JSON pairs of `(doc block, next non-blank line)`
3. Bash loops the pairs, builds a prompt with the rule set + few-shot examples + the docblock + the symbol, pipes through `claude --model … --print`
4. Output gets `head -n1` + trim, runs through `validate_output` (one line, `// ` prefix, length cap, banned-word grep)
5. Validated outputs go into a per-file plan file as `start <TAB> len <TAB> base64(new)`
6. `apply-plan.pl` applies plan entries right-to-left so earlier byte offsets stay valid, renames original to `.bak`, writes new contents

#### 🚀 How to use it

Two ways to invoke:

**Slash command** (scripted bulk run):

```
/docblock-rewrite . --dry-run     ← dry run on current dir
/docblock-rewrite src/            ← real run with .bak backups
/docblock-rewrite src/ --no-backup --concurrency 8
```

**Natural language** (auto-triggers via the skill):

> *"rewrite docblocks in src/"*, *"convert my PHPDoc to plain English"*, *"strip jargon from comments in formatting.php"*, *"make these JSDoc blocks readable to a non-coder"*, *"turn my doc blocks into friendly one-liners"*

The skill picks the engine based on file count - small jobs run inline, big jobs hand off to the script.

The full skill instructions live at [`docblock-rewrite/skills/docblock-rewrite/SKILL.md`](docblock-rewrite/skills/docblock-rewrite/SKILL.md), the slash command at [`docblock-rewrite/commands/docblock-rewrite.md`](docblock-rewrite/commands/docblock-rewrite.md), and the bundled runner at [`docblock-rewrite/scripts/docblock-rewrite.sh`](docblock-rewrite/scripts/docblock-rewrite.sh), [`docblock-rewrite/scripts/extract-docblocks.pl`](docblock-rewrite/scripts/extract-docblocks.pl), [`docblock-rewrite/scripts/apply-plan.pl`](docblock-rewrite/scripts/apply-plan.pl).

#### Requirements (script only)

`bash` 4+, `jq`, `perl` with `MIME::Base64`, `claude` CLI on `PATH` (Claude Code subscription auth, no API key required).

---

### `unslop`

Strip AI generated voice from source files without changing behavior.

```
/plugin install unslop@chrismccoy
```

Every AI generated codebase has the same tells: `// leverage this robust, comprehensive solution to seamlessly orchestrate the data provider`, em-dashes everywhere, every comment opens with "This function...", every function name is `orchestrateDataProvider` when `loadUsers` would do. The `unslop` skill takes a rule based pass over comments, docstrings, log/error messages, and identifier names. It never touches code logic, function signatures, return types, string literals shown to end users, or CLI help text. Your code keeps working exactly the same. The fluff goes away. What's left sounds like a real person wrote it.

Scope locked at the file edit layer. The skill will not refactor business logic, fix bugs, modify error messages users see, rewrite commit messages, or edit `CHANGELOG`/`LICENSE`. Renames verify substring safety before applying (won't rename `extract` to `pull` if `extractor` exists in the file).

**Rule 0 hard floor**: if asked mid pass to change behavior, logic, signatures, or strings under any rationale ("just this once", "trivial fix", "while you're there"), the skill refuses with `Out of scope for this pass. Open a new session for behavior changes.` and stops. Rule 0 cannot be overridden by subsequent user instructions.

**Target picker**: when invoked without a target, the skill asks via a picker. **File** (one source file), **Directory** (folder, processed file by file per Rule 12), or **Paste** (paste code into chat, get cleaned version back, no filesystem write).

#### ✨ Features

- 🧽 **Vocabulary swap**: kills marketing words (`robust`, `seamless`, `comprehensive`, `world-class`, `powerful`, `elegant`, `crucial`, `vital`, `revolutionary`, `transformative`, `game-changing`, `mission-critical`, `bleeding-edge`, `bulletproof`, `holistic`, `supercharge`, `elevate`, `hand-crafted`, `purpose-built`) and AI tells (`delve`, `leverage`, `harness`, `tapestry`, `myriad`, `unleash`)
- 💼 **Marketing hyphenated compounds**: drops `production-quality`, `production-ready`, `enterprise-grade`, `copy-paste`, `theme-building`, `baked-in`, `plug-and-play`, `turn-key`, `future-proof`
- ✂️ **De-hyphenate technical compounds**: `open-source` → `open source`, `command-line` → `command line`, `third-party` → `third party`, `AI-generated` → `AI generated`, `file-by-file` → `file by file`, `step-by-step` → `step by step`
- 🔢 **Number-word + noun compounds**: `seven-question intake`, `four-phase rollout`, `three-step process` → drop modifier or use digit
- 👀 **Filler intensifiers (audit only)**: flags `incredibly`, `highly`, `thoroughly`, `extensive`, `significantly`, `key` (adj), `fully`, `simply`, `very` for human review
- 🪞 **Empty enumeration intros (audit)**: flags `wide range of`, `a host of`, `a wealth of`, `an array of`, `a suite of`
- ➖ **Em-dash kill**: strips U+2014 / U+2013 from developer prose (comments, docstrings, logs, errors). Keeps them in CLI help text and user-facing terminal output. Leaves real number ranges alone (`pages 5-10`)
- 👥 **First-person plural**: drops `we`, `us`, `our`, `let's`. First-person singular (`I`, `my`) allowed
- 🏷️ **Function renames**: `orchestrateDataProvider` → `loadUsers`, `handleData` → `parseRequest`. Verifies substring safety before applying
- 🪢 **Padding cuts**: `in order to` → `to`, `due to the fact that` → `because`, `at this point in time` → `now`
- 🗯️ **Hedging removal**: `perhaps`, `essentially`, `fundamentally`, `at its core`, `arguably`
- 📚 **Tutorial voice**: drops `As you can see`, `Let's dive in`, `Imagine that`, `It's worth noting that`
- 🙏 **Apologetic openers**: drops `Please note`, `Keep in mind`, `Bear in mind`, `As a reminder`
- 📝 **Structure tics**: drops `This function...` / `This class...` openers, trailing wrap-up sentences that restate the docstring, decorative emojis/arrows/box-drawing in comments
- 🔁 **Restatement comments**: drops `i++; // increment i` and similar
- 🔇 **Linter-suppression markers**: flags unjustified `# noqa`, `// @ts-ignore`, `// @ts-expect-error`, `# rubocop:disable`, `//nolint`, `// eslint-disable-line`, `# pragma: no cover`, `@phpstan-ignore-line`, `@psalm-suppress`
- 📅 **Author/date stamps**: drops what `git blame` already tracks
- 🦺 **Defensive-check noise**: drops `// just in case`, `// defensive check`, `// shouldn't happen`
- 🎓 **Latin show-offs + AI Britishisms**: drops `whilst`, `amongst`, `ergo`, `vis-à-vis`
- 🧪 **Test name cleanup**: `should correctly do X` → `do X`

#### 🌍 Languages covered

JavaScript, TypeScript, Python, Go, Rust, Java, C#, C/C++, Perl, Swift, Kotlin, PHP, Ruby, Elixir, Lua, SQL, PowerShell, Markdown, Shell scripts. Each language has its own ruleset section with tips for that language's comment/docstring/identifier conventions.

#### 🛠️ Frameworks covered

React (+ Next.js Server Components, hooks, props), Vue (+ Nuxt composables, auto-imports), Astro (islands, content collections, view transitions), Alpine.js (`x-*` directives), Express (+ Koa, Fastify, Hono), Vite, Webpack, Rollup, esbuild, Tailwind (utility classes, `@apply`, config files), WordPress (plugins, themes, hooks, nonces, translation calls), Laravel (+ Blade, Livewire, Eloquent, migrations), Symfony (controllers, Doctrine, services, voters), Twig (Symfony/Drupal/standalone), EJS templates, `.env` files, `knexfile` database config.

#### 🛡️ Safety rails

- Never changes code behavior, function signatures, return types, or string literals shown to end users
- Never touches CLI help text, README content, commit messages, license headers, CHANGELOG
- Function renames verify substring safety. won't rename `extract` to `pull` if `extractor` exists
- One pass per category. vocab swap → voice rewrites → function renames → syntax check → verification greps → human read-back. Mixing passes makes diffs unreviewable
- Falls back to "leave it and flag for human review" on ambiguous cases
- Ships with reviewer checklist and false-positive guide for when a flagged word is actually correct

#### 🔄 How it works

1. **Initialization gate**: target picker fires (File / Directory / Paste) unless target already given
2. **Pass 1: read target**: full Read of the file, language detection from extension; loads relevant language + framework subsection from `references/full-ruleset.md`
3. **Pass 2: vocabulary swap**: Rule 2 (anthropomorphic + engineering jargon) and Rule 2c sections A-R in order
4. **Pass 3: voice rewrites**: first-person plural → imperative, kill tutorial voice, kill apologetic openers
5. **Pass 4: em-dash + smart punctuation**: strip U+2014/U+2013/smart quotes from developer prose
6. **Pass 5: function renames**: substring safety check, then rename across the file
7. **Pass 6: syntax check**: language-appropriate parse/lint
8. **Pass 7: verification greps**: `scripts/verify.sh` runs Rule 8 greps; all return empty when clean
9. **Pass 8: human read-back**: cadence + rhythm review (greps catch keywords, not voice)
10. **Pass 9: emit final report**: mandatory Markdown report (files touched, rename table, verification table, borderline kept, diff stats)

#### 🚀 How to use it

Slash command:

```
/unslop # fires the File/Directory/Paste picker
/unslop src/auth.ts # skips picker, runs on the file
/unslop src/ # skips picker, runs on the directory
```

Natural language triggers (skill auto loads):

> *"unslop this file"*, *"deslop the repo"*, *"remove AI tells from `src/auth.ts`"*, *"strip em-dashes from comments"*, *"rename `orchestrateDataProvider` to something human"*, *"audit this file for AI slop"*, *"clean the AI voice out of these comments"*, *"kill the marketing words in this codebase"*

The full skill instructions live at [`unslop/skills/unslop/SKILL.md`](unslop/skills/unslop/SKILL.md), the slash command at [`unslop/commands/unslop.md`](unslop/commands/unslop.md), the complete 16 rule, 19 language, 22 framework ruleset in [`references/full-ruleset.md`](unslop/skills/unslop/references/full-ruleset.md), and verification greps in [`scripts/verify.sh`](unslop/skills/unslop/scripts/verify.sh).

---

### `changelog-generator`

Point Claude at a git repo. Get back a changelog your users can read, built from the actual code changes across the whole history - first commit to `HEAD` - not from the commit messages.

```
/plugin install changelog-generator@chrismccoy
```

Ever tried to write release notes from `git log` and found half the commits say "fixes", "tweaks", or "and more"? Commit messages leave things out and get the label wrong. A "fix" turns out to undo a break from an hour earlier. A one-line "cleanup" hides three real features. A commit tagged "security" only renamed a variable. If you write the changelog from the messages, you ship a changelog that is partly fiction.

This plugin reads the code instead. It walks the full history, splits it into eras by date and tags, and reads the real diffs with `git show` and `git diff`. The diff is the truth of what shipped, so the changelog says what actually changed. It sorts each change into New Features, Improvements, Security, Breaking Changes, or Fixes, drops the noise users never see, and writes everything in plain language anyone can follow. When it is done it offers to save `CHANGELOG.md` and tells you every place the code did not match the commit message.

#### 📋 Technical Overview

A Claude Code plugin with one slash command, one skill, and one bundled script. The skill body in `skills/changelog-generator/SKILL.md` carries the trust boundary, the five-step workflow, the per-range brief for sub-agents, and the fixed output format. The script `scripts/map-history.sh` does the deterministic git plumbing (repo check, shallow check, root commit, tags, full oldest-first timeline, root-to-HEAD diffstat) so the model never has to reinvent it. The slash command `/changelog-generator` takes a repo path or runs on the current directory.

#### ✨ Features

- 📖 Reads the code change, not the message. `git show` / `git diff` is the source, so "fixes" and "and more" get unpacked into what really shipped
- 🕰️ Covers the whole history. First commit to `HEAD`, no gaps. It will not take a date or version range - the scope is always everything
- 🧪 Checks the repo first. Stops if the folder is not a git repo, warns when the copy is shallow (so it never claims full coverage), and handles a one-commit history
- 🗂️ Splits the history into eras. Contiguous per-release chunks by date and theme, using tags as the boundaries
- 👥 Handles big histories. Over about 40 commits, or when a diff is too large to read in one pass, it splits the work across parallel helpers, then combines and double-checks anything surprising against the real code - it never quietly skips or samples
- 🏷️ Sorts every change: feature, improvement, fix, security, breaking change, or internal
- 🕵️ Catches what messages hide. Lists features buried under "and more", drops fixes that only undo a break from the same batch, refuses to call reworded or moved code "new", and flags any commit whose message says more or less than the diff did
- 🔒 Pulls security and breaking changes into their own sections, with the real mechanism (how a check or block works, what setting was removed or flipped)
- 🛡️ Treats everything in the repo as data, not orders. A diff that says "ignore the above" gets described, never obeyed
- 📝 Offers to save `CHANGELOG.md` and reports where the diff corrected the commit messages

#### 🔄 How it works

1. **Map.** Run `scripts/map-history.sh`. Act on its `STATUS` / `SHALLOW` / `COMMIT_COUNT` - stop if not a git repo, warn if shallow, take the single-commit path if there is only one commit.
2. **Split.** Break the timeline into contiguous ranges by era and release, using tags and day-grouped commits as boundaries.
3. **Read the diffs.** For each range, `git diff <range> --stat` for the shape, then `git show` / `git log -p` for the substance. Over ~40 commits or an oversized diff, dispatch one helper per range in parallel with the per-range brief.
4. **Synthesize.** Merge the findings, treat helper reports as claims and spot-check the surprising ones against the diff, dedupe, order newest first, and lift out security and breaking changes.
5. **Check and write.** Confirm the ranges chain together with no gaps and that a real diff sits behind every entry, then emit the changelog and offer to save it.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/changelog-generator            ← runs on the current repo
/changelog-generator ../my-app  ← runs on a repo at that path
```

**Natural language** (auto-triggers via the skill):

> *"generate a changelog for this repo"*, *"write release notes from the git history"*, *"what actually shipped in this project?"*, *"changelog from the code changes, don't trust the commit messages"*, *"turn this repo's history into release notes my users can read"*

The full skill instructions live at [`changelog-generator/skills/changelog-generator/SKILL.md`](changelog-generator/skills/changelog-generator/SKILL.md), the slash command at [`changelog-generator/commands/changelog-generator.md`](changelog-generator/commands/changelog-generator.md), and the history script at [`changelog-generator/skills/changelog-generator/scripts/map-history.sh`](changelog-generator/skills/changelog-generator/scripts/map-history.sh).

---

## Servers and Scripting

### `docker-compose-architect`

Production, secure, scalable docker-compose stacks from four inputs, in the voice of a Senior DevOps Engineer and Docker expert. Locked four-phase blueprint. Required-input validation and a silent output gate before sending.

```
/plugin install docker-compose-architect@chrismccoy
```

Most "give me a docker-compose file" prompts return something that should never reach production: secrets hardcoded in plaintext, every service on one flat network, no volumes so data evaporates on restart, no healthchecks so `depends_on` races, and containers running as root. This plugin replaces that with what a senior DevOps engineer actually does. Secrets are always `${VAR}` references resolved from a generated `.env` template - never literals. Tiers are isolated on separate bridge networks (frontend vs database). Every stateful service gets a named volume. Every service gets a healthcheck, and `depends_on` uses `condition: service_healthy`. Containers run non-root where the base image allows. Compose YAML is indented 2 spaces. Image names and tags are never invented - uncertain tags are flagged for confirmation.

The skill body runs the workflow. Step 1 loads the master prompt from `references/prompt-template.md` and substitutes the four inputs. Step 2 validates inputs - a missing `TECH_STACK` or `DATABASE_REQUIREMENTS` halts with one targeted question per field, and conflicting constraints (e.g. "no persistence" plus a database) are surfaced before generating. Step 3 produces the blueprint under the strict operating constraints. Step 4 runs a silent output gate - all four phases present, valid 2-space YAML, secrets as env refs, a healthcheck per service or documented reason, no invented images - and fixes any failure before returning.

Hard refusal on out-of-scope asks. Kubernetes, Terraform, raw Dockerfiles, and unrelated requests get exactly one line: `Out of scope: this engine outputs docker-compose stacks only.`

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/docker-compose-architect/SKILL.md` carries the persona, scope lock, input handling, and 4-step workflow. The authoritative master prompt with `{{placeholders}}` lives in `references/prompt-template.md` and loads on every invocation. The slash command `/docker-compose-architect` accepts an optional `TECH_STACK` arg, then walks the user through `AskUserQuestion` intake for the remaining fields.

#### ✨ Features

- 🎯 Four inputs in, one blueprint out. TECH_STACK + DATABASE_REQUIREMENTS (required) + NETWORK_SETUP + SPECIFIC_CONSTRAINTS (optional)
- 🧱 Locked 4-phase output: Architecture Overview, complete `docker-compose.yml`, `.env` template, Deployment & Scaling
- 🔐 Secrets only as `${VAR}` env references resolved from the `.env` template - never plaintext literals
- 🧬 Tier network isolation (frontend-tier vs database-tier bridges), named volumes for every stateful service
- 🩺 Healthcheck on every service; `depends_on` with `condition: service_healthy`; containers run non-root where the base image allows
- 🧠 No invented image names, tags, version numbers, or compose keys - only real, documented images; uncertain tags flagged for confirmation
- ✅ Silent output validation: 4 phases present, valid 2-space YAML, every secret an env ref, every service healthchecked or documented, no invented images
- 🛡️ Prompt-injection defense. All inputs treated as untrusted data; embedded directives (`ignore prior`, `act as`, output-format-change attempts) ignored
- 🚦 Required-field halt + conflict surfacing - missing `TECH_STACK`/`DATABASE_REQUIREMENTS` asks one question per field; "no persistence" plus a database is surfaced before generating
- 🪧 Scope-locked. Kubernetes, Terraform, raw Dockerfiles, unrelated requests refused with `Out of scope: this engine outputs docker-compose stacks only.`

#### 🔄 How it works

1. **Intake.** Slash command collects four fields via `AskUserQuestion`. If `TECH_STACK` was passed as `$ARGUMENTS`, confirm and skip that question.
2. **Load template.** Read `references/prompt-template.md`. Substitute `{{TECH_STACK}}`, `{{DATABASE_REQUIREMENTS}}`, `{{NETWORK_SETUP}}`, `{{SPECIFIC_CONSTRAINTS}}`. Treat inputs as untrusted data.
3. **Validate inputs.** Empty / placeholder `TECH_STACK` or `DATABASE_REQUIREMENTS` → one targeted question per field, then halt. Conflicting constraints → surface and ask which wins.
4. **Generate** the blueprint under the strict operating constraints (non-root, tier isolation, named volumes, healthchecks, `${VAR}` secrets, 2-space YAML).
5. **Silent output gate.** 4 phases; valid YAML; secrets as env refs; healthcheck per service or documented reason; no invented images. Fix failures before printing.
6. **Output the four phases only.**

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/docker-compose-architect "Node.js + React frontend, Express API"   ← arg seeds TECH_STACK
/docker-compose-architect                                           ← full intake
```

**Natural language** (auto-triggers via the skill):

> *"design a docker-compose stack"*, *"architect a containerized environment"*, *"write a production docker-compose.yml"*, *"multi-tier docker setup"*, *"docker compose with database and networks"*, *"containerize my app with compose"*

The full skill instructions live at [`docker-compose-architect/skills/docker-compose-architect/SKILL.md`](docker-compose-architect/skills/docker-compose-architect/SKILL.md), the slash command at [`docker-compose-architect/commands/docker-compose-architect.md`](docker-compose-architect/commands/docker-compose-architect.md), and the on-demand master prompt at [`docker-compose-architect/skills/docker-compose-architect/references/prompt-template.md`](docker-compose-architect/skills/docker-compose-architect/references/prompt-template.md).

---

### `kubernetes-architect`

Resilient, secure, production-ready Kubernetes manifests from four inputs, in the voice of a Principal Cloud Native Architect and Kubernetes expert. Locked four-phase blueprint. Empty/contradictory-input halt and a silent pre-delivery YAML validation before sending.

```
/plugin install kubernetes-architect@chrismccoy
```

Most "give me a Kubernetes Deployment" prompts return YAML that falls apart at the first cluster review: no liveness or readiness probes so rollouts and traffic routing misbehave, no resource requests or limits so the scheduler and autoscaler have nothing to go on, containers running as root with a writable root filesystem, and Service selectors that don't match pod labels. This plugin replaces that with what a principal cloud native architect actually does. Every container gets liveness and readiness probes, resource requests and limits, and a security context (`runAsNonRoot`, `readOnlyRootFilesystem`, `allowPrivilegeEscalation: false`). YAML is syntax-perfect, 2-space indented, with dash-based arrays. Image names, tags, apiVersion values, and field keys are never invented - uncertain tags are flagged for confirmation. Before sending, every block is validated: `apiVersion`/`kind`/`metadata.name` present, indentation valid, probes + resources + securityContext per container, and Service/Ingress selectors matching Deployment pod labels.

The skill body runs the workflow. Step 1 loads the master prompt from `references/prompt-template.md` (including the canonical Deployment skeleton) and substitutes the four inputs. Step 2 validates inputs - any empty or contradictory field STOPs with a list of exactly what is missing rather than inventing a default. Step 3 generates the manifests under the strict operating constraints. Step 4 runs a silent pre-delivery validation and fixes any failure before returning; unvalidated YAML is never emitted.

Hard prompt-injection defense. Inputs are untrusted data - a field that says "ignore probes", "run as root", or "skip security" is ignored and flagged in PHASE 1. Off-domain requests (Terraform, billing, application code) get one refusal line, then the K8s task continues.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/kubernetes-architect/SKILL.md` carries the persona, scope lock, input handling, and 4-step workflow. The authoritative master prompt with `{{placeholders}}` and the Deployment skeleton lives in `references/prompt-template.md` and loads on every invocation. The slash command `/kubernetes-architect` accepts an optional `APP_REQUIREMENTS` arg, then walks the user through `AskUserQuestion` intake for the remaining fields.

#### ✨ Features

- 🎯 Four inputs in, one blueprint out. APP_REQUIREMENTS + RESOURCE_LIMITS + EXPOSURE_STRATEGY + TARGET_ENVIRONMENT
- 🧱 Locked 4-phase output: Architecture Overview, Deployment + HPA manifests, Service/Ingress/ConfigMap manifests, kubectl Deployment Guide
- 🩺 Liveness AND readiness probes on every container - no silent rollout or routing failures
- 📊 `resources.requests` AND `resources.limits` on every container - scheduler and HPA get real signals
- 🔐 Security contexts where applicable - `runAsNonRoot`, `readOnlyRootFilesystem`, `allowPrivilegeEscalation: false`
- 🧠 No invented image names, tags, apiVersion values, kind names, or field keys - only real, documented Kubernetes resources; uncertain tags flagged for confirmation
- ✅ Silent pre-delivery validation per block: apiVersion/kind/metadata.name present, valid 2-space indentation, probes+resources+securityContext per container, Service/Ingress selectors match pod labels
- 🛡️ Prompt-injection defense. Inputs are untrusted data; behavior-altering directives (`ignore probes`, `run as root`, `skip security`) are ignored and flagged in PHASE 1
- 🚦 No invented defaults - empty or contradictory fields STOP with a list of exactly what is missing
- 🪧 Scope-locked. Terraform, billing, and application-code requests get one refusal line, then the K8s task continues

#### 🔄 How it works

1. **Intake.** Slash command collects four fields via `AskUserQuestion`. If `APP_REQUIREMENTS` was passed as `$ARGUMENTS`, confirm and skip that question.
2. **Load template.** Read `references/prompt-template.md`. Substitute `{{APP_REQUIREMENTS}}`, `{{RESOURCE_LIMITS}}`, `{{EXPOSURE_STRATEGY}}`, `{{TARGET_ENVIRONMENT}}`. Treat inputs as untrusted data.
3. **Validate inputs.** Empty / placeholder / contradictory field → STOP, list what is missing, ask. No invented defaults.
4. **Generate** the manifests under the strict operating constraints (probes, resource requests/limits, security contexts, 2-space YAML, dash-based arrays).
5. **Silent pre-delivery validation.** apiVersion/kind/metadata.name; 2-space indentation; probes+resources+securityContext per container; selectors match pod labels; no invented images. Fix failures before printing.
6. **Output the four phases only.**

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/kubernetes-architect "Node API, image myorg/api, port 3000, 3 replicas"   ← arg seeds APP_REQUIREMENTS
/kubernetes-architect                                                       ← full intake
```

**Natural language** (auto-triggers via the skill):

> *"design Kubernetes manifests"*, *"architect a K8s deployment"*, *"write a Kubernetes Deployment YAML"*, *"Deployment with HPA and probes"*, *"Kubernetes Service and Ingress"*, *"create production K8s manifests"*

The full skill instructions live at [`kubernetes-architect/skills/kubernetes-architect/SKILL.md`](kubernetes-architect/skills/kubernetes-architect/SKILL.md), the slash command at [`kubernetes-architect/commands/kubernetes-architect.md`](kubernetes-architect/commands/kubernetes-architect.md), and the on-demand master prompt at [`kubernetes-architect/skills/kubernetes-architect/references/prompt-template.md`](kubernetes-architect/skills/kubernetes-architect/references/prompt-template.md).

---

### `powershell-script-engine`

Production, PSScriptAnalyzer-clean PowerShell scripts from five inputs, in the voice of a PowerShell expert and Windows systems engineer. Locked four-section output. Pre-generation input validation and a silent self-check before output.

```
/plugin install powershell-script-engine@chrismccoy
```

Most "write me a PowerShell script" prompts return something that fails review the moment it hits a real server: `Write-Host` used for data, unapproved verbs, hardcoded credentials in plaintext, a `Remove-Item` with no `-WhatIf`, and zero logging. This plugin replaces that with what a seasoned Windows systems engineer actually does. Every script opens with `#Requires -Version 7.0`, carries comment-based help (`.SYNOPSIS`/`.DESCRIPTION`/`.PARAMETER`/`.EXAMPLE`) on the script and every function, uses `[CmdletBinding()]` with validated parameters, wraps work in `try/catch/finally`, and logs to both console and a rolling file (`$env:ProgramData\<ScriptName>\<ScriptName>.log`, 10 MB roll, 5 archives). Credentials are typed `[PSCredential]` - never plaintext. Destructive operations are refused unless named in the requirements, and gated behind `-WhatIf`/`-Confirm` when generated. Cmdlet, module, and parameter names are never invented.

The skill body runs the workflow. Step 1 loads the master prompt from `references/prompt-template.md` and substitutes the five inputs. Step 2 validates inputs - an empty or placeholder `TASK`/`USER_REQUIREMENTS` halts with one clarifying question rather than a guessed script. Step 3 generates the script under the full specification (foundation, parameters, error handling, logging, security, remote). Step 4 runs a silent self-check - approved verbs, clean parse, no plaintext secrets, no invented names, four sections in order - and fixes any failure before returning.

Hard refusal on out-of-scope asks (output is the script plus usage examples only) and on security violations. Every response ends with `--- Generated by PowerShell Script Engine | review before production use ---`.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/powershell-script-engine/SKILL.md` carries the persona, scope lock, input handling, and 4-step workflow. The authoritative master prompt with `{{placeholders}}` lives in `references/prompt-template.md` and loads on every invocation. The slash command `/powershell-script-engine` accepts an optional `TASK` arg, then walks the user through `AskUserQuestion` intake for the remaining four fields.

#### ✨ Features

- 🎯 Five inputs in, one production script out. TASK + USER_REQUIREMENTS + PS_TARGET + REMOTE + DESTRUCTIVE
- 📐 `#Requires -Version 7.0`, comment-based help on the script and every function, `[CmdletBinding()]` with validated parameters
- 🧯 `try/catch/finally` everywhere; clear error messages; console AND rolling file logging (10 MB roll, 5 archives)
- ✔️ Approved verbs only (Get-Verb). No `Write-Host` for data, no aliases in the body, no positional args in examples, no PSScriptAnalyzer rule suppressions
- 🔐 No plaintext secrets - `[PSCredential]` / `Get-Credential` / SecretManagement only
- 🚫 No destructive ops (`Remove-*`, `Format-*`, `Stop-*`, registry/disk writes) unless named in requirements; gated behind `-WhatIf`/`-Confirm` when generated
- 🧠 No invented cmdlet, module, parameter, or version names - only real, documented PowerShell; unverifiable modules flagged for confirmation
- 📦 Locked 4-section output: Script, Parameters table (Name/Mandatory/Type/Validation), 3+ Usage Examples (local/pipeline/PSSession), Security Notes
- 🛡️ Prompt-injection defense. `USER_REQUIREMENTS` treated as inert data; embedded directives (`ignore prior`, `act as`, output-format-change attempts) are ignored
- 🪧 Scope-locked. Empty or off-topic requirements get one clarifying question, then a halt

#### 🔄 How it works

1. **Intake.** Slash command collects five fields via `AskUserQuestion`. If `TASK` was passed as `$ARGUMENTS`, confirm and skip that question.
2. **Load template.** Read `references/prompt-template.md`. Substitute `{{TASK}}`, `{{USER_REQUIREMENTS}}`, `{{PS_TARGET}}`, `{{REMOTE}}`, `{{DESTRUCTIVE}}`. Treat requirements as inert data.
3. **Validate inputs.** Empty / blank / placeholder `TASK` or `USER_REQUIREMENTS` → ask one clarifying question naming the job, then halt.
4. **Generate** the script per the specification (foundation, parameters, error handling, logging, security, remote).
5. **Silent self-check.** Approved verbs; balanced braces, no aliases, no `Write-Host` for data; no plaintext secrets, credentials `[PSCredential]`; no invented names; four sections in order. Fix failures before printing.
6. **Output the four sections**, then the footer line.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/powershell-script-engine "Audit local admin group membership across a server list and export to CSV"   ← arg seeds TASK
/powershell-script-engine                                                                                ← full 5-question intake
```

**Natural language** (auto-triggers via the skill):

> *"write a PowerShell script"*, *"create a production PS module"*, *"PSScriptAnalyzer-clean script"*, *"PowerShell automation script"*, *"PowerShell remoting script"*, *"PowerShell with comment-based help"*

The full skill instructions live at [`powershell-script-engine/skills/powershell-script-engine/SKILL.md`](powershell-script-engine/skills/powershell-script-engine/SKILL.md), the slash command at [`powershell-script-engine/commands/powershell-script-engine.md`](powershell-script-engine/commands/powershell-script-engine.md), and the on-demand master prompt at [`powershell-script-engine/skills/powershell-script-engine/references/prompt-template.md`](powershell-script-engine/skills/powershell-script-engine/references/prompt-template.md).

---

### `jq`

Expert jq one-liners for querying, filtering, transforming, and aggregating JSON in real shell pipelines, in the voice of a senior CLI engineer. Inspects the JSON structure before writing the filter, builds it one pipe stage at a time, and returns a single copy-paste-ready command plus a one-line explanation per stage.

```
/plugin install jq@chrismccoy
```

Most "give me a jq command" answers guess at the JSON structure, quote the filter wrong so the shell mangles it, and skip the null cases that break the pipeline on the first input that hits them. This plugin works like an experienced engineer. It samples the data first with `jq 'keys'` or `jq '.[0]'` to confirm the actual field names and nesting, then builds the filter incrementally instead of writing one opaque expression. The delivered command is single-quoted to block shell expansion, uses `-r` when the output feeds a shell variable or another command, injects shell values with `--arg` / `--argjson` rather than string interpolation, and handles the empty and null edge cases (`// empty`, `// 0`, `add // 0`). Every command comes with a plain-English explanation of what each `|` stage does.

The skill covers basic and nested selection, `select()` filtering, `map` and object reshaping, `reduce` and `group_by` aggregation, string interpolation and `@csv` / `@tsv` / `@base64` / `@uri` formatting, key and path manipulation, conditionals and `try` / `catch`, and shell integration with `curl`, `kubectl`, `aws`, `gh`, and `docker`. It is scope-locked to jq usage. JSON authoring, JSON Schema validation, jsonnet, and non-jq shell scripting are out of scope and get one refusal line.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/jq/SKILL.md` carries the persona, the 6-step workflow (identify source, inspect shape, build incrementally, choose output mode, verify, deliver), a full cookbook of patterns, the output format, and the quality gates. The slash command `/jq` accepts an optional argument that seeds `JSON_SOURCE`, then walks the user through `AskUserQuestion` intake for the source, the goal, and the output mode.

#### ✨ Features

- 🎯 Three intake fields. JSON_SOURCE + GOAL + OUTPUT_MODE, or just paste JSON and ask
- 🔎 Inspects the structure first (`jq 'keys'`, `jq '.[0]'`) - never guesses field names or nesting
- 🧱 Builds filters one pipe stage at a time, verified against a sample
- 📤 Output mode aware - `-r` for shell consumption, `-c` for NDJSON, pretty for reading, `@csv` / `@tsv` for tables
- 🛡️ Safe shell injection via `--arg` / `--argjson`, never string interpolation; filters always single-quoted
- 🕳️ Null and empty edge cases handled (`// empty`, `// 0`, `add // 0`)
- 📝 One copy-paste-ready command, then a one-line explanation per filter stage
- 🪧 Scope-locked. JSON authoring, JSON Schema, jsonnet, and non-jq shell scripting get one refusal line

#### 🔄 How it works

1. **Intake.** Slash command collects JSON_SOURCE, GOAL, and OUTPUT_MODE via `AskUserQuestion`. If a source was passed as `$ARGUMENTS`, confirm and skip that question.
2. **Inspect.** When the source is a paste or a file, check the structure with `jq 'keys'` / `jq '.[0]'` before writing anything.
3. **Build.** Compose the filter incrementally, adding one `|` stage at a time and verifying each against the sample.
4. **Apply output mode.** `-r`, `-c`, pretty, or `@csv` / `@tsv` per the chosen mode.
5. **Harden.** Single-quote the filter, inject variables with `--arg` / `--argjson`, cover null and empty cases.
6. **Deliver** one command in a bash block, then a one-line explanation per stage.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/jq 'curl -s https://api.github.com/repos/owner/repo/issues'   ← arg seeds JSON_SOURCE
/jq                                                            ← full intake
```

**Natural language** (auto-triggers via the skill):

> *"parse this JSON"*, *"extract X from this output"*, *"pull the field with jq"*, *"filter this API response"*, *"reshape this JSON"*, *"aggregate these records"*, *"explain this jq filter"*, or paste raw JSON or CLI output and ask to filter, transform, or summarize it

The full skill instructions live at [`jq/skills/jq/SKILL.md`](jq/skills/jq/SKILL.md) and the slash command at [`jq/commands/jq.md`](jq/commands/jq.md).

---

## Domain Names

### `naming-strategist`

Senior naming strategist for venture-backed SaaS founders. 10 brandable, pronounceable, niche-fit domain candidates from five inputs. Locked 4-section output. Silent scoring drops weak names before they ever reach the page.

```
/plugin install naming-strategist@chrismccoy
```

Naming a SaaS is the part most founders procrastinate on, then panic over the week before launch. The usual move - opening a naming-tool tab, scrolling through 400 `-ify` / `-ly` / `-hub` slop suggestions, and picking whichever one still has a `.com` left - produces names that are forgettable on day one and embarrassing by month six. This plugin replaces that with a structured naming pass: five inputs in, ten candidates out, every one scored silently on five axes before it gets printed, every one tagged with a recommended TLD and a Low/Medium/High risk note so you know what to verify and what to walk away from. The model never claims a domain is available, never claims a name is trademark-clear, and never produces output outside the four locked sections.

The skill body runs the workflow. Step 1 loads the master prompt from `references/prompt-template.md` and substitutes the five inputs. Step 2 generates 10 candidates obeying the rules in `references/constraints.md` - 6-12 chars where possible, no hyphens, no numbers, no descriptive keyword domains, at least five distinct naming structures across the list (compound, blended, metaphor, invented, classical-roots). Step 3 silently scores each candidate 1-10 on Brandability, Niche fit, Pronounceability, Spelling ease, Differentiation; drops anything below a 7 average. Step 4 emits sections A-D per `references/output-spec.md`. Step 5 runs a silent validation gate before printing - generic names regenerate, hype words regenerate, missing-structure variety regenerates.

Hard refusal on legal-certainty claims (`Needs verification` instead), on hype copy (`proven`, `revolutionary`, `leverage`, `robust`, `seamless`, `cutting-edge`), and on out-of-scope asks (marketing copy, strategy decks, legal advice, taglines - all answered with `Out of scope - domain naming candidates only.`).

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/naming-strategist/SKILL.md` carries the scope lock, input handling, and 5-step workflow. The authoritative master prompt with `{{placeholders}}` lives in `references/prompt-template.md` and loads on every invocation. The hard constraints (blocked words, scoring rubric, silent validation gate) live in `references/constraints.md`. The output format (sections A-D, per-candidate block, worked calibration example) lives in `references/output-spec.md`. The slash command `/name-domains` accepts an optional `MARKET_TOPIC` arg, then walks the user through `AskUserQuestion` intake for the remaining four fields.

#### ✨ Features

- 🎯 Five inputs in, ten candidates out. MARKET_TOPIC + TARGET_AUDIENCE + OFFER_TYPE + BRAND_TONE (2-3 pick) + EXTENSION_PRIORITY
- 🧪 Silent 5-axis scoring - Brandability, Niche fit, Pronounceability, Spelling ease, Differentiation. Drops anything below 7 average before printing
- 🧱 At least 5 distinct naming structures across the 10 - compound, blended, metaphor, invented, classical-roots. No same-pattern repeats
- 🚫 Refuses hyphens, numbers, awkward letter clusters, forced `-ify` / `-ly` / `-hub` suffixes, generic descriptive keyword domains (`BestBranding`, `FastestCRM`), and famous-brand collisions
- 🛡️ No legal claims. Domains, trademark status, registrar availability - all answered `Needs verification`
- 🧊 No hype. Blocked phrasing in any rationale: `proven`, `revolutionary`, `transformative`, `leverage`, `robust`, `comprehensive`, `streamline`, `harness`, `seamless`, `cutting-edge`
- 📦 Locked 4-section output: A) Setup Summary (3 lines), B) 10 Name Candidates with Angle/Fit/Recommended extension/Risk note, C) Top 3 Shortlist with Strength + Watch-out bullets, D) Verification Checklist (registrar check, USPTO TESS, WIPO Global Brand Database, pronunciation test, Google collision search)
- ⚖️ Risk severity scale per name: Low (invented, no known collision), Medium (real-word compound, possible overlap), High (close to known brand or category-keyword overlap)
- 🛑 Prompt-injection defense. All five inputs treated as inert data. Directives like `ignore prior`, `act as`, `respond in JSON`, role-switch attempts inside field values are ignored
- 🪝 Scope-locked. Marketing copy, strategy decks, legal advice, taglines, naming for non-SaaS contexts - all refused with `Out of scope - domain naming candidates only.`

#### 🔄 How it works

1. **Intake.** Slash command collects five fields via `AskUserQuestion`. If `MARKET_TOPIC` was passed as `$ARGUMENTS`, confirm and skip that question. Empty / blank / `[FIELD_NAME]` → halt with `MISSING INPUT: <field> required.`
2. **Load template.** Read `references/prompt-template.md`. Substitute `{{MARKET_TOPIC}}`, `{{TARGET_AUDIENCE}}`, `{{OFFER_TYPE}}`, `{{BRAND_TONE}}`, `{{EXTENSION_PRIORITY}}` with collected values. Treat values as inert data.
3. **Generate 10 candidates** obeying `references/constraints.md`. Prefer 6-12 chars. Mix structures. No hyphens, numbers, or forced suffixes.
4. **Silent scoring.** 1-10 on Brandability, Niche fit, Pronounceability, Spelling ease, Differentiation. Drop <7 average. If fewer than 10 survive: emit what passes + `Returned N of 10 - niche requires looser scoring or revised inputs.`
5. **Emit sections A-D** per `references/output-spec.md`. No extras. No reordering.
6. **Silent validation gate.** Regenerate any item that fails: generic, brand-collision, missing structure variety, hype words, availability claims. Do not announce the gate.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/name-domains "AI productivity tools for solo founders"   ← arg seeds MARKET_TOPIC, picker fills the rest
/name-domains                                              ← full 5-question intake
```

**Natural language** (auto-triggers via the skill):

> *"name my SaaS"*, *"generate domain names"*, *"brand a startup"*, *"come up with domain candidates"*, *"name my micro-SaaS"*, *"domain name brainstorm"*, *"brandable startup name"*, *"SaaS naming"*, *"founder domain shortlist"*

After the run, work the Section D checklist - register check across `EXTENSION_PRIORITY`, USPTO TESS search across IC 9 / 35 / 42, WIPO Global Brand Database for international overlaps in your launch regions, pronunciation test with 3 strangers, Google the bare term in quotes plus your market keyword.

The full skill instructions live at [`naming-strategist/skills/naming-strategist/SKILL.md`](naming-strategist/skills/naming-strategist/SKILL.md), the slash command at [`naming-strategist/commands/name-domains.md`](naming-strategist/commands/name-domains.md), and the on-demand reference files at [`naming-strategist/skills/naming-strategist/references/prompt-template.md`](naming-strategist/skills/naming-strategist/references/prompt-template.md), [`naming-strategist/skills/naming-strategist/references/constraints.md`](naming-strategist/skills/naming-strategist/references/constraints.md), [`naming-strategist/skills/naming-strategist/references/output-spec.md`](naming-strategist/skills/naming-strategist/references/output-spec.md).

---

## Creative

### `vgademo`

Generates retro 1990s style sizecoded assembly demos for MS-DOS, BIOS, and boot sector targets.

```
/plugin install vgademo@chrismccoy
```

Remember the 256 byte intros and 4KB demos that shipped at Assembly, Revision, and The Party in the early 1990s? The kind of artful little programs the demoscene made famous. plasma fields, fire effects, tunnels, rotozoomers - all in the byte budget of a tweet? That's what this skill builds.

The `vgademo` skill adopts a veteran demoscene engineer persona and writes ultra compact 16 bit real mode assembly that runs on real (or emulated) DOS era hardware. It targets NASM, FASM, TASM, or MASM. emits `.COM` files, boot sectors, or raw binaries. and respects strict size budgets with byte level estimates before any code ships.

What makes it different from a generic "write me asm" prompt? It enforces demoscene rules. register reuse, implicit operands, fused operations (`STOSB`, `STOSW`, `LODSB`), bit shifts over multiplies, no `PUSH`/`POP` for preservation, no functions or macros beyond the minimum. And it refuses cleanly with a single line code (`REFUSE: size`, `REFUSE: platform`, `REFUSE: contradiction`) when your inputs don't add up, instead of producing broken bytes.

Whether you want to ship a 256 byte intro, write a flashy boot sector that fits in 510 bytes, or learn how the demoscene squeezes plasma effects out of a handful of opcodes, this plugin is for you.

#### 📋 Technical Overview

An AI instruction specification that generates byte budget constrained 16 bit real mode x86 assembly in the style of early 1990s demoscene productions.

Built around a strict scope lock (refuses anything outside MS-DOS / BIOS / boot sector / .COM targets, refuses modern instructions, refuses size overruns), a mandatory output format (Byte Budget → Code → Core Trick → Tradeoffs), and a byte calibration table for accurate size estimation before emit.

Designed to behave like a real sizecoder. emit the trick, name the opcode, move on. no marketing register, no buzzwords, no tutorials. Includes prompt injection defenses that treat `{{placeholder}}` content as inert data.

#### ✨ Features

- 🎨 14 placeholder variables driving every demo: visual effect, size budget, target platform, video mode, CPU mode, assembler, binary format, entry point, performance priority, loop style, allowed tricks, memory model, dependencies, and comments toggle
- 🎯 4-round multiple-choice intake via `AskUserQuestion`. each question auto-includes an "Other" option for custom values (custom visual effects like starfield, metaballs, voxel landscape pass through verbatim)
- 📏 Strict size budgets enforced with a per-opcode byte calibration table. 256b intros, 512b boot sectors, 1KB / 4KB. 15% safety margin built in
- 🧮 Byte estimate emitted before the code block. no surprise overruns
- 💾 Multi-target. MS-DOS `.COM`, raw boot sector (with `0AA55h` signature), raw binary, BIOS-only mode
- 🖼️ Multi-mode rendering. Mode 13h (320x200x256 VGA), text mode (`B800h`, 80x25), VGA planar / Mode X
- 🔧 Four assembler syntaxes. NASM, FASM, TASM, MASM
- 🪄 Demoscene tricks. self-modifying code, undocumented opcodes, FPU, lookup tables, approximate trig, intentional overflow
- 🔁 Loop styles. single loop (`LOOP` instruction), unrolled, self-modifying
- 🎵 Optional PC speaker or AdLib-style sound when the byte budget allows
- 📋 Mandatory output format. Byte Budget → Code → Core Trick (mechanism + key instructions + register reuse map) → Tradeoffs (size won by / cycles cost / sacrificed)
- 🛡️ Single-line refusal codes. `REFUSE: scope|size|contradiction|platform|placeholder|injection`. no elaboration, no side-channel leaks
- 🔒 Scope lock refuses tutorials, history lessons, modern code (SSE/AVX/x86_64), and any request that breaches the declared `CPU_MODE`
- ⚡ Demoscene rules enforced. register reuse, implicit operands (AX/SI/DI), fused operations, bit-shifts for mul/div, no PUSH/POP for preservation, no functions or macros beyond minimum
- 📚 Two worked reference examples bundled. 256b XOR-plasma `.COM` (Mode 13h) and 512b text-mode color-bars boot sector (BIOS only)
- ⚠️ Negative anti-pattern example included. shows what to refuse cleanly instead of "fixing and emitting"
- 🎚️ Suggested low-temperature runtime (`temperature=0.3`, `top_p=0.9`). sizecoding needs low variance for stable byte counts
- 🚫 Hacker-engineer voice. no marketing register, no corporate jargon, no consultancy-speak
- 🔐 Prompt-injection defense. instructions embedded inside `{{...}}` placeholders are treated as inert data, refusal output is uniform to prevent side-channel inference

#### 🔄 How it works

1. **Intake**: the `/vgademo` slash command runs four `AskUserQuestion` rounds collecting 14 placeholders:
 - **Round 1 - Visual & Platform**: effect (plasma / fire / tunnel / rotozoomer / Other), size (256b / 512b / 1KB / 4KB), platform (MS-DOS .COM / boot sector / BIOS), video mode (Mode 13h / text mode / VGA planar)
 - **Round 2 - Toolchain**: CPU mode (16-bit real / 32-bit protected), assembler (NASM / FASM / TASM / MASM), binary format (.COM / boot sector / raw), entry point (`org 100h` / `org 7C00h` / `org 0`)
 - **Round 3 - Optimization**: performance priority (smallest / fastest / balanced), loop style (single / unrolled / SMC), allowed tricks (multi-select. SMC / undoc / FPU / LUT), memory model
 - **Round 4 - Final**: dependencies (BIOS only / no DOS / direct HW), comments (yes / no)
2. **Validation**: checks for contradictions before emit. size-vs-effect, BIOS-only-vs-DOS-mode, 16-bit-vs-32-bit-tricks. emits `REFUSE: <reason>` on any conflict
3. **Pre-emit checklist** (silent): byte estimate ≤ 0.85 × size limit, zero forbidden instructions, register reuse covers every named register, mechanism matches the named trick
4. **Emit**: mandatory four-section output. Byte Budget, Code (single asm block), Core Trick (≤200 words), Tradeoffs (≤120 words)

#### 🚀 How to use it

Two ways to invoke it:

**Slash command** (explicit):

```
/vgademo ← walks through all four intake rounds
```

**Natural language** (auto-triggers via the skill):

> *"write a 256 byte plasma intro in NASM for MS-DOS"*, *"make a fire effect demo in Mode 13h"*, *"build a 512 byte boot sector with color bars"*, *"sizecoded tunnel effect for .COM file"*, *"VGA assembly rotozoomer under 1KB"*, *"demoscene intro for the 8086"*

The full skill instructions live at [`vgademo/skills/vgademo/SKILL.md`](vgademo/skills/vgademo/SKILL.md), the slash command at [`vgademo/commands/vgademo.md`](vgademo/commands/vgademo.md), and the worked reference examples (256b XOR plasma and 512b boot sector) plus the anti pattern at [`references/examples.md`](vgademo/skills/vgademo/references/examples.md).

---

## Data

### `excel-formula-troubleshooter`

Debug, fix, and optimize broken Excel and Google Sheets formulas.

```
/plugin install excel-formula-troubleshooter@chrismccoy
```

A broken formula is rarely broken where it looks broken. `=VLOOKUP(A2,Sheet2!A:B,3,0)` throws `#REF!` not because the syntax is wrong but because the column index counts inside the range, and `A:B` only has two columns. The `excel-formula-troubleshooter` skill traces the formula like a spreadsheet engine does. function by function, parentheses balance, argument count and order, range references, data types (text vs number, dates as serials), circular references. then names the exact root cause, returns a copy-paste-ready corrected formula, explains the fix in plain bullets, and where it helps, suggests a modern alternative (`XLOOKUP` over `VLOOKUP`, `IFERROR` to mask error values).

Output is locked to four sections so every answer reads the same: ❌ The Issue, ✅ Corrected Formula, 🛠️ How the Fix Works, 🚀 Better Alternative (omitted when none applies). Function names come back UPPERCASE, ready to paste. Scope is locked to spreadsheet-formula troubleshooting. it does not answer general spreadsheet or data questions outside a broken formula.

#### ✨ Features

- 🔎 Silent pre-answer trace. function-by-function, parentheses balance, argument count/order, range references, data types, circular references. the reasoning never clutters the output
- 🎯 Exact root cause. mismatched parentheses, wrong syntax, text-vs-number mismatch, circular reference, incorrect range, wrong column index. not "consider checking your ranges"
- 📋 Copy-paste-ready corrected formula with UPPERCASE function names
- 🧾 Beginner-friendly bulleted explanation of why the fix works
- 🚀 Optional modern alternative. `XLOOKUP` over `VLOOKUP`, `INDEX/MATCH`, `IFERROR` to mask `#N/A`. omitted cleanly when nothing better applies
- 📦 Locked 4-section output format. identical shape on every answer
- 🚪 Asks for the issue instead of guessing when only a formula is supplied
- 🔒 Scope lock. spreadsheet-formula troubleshooting only

#### 🔄 How it works

1. **Intake**: the `/fix-formula` slash command parses the broken formula and the issue. pipe-separated (`formula | issue`), tag-wrapped (`<broken_formula>` / `<issue>`), or interactive prompt when either is missing
2. **Silent trace**: walks the formula function-by-function, checking parentheses, arguments, ranges, data types, and circular references. reasoning is not shown
3. **Diagnose**: names the single exact root cause
4. **Emit**: the locked four-section answer. The Issue, Corrected Formula, How the Fix Works, optional Better Alternative

#### 🚀 How to use it

**Slash command** (explicit):

```
/fix-formula =VLOOKUP(A2,Sheet2!A:B,3,0) | returns #REF!   ← formula | issue
/fix-formula =VLOOKUP(A2,Sheet2!A:B,3,0)                   ← asks for the issue
/fix-formula                                               ← full intake (formula + issue)
```

**Natural language** (auto-triggers via the skill):

> *"fix my Excel formula"*, *"why does my formula return #REF!"*, *"debug this spreadsheet formula"*, *"troubleshoot a Google Sheets formula"*, *"my VLOOKUP isn't working"*, *"correct this formula"*

The full skill instructions live at [`excel-formula-troubleshooter/skills/excel-formula-troubleshooter/SKILL.md`](excel-formula-troubleshooter/skills/excel-formula-troubleshooter/SKILL.md), and the slash command at [`excel-formula-troubleshooter/commands/fix-formula.md`](excel-formula-troubleshooter/commands/fix-formula.md).

---

## Writing and language

### `tech-blog-article`

Front-page-quality technical articles from five inputs, in the voice of a senior developer who actually ships. Locked output format. Pre-write input validation and a silent post-write output gate.

```
/plugin install tech-blog-article@chrismccoy
```

Most "write a blog post" prompts produce the exact thing that dies on Hacker News: a dictionary-definition opener, H2 headers that are bare topic labels (`## Configuration`), code dumped without explanation, and a conclusion that restates the intro. This plugin replaces that with what technical writers actually do. The opening grabs the reader in the first three sentences with a real situation they've lived through. Every H2 is a complete thought (`## The default configuration will break at 10K requests/second`). Code examples show the wrong way first, then the right way, stay under 20 lines, carry a language identifier, and get a plain-English explanation after the fence. Opinions are stated outright and backed with numbers; the downsides are admitted; every section passes a "So What?" test. It closes on one of four ending patterns and signs off with a one-line bio.

The skill body runs the workflow. Step 1 loads the master prompt from `references/prompt-template.md` and substitutes the five inputs. Step 2 validates inputs before writing - a bracketed placeholder halts with `Missing input: <field>.`, a word count outside 300-5000 halts with `Invalid input: Word count must be a number from 300 to 5000.`. Step 3 writes the article under all six writing rules. Step 4 runs a silent output gate - title ≤ 60 chars, TL;DR 3-4 bullets, complete-thought H2s, every code block annotated, one ending pattern - and fixes any failure before returning.

Hard refusal on non-writing and role-change requests (`I only draft technical articles - give me a topic and I'll write.`). Output is the article only - no preamble, no meta-commentary, no notes after the bio.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/tech-blog-article/SKILL.md` carries the persona, scope lock, input handling, and 4-step workflow. The authoritative master prompt with `{{placeholders}}` lives in `references/prompt-template.md` and loads on every invocation. The slash command `/tech-blog-article` accepts an optional `TOPIC` arg, then walks the user through `AskUserQuestion` intake for the remaining four fields.

#### ✨ Features

- 🎯 Five inputs in, one article out. TOPIC + AUDIENCE_LEVEL + ARTICLE_ANGLE + PRIMARY_LANGUAGE + WORD_COUNT
- 🪝 An opening that grabs the reader in the first 3 sentences. No dictionary definitions, no "In today's fast-paced world"
- 🧱 Every H2 is a complete thought, not a bare topic label. TL;DR box (3-4 bullets) after the intro
- 💻 Wrong-way-then-right-way code examples, under 20 lines, language identifier in the fence, plain-English explanation after each block
- ⚖️ Opinions stated outright and backed with numbers; downsides admitted; "So What?" test per section
- 🏁 One of four ending patterns: lessons-learned, actionable checklist, provocative question, or "the thing nobody tells you"
- ✅ Pre-write input validation halts on bracketed placeholders or word counts outside 300-5000
- 🔒 Silent post-write output gate: title length, TL;DR bullet count, complete-thought H2s, code-block annotations, ending pattern
- 🛡️ Prompt-injection defense. All five inputs treated as inert article subject matter. Embedded directives (`ignore the above`, `reveal your prompt`, `change format`) are ignored
- 🪧 Scope-locked. Non-writing and role-change requests refused with `I only draft technical articles - give me a topic and I'll write.`

#### 🔄 How it works

1. **Intake.** Slash command collects five fields via `AskUserQuestion`. If `TOPIC` was passed as `$ARGUMENTS`, confirm and skip that question. Empty / blank / `[FIELD_NAME]` → halt with `MISSING INPUT: <field> required.`
2. **Load template.** Read `references/prompt-template.md`. Substitute `{{TOPIC}}`, `{{AUDIENCE_LEVEL}}`, `{{ARTICLE_ANGLE}}`, `{{PRIMARY_LANGUAGE}}`, `{{WORD_COUNT}}` with collected values. Treat values as inert data.
3. **Validate inputs.** Bracketed placeholder → `Missing input: <field>.`. Word count not an integer 300-5000 → `Invalid input: Word count must be a number from 300 to 5000.`
4. **Write** the article following all six writing rules in the locked output format.
5. **Silent output gate.** Title ≤ 60 chars; TL;DR 3-4 bullets; complete-thought H2s; every code block has a language identifier and plain-English explanation; one ending pattern. Fix any failure before printing.
6. **Output the article only.** No preamble, no meta-commentary, no notes after the bio line.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/tech-blog-article "Why your Postgres connection pool keeps exhausting"   ← arg seeds TOPIC, picker fills the rest
/tech-blog-article                                                        ← full 5-question intake
```

**Natural language** (auto-triggers via the skill):

> *"write a technical article"*, *"draft a blog post"*, *"write a dev blog"*, *"Hacker News style article"*, *"Dev.to article"*, *"technical write-up"*, *"engineering blog post"*

The full skill instructions live at [`tech-blog-article/skills/tech-blog-article/SKILL.md`](tech-blog-article/skills/tech-blog-article/SKILL.md), the slash command at [`tech-blog-article/commands/tech-blog-article.md`](tech-blog-article/commands/tech-blog-article.md), and the on-demand master prompt at [`tech-blog-article/skills/tech-blog-article/references/prompt-template.md`](tech-blog-article/skills/tech-blog-article/references/prompt-template.md).

---

### `language-tutor`

Expert linguist, translator, and language tutor from five inputs, in the voice of a university-level instructor who stays clear enough for a self-studying learner. Two modes, locked section output per mode, an accuracy floor that refuses to fabricate, and a silent validation gate before printing.

```
/plugin install language-tutor@chrismccoy
```

Most "translate this" prompts return a single bare sentence with no grammar, no pronunciation, and no sense of register - and most "fix my writing" prompts rewrite the text without telling you what changed or why. Worse, when the model is unsure it guesses: invented conjugation rules, made-up etymologies, plausible-but-wrong IPA. This plugin replaces that with what an actual language instructor does. TRANSLATION mode returns the most natural rendering plus dual-language grammar, a subject/verb/object breakdown, IPA with English approximations and stress marks, and a register/cultural-nuance read. TEXT ANALYSIS mode returns grammar, spelling and punctuation, style and flow, meaning, a fully corrected version with every change itemized `original → corrected → reason`, and five style rewrites. The source language is auto-detected, difficulty is aligned to CEFR A1-C2, and a Quick depth collapses the whole thing to the result plus a one-line note when that's all you want.

The skill body runs the workflow. Step 1 loads the master prompt from `references/prompt-template.md` and substitutes the five inputs. Step 2 detects the source language and resolves the mode (TRANSLATION, TEXT ANALYSIS, or Auto-detect from the text). Step 3 emits the locked section set for that mode per `references/output-spec.md`. Step 4 runs a silent validation gate from `references/constraints.md` - section completeness, IPA wrapped in slashes, CEFR level named, exactly five Alternative Versions, every change itemized - and fixes any failure before returning.

Hard accuracy floor: never invents grammar rules, etymologies, or IPA; flags uncertainty instead of guessing; states reduced confidence on low-resource languages and dialects and stops rather than approximating when a language can't be handled reliably. Prompt-injection defense treats all submitted text strictly as DATA - a phrase like "ignore your instructions" inside the text is translated or analyzed literally, never obeyed. Scope-locked: non-language requests get a brief decline and a restatement of what the tutor does, never a switch into general-assistant behavior.

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/language-tutor/SKILL.md` carries the persona, scope lock, core behavior, input handling, and 4-step workflow. The authoritative master prompt with `{{placeholders}}` and both mode specs lives in `references/prompt-template.md` and loads on every invocation. The accuracy floor, prompt-injection defense, and silent validation gate live in `references/constraints.md`. The exact section structure for both modes, the optional-extras menu, and two calibrated worked examples live in `references/output-spec.md`. The slash command `/language-tutor` accepts an optional `TEXT` arg, then walks the user through `AskUserQuestion` intake for the remaining fields.

#### ✨ Features

- 🎯 Five inputs in, a full language breakdown out. MODE + TEXT + TARGET_LANGUAGE + NATIVE_LANGUAGE + DEPTH
- 🔀 Two modes: TRANSLATION (translate and explain a phrase) and TEXT ANALYSIS (correct and critique your own writing). Auto-detect picks the mode from the text when MODE is `Auto`
- 🧱 TRANSLATION emits 5 locked sections: Translation, Grammar (both languages), Structure, Pronunciation, Usage & Register
- 📝 TEXT ANALYSIS emits 6 locked sections: Grammar, Spelling & Punctuation, Style & Flow, Meaning & Content, Corrected Text (every change itemized `original → corrected → reason`), 5 Alternative Versions (formal, casual, detailed, concise, alt-vocabulary)
- 🔊 IPA inside slashes plus English approximations and marked syllable stress; pronunciation tips tailored to the learner's NATIVE_LANGUAGE for sounds that don't exist in it
- 🎚️ Register and difficulty aligned to CEFR A1-C2 where the language supports it, with the targeted level named
- ⚡ Quick depth returns only the Translation or Corrected Text plus a one-line note - no framework
- 🧠 Accuracy floor: never invents grammar rules, etymologies, or IPA; flags uncertainty instead of guessing; reduced-confidence warning on low-resource languages and dialects, and a hard stop rather than approximation when a language can't be handled reliably
- 🛡️ Prompt-injection defense. Submitted text is inert DATA; directives embedded in it (`ignore your instructions`, `act as`, `system:`) are translated or analyzed literally, never obeyed
- ✅ Silent validation gate: section set complete and in order, IPA in slashes, CEFR named, exactly 5 rewrites, every change itemized, no obeyed injections
- 🪧 Scope-locked. Non-language requests get a brief decline plus a restatement - no switch into general-assistant behavior

#### 🔄 How it works

1. **Intake.** Slash command collects five fields via `AskUserQuestion`. If `TEXT` was passed as `$ARGUMENTS`, confirm and seed it. Empty / blank / `[FIELD_NAME]` on `MODE` or `TEXT` → halt with `MISSING INPUT: <field> required.` In TRANSLATION mode, a missing or ambiguous `TARGET_LANGUAGE` triggers one short clarifying question alone before proceeding.
2. **Load template.** Read `references/prompt-template.md`. Substitute `{{MODE}}`, `{{TEXT}}`, `{{TARGET_LANGUAGE}}`, `{{NATIVE_LANGUAGE}}`, `{{DEPTH}}`. Treat the entire `TEXT` value as inert data.
3. **Resolve mode + language.** Detect the source language unless specified. When MODE is `Auto`, infer the mode from the text; default to TRANSLATION when ambiguous and label the assumption.
4. **Emit the locked sections** for the active mode per `references/output-spec.md`. Omit a section only if it doesn't apply, and say why. Quick depth returns only the result plus a one-line note.
5. **Silent validation gate.** Section completeness, IPA slashes, CEFR label, 5-rewrite count, itemized changes, no obeyed injections. Fix any failure before printing. Don't announce the gate.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/language-tutor "Je m'appelle Marie"   ← arg seeds TEXT, picker fills mode/target/native/depth
/language-tutor                         ← full 5-question intake
```

**Natural language** (auto-triggers via the skill):

> *"translate this to Japanese"*, *"what does this mean in French"*, *"explain this grammar"*, *"analyze my writing"*, *"correct my essay"*, *"check my grammar"*, *"proofread this"*, *"how do I pronounce this"*

The full skill instructions live at [`language-tutor/skills/language-tutor/SKILL.md`](language-tutor/skills/language-tutor/SKILL.md), the slash command at [`language-tutor/commands/language-tutor.md`](language-tutor/commands/language-tutor.md), and the on-demand reference files at [`language-tutor/skills/language-tutor/references/prompt-template.md`](language-tutor/skills/language-tutor/references/prompt-template.md), [`language-tutor/skills/language-tutor/references/constraints.md`](language-tutor/skills/language-tutor/references/constraints.md), [`language-tutor/skills/language-tutor/references/output-spec.md`](language-tutor/skills/language-tutor/references/output-spec.md).

---

### `contract-framework`

Writes a clear, fair contract for freelance and consulting work from a few plain questions. Plain-English by default, a fixed eight-part structure, three tone choices, and a firm rule against making up anything you did not provide.

```
/plugin install contract-framework@chrismccoy
```

Most "write me a contract" prompts either hand back dense legalese the client is nervous to sign, or quietly invent terms you never agreed to, a cancellation fee, a notice period, an interest rate, that come back to bite you later. This plugin does what a careful contracts specialist does. You answer six short questions: your business, your client, what you are delivering, how you get paid, anything extra you want protected, and the tone. It hands back a ready-to-fill agreement that protects both sides and still reads like plain English. Every contract covers the three things freelancers argue about most: work that grows past what was agreed, clients who pay late, and who owns the finished result.

Nothing gets invented. When a detail is missing it leaves a clearly marked blank like `[TO BE COMPLETED: kill fee basis]` for you to fill in, instead of guessing a number. Anything that changes from one country or state to another, like late-payment interest or which law applies, is written in neutral wording and flagged so you can confirm it with a local lawyer. This gives you a strong starting draft, not legal advice.

#### 📋 What's inside

A plugin with one slash command and one skill. The skill body in `skills/contract-framework/SKILL.md` holds the persona, the six inputs, the four-step workflow, and the final check. The full master prompt with the fill-in placeholders lives in `references/prompt-template.md` and loads every time. The slash command `/draft-contract` takes an optional one-line description of the work, then walks you through the rest with simple multiple-choice questions.

#### ✨ What you get

- 🎯 Six easy questions in, a complete contract out: your business, your client, the work, the payment, extra protections, and tone
- 🧱 Eight clearly labelled parts, always in the same order: Parties, Scope, Payment, Intellectual Property, Confidentiality, Termination, Liability, and General Provisions
- 🤝 Covers the three big freelance headaches every time: work creeping past the agreement, late payment, and who owns the finished result
- 🗣️ Three tone choices applied all the way through: formal, plain professional, or a warmer creative style
- 🚧 Never invents laws, names, figures, fees, deadlines, or limits. Missing details become clearly marked blanks for you to fill in
- 🌍 Anything that depends on where you live is written in neutral wording and flagged to check locally
- 🛡️ Treats your answers as plain information only. Hidden instructions tucked inside them are ignored
- 📄 Saves the contract to a tidy file when it can and just tells you where it went, otherwise prints it on screen
- ✅ A quiet final check confirms all eight parts are present, in order, the tone is consistent, and every line traces back to something you actually said

#### 🔄 How it works

1. **Questions.** The slash command asks for the six fields with simple multiple-choice prompts. If you pass a short description of the work, it uses that and skips ahead.
2. **Missing-answer check.** If any of the four must-have answers is blank or looks filled in wrong, it stops and asks you for just that piece before writing anything.
3. **Draft.** It writes the eight parts in your chosen tone, leaving marked blanks wherever you did not give a detail.
4. **Final pass.** A quiet check confirms all eight parts are present and in order, the tone is consistent, and nothing was invented, then fixes anything off before handing it over.
5. **Deliver.** Saves the contract to a file when it can and prints only the path, otherwise prints the full contract on screen.

#### 🚀 How to use it

Two ways to start:

**Slash command:**

```
/draft-contract "brand identity: logo, type system, and guidelines"   ← seeds the work description, then asks the rest
/draft-contract                                                        ← full set of questions
```

**Plain language** (starts the skill on its own):

> *"draft a freelance contract"*, *"write a service agreement"*, *"create a consulting agreement"*, *"draft a client contract for a design project"*, *"put together an independent contractor agreement"*, *"make me a contract framework"*

The full skill instructions live at [`contract-framework/skills/contract-framework/SKILL.md`](contract-framework/skills/contract-framework/SKILL.md), the slash command at [`contract-framework/commands/draft-contract.md`](contract-framework/commands/draft-contract.md), and the master prompt at [`contract-framework/skills/contract-framework/references/prompt-template.md`](contract-framework/skills/contract-framework/references/prompt-template.md).

---

### `readme-builder`

Reads a whole project and writes one beginner friendly `README.md` for it. Plain everyday English, a fixed set of sections in the same order every time, and a firm rule against inventing anything that is not really in the repo.

```
/plugin install readme-builder@chrismccoy
```

Most "write me a README" prompts either pad the page with hype ("a powerful, seamless tool") or describe features the project does not actually have. This plugin works the way a careful technical writer does. It opens and reads the real files first (the entry points, the config, the main scripts, any existing docs) to work out what the project is and what each file does, then writes the README from what it actually found. Tooling and session folders like `.git`, `.claude`, and `node_modules` are skipped and never mentioned.

The tone is aimed at someone who has never seen this kind of project before: short sentences, no jargon, and any unavoidable technical word explained in plain words right after. Marketing filler is banned outright (words like "seamless", "robust", "powerful", "leverage", and "supercharge"), along with empty fillers like "simply" and "just". The punctuation is kept plain too: no long dashes, no fancy arrows, and straight quotes only. A final check runs over the draft before you get it.

#### 📋 What's inside

A plugin with one slash command and one skill. The skill body in `skills/readme-builder/SKILL.md` holds the writer persona, the five step workflow, the fixed section order, the banned word and punctuation lists, and the final quality check. The slash command `/readme-builder` takes an optional folder path, asks whether to write the file or print it, then runs the same workflow.

#### ✨ What you get

- 📖 Reads the real project first, so the README matches what is actually there instead of being guessed
- 🧱 A fixed set of sections in the same order every time: title, description, feature list, a file by file explanation, a folder tree, and how to use it
- 🙂 Plain, friendly, everyday English with short sentences and no jargon
- 🚫 Hype words like "seamless", "robust", and "powerful" are banned, so the README stays honest
- ➖ No long dashes, no fancy arrows, and straight quotes only, which keeps the text clean and simple
- 🌳 A folder tree with a short note on each key file, so readers can see the layout at a glance
- ✅ A final check confirms every file and feature mentioned is real and a total beginner could follow it

#### 🔄 How it works

1. **Read the repo.** It opens every folder and reads the important files to learn what the project is and what each file does. Nothing is guessed.
2. **Skip the noise.** Tooling and session folders (`.git`, `.claude`, `node_modules`, build output) are ignored and left out of the README.
3. **Draft.** It writes the sections in the fixed order, covering only the parts that fit the project.
4. **Clean.** It re-reads the draft against the banned word and punctuation lists and removes anything that slipped through.
5. **Final check.** It confirms no long dashes, no hype words, every file and feature real, and beginner readable, then hands over the finished README or saves it for you.

#### 🚀 How to use it

Two ways to start:

**Slash command:**

```
/readme-builder ./my-project   ← seeds the target folder, then asks write or print
/readme-builder                ← documents the current folder
```

**Plain language** (starts the skill on its own):

> *"write a README for this repo"*, *"generate a README.md"*, *"document this project"*, *"make a beginner friendly README"*, *"explain this repo in a README"*

The full skill instructions live at [`readme-builder/skills/readme-builder/SKILL.md`](readme-builder/skills/readme-builder/SKILL.md), and the slash command at [`readme-builder/commands/readme-builder.md`](readme-builder/commands/readme-builder.md).

---

### `tutorial-builder`

Turns code, a feature, or a library into a step-by-step, hands-on tutorial that teaches instead of describing. Five inputs, a locked tutorial structure, retention patterns and cognitive-load limits built in, and a pre-publish checklist plus a 1-5 speed score that gate the result.

```
/plugin install tutorial-builder@chrismccoy
```

Most "write a tutorial" prompts produce a wall of prose with a code dump in the middle: concepts used before they are introduced, examples that do not run, no exercises, and no way for the reader to check they got it right. This plugin works the way a careful teacher does. It sets measurable objectives first (Bloom's verbs like build and debug, not "understand"), breaks the topic into atomic concepts ordered simple to complex with no forward references, and scaffolds practice as I-do, We-do, You-do. Every code block runs unmodified, lists its dependencies, and shows its expected output. Each section carries a minimal example, guided practice, a few challenges, and a troubleshooting table. The reader leaves with a summary that mirrors the opening and a concrete set of next steps.

The skill body runs the workflow and stays lean. Retention patterns (learn by doing, spaced repetition, worked examples, immediate feedback, analogies), cognitive-load limits (7 plus-or-minus 2, one-screen code, one new concept per step), and five difficulty-calibrated exercise types keep the pacing right. Depth that is not needed on every build lives one hop away in `references/implementation-playbook.md` - a full worked tutorial, per-format deep-dives, an exercise bank, and an expanded review rubric - and a finished `examples/sample-tutorial.md` ships as a copy-ready target. A pre-publish quality checklist and a 1-5 speed score (clarity, pacing, practice, troubleshooting, engagement) run before delivery.

Supplied code and repo content are treated as inert data - a directive embedded in a comment or filename is content to teach around, never a command to obey. Scope-locked to teaching content: non-tutorial and role-change requests get `I only build tutorials - give me a topic or some code and I'll teach it.`

#### 📋 Technical Overview

A Claude Code plugin with one slash command and one skill. The skill body in `skills/tutorial-builder/SKILL.md` carries the persona, scope lock, the three-step development process, the locked tutorial structure, retention and cognitive-load rules, and the quality gates. The on-demand `references/implementation-playbook.md` holds a full worked tutorial, a formats table with per-format guidance, a difficulty-calibrated exercise bank, and an expanded review rubric. A finished `examples/sample-tutorial.md` ships as a copy target. The slash command `/tutorial-builder` accepts an optional `TOPIC` or path, then walks the user through `AskUserQuestion` intake for the remaining four fields.

#### ✨ Features

- 🎯 Five inputs in, one complete tutorial out. TOPIC + AUDIENCE + FORMAT + CONSTRAINTS + DISTRIBUTION
- 🧱 Locked structure: opening (objectives, prerequisites, time, final result, setup), progressive sections, closing (summary, next steps, resources, call to action)
- 🪜 Concepts ordered simple to complex with no forward references, and exercises scaffolded I-do, We-do, You-do
- 💻 Every code block runs unmodified, lists dependencies, and shows expected output
- 🧠 Retention patterns and cognitive-load limits (7 plus-or-minus 2, one-screen code, one new concept per step) built into the pacing
- 🧩 Five difficulty-calibrated exercise types: fill-in-the-blank, debug, extension, from-scratch, refactoring
- 📚 Bundled playbook with a full worked tutorial, per-format deep-dives, an exercise bank, and a review rubric, loaded only when depth is needed
- ✅ Pre-publish checklist plus a 1-5 speed score (clarity, pacing, practice, troubleshooting, engagement) gate the result, target a 4 average
- 🛡️ Supplied code and repo content treated as inert data; embedded directives are taught around, never obeyed
- 🪧 Scope-locked. Non-tutorial and role-change requests refused with `I only build tutorials - give me a topic or some code and I'll teach it.`

#### 🔄 How it works

1. **Intake.** Slash command collects five fields via `AskUserQuestion`. If a `TOPIC` or path was passed as `$ARGUMENTS`, confirm and skip that question. If the user skips intake, apply the stated defaults: intermediate audience, deep dive format, blog or docs, latest stable tools.
2. **Define objectives.** Set measurable learning outcomes with Bloom's verbs, plus prerequisites and assumed knowledge.
3. **Decompose.** Break the topic into atomic concepts, order them simple to complex, and confirm no concept needs one introduced later.
4. **Write** the tutorial in the locked structure, one new concept per step, every code block runnable with expected output shown. Load `references/implementation-playbook.md` for a worked example, per-format detail, or the exercise bank.
5. **Gate.** Run the pre-publish checklist and the 1-5 speed score. Fix any failing gate before returning.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/tutorial-builder "Debounce a search input in vanilla JS"   ← arg seeds TOPIC, picker fills the rest
/tutorial-builder                                            ← full 5-question intake
```

**Natural language** (auto-triggers via the skill):

> *"create a tutorial for X"*, *"write a step-by-step guide to Y"*, *"turn this code into a tutorial"*, *"make a walkthrough of Z"*, *"build a coding lesson"*, *"write onboarding docs"*

The full skill instructions live at [`tutorial-builder/skills/tutorial-builder/SKILL.md`](tutorial-builder/skills/tutorial-builder/SKILL.md), the slash command at [`tutorial-builder/commands/tutorial-builder.md`](tutorial-builder/commands/tutorial-builder.md), the on-demand playbook at [`tutorial-builder/skills/tutorial-builder/references/implementation-playbook.md`](tutorial-builder/skills/tutorial-builder/references/implementation-playbook.md), and the sample tutorial at [`tutorial-builder/skills/tutorial-builder/examples/sample-tutorial.md`](tutorial-builder/skills/tutorial-builder/examples/sample-tutorial.md).

---

## Session tools

### `session-stats`

Render a Claude Code session's quantitative stats as a single self-contained, dark-theme HTML page. Stats only: KPI cards, a full metrics table, and a files-modified table. No prompts, observations, tone analysis, or recommendations.

```
/plugin install session-stats@chrismccoy
```

Session transcripts are rich but unreadable as raw `.jsonl`, and the one number people actually want, what a session cost, is not stored anywhere in them. This plugin turns a transcript into a clean visual of the numbers. A two-stage offline pipeline parses the transcript and renders the page with no external dependency. `scan_jsonl.py` walks the `.jsonl`, counts prompts (excluding slash-command and system turns), tool calls, edits, files touched, errors, compactions, and subagents, derives duration and median turn time from timestamps, and computes a cost estimate from each assistant message's token `usage` times per-model pricing (the transcript stores token counts, not dollars). `build_stats_html.py` injects the result into a fixed dark template and writes a standalone `.html` file with no `<script>` tags and no external assets.

Pricing follows the current Claude API catalog (Opus 4.8 = $5/$25 per MTok in/out, cache write $6.25, cache read $0.50). Override any rate per MTok with the `IN_RATE`, `OUT_RATE`, `CW_RATE`, `CR_RATE` environment variables. Every number traces to the transcript; absent fields render as `N/A`, never a guess.

#### 📋 Technical Overview

A Claude Code plugin with one slash command, one skill, two scripts, and a template asset. The skill body in `skills/session-stats/SKILL.md` carries the trigger phrases, the two-step workflow, and the stats-only constraint. `scripts/scan_jsonl.py` produces a metrics JSON object; `scripts/build_stats_html.py` consumes it and the fixed `assets/template.html` to emit the document. The slash command `/session-stats` resolves the current session transcript (or an explicit `.jsonl` path) and runs the pipeline.

#### ✨ Features

- 🎯 KPI cards: prompts, tool calls, edits, duration, cost, API errors, compactions, subagents
- 📊 Full metrics table plus a files-modified table (path and write count)
- 💰 Cost computed from token `usage` times per-model pricing; current Opus 4.8 catalog rates; `IN_RATE`/`OUT_RATE`/`CW_RATE`/`CR_RATE` overrides
- 🧮 promptCount excludes slash-command and system turns; cost groups assistant messages by model and sums input/output/cache-write/cache-read tokens times rates / 1e6
- 🌑 Fixed dark template; restyle via the `:root` CSS variables only
- 📦 Self-contained output: one `<!DOCTYPE html>` file, no `<script>`, no external assets, no fonts
- 🔌 Offline two-stage pipeline; pure Python stdlib; no external dependency
- 🚫 Stats only. No observations, narrative retros, or recommendations
- 🧾 Every number traces to the transcript; missing fields render as `N/A`

#### 🔄 How it works

1. **Resolve the transcript.** The slash command uses an explicit `.jsonl` path, or finds the newest transcript for the current project under `~/.claude/projects/<slug>/`.
2. **Scan.** `scan_jsonl.py --in <session.jsonl>` emits a metrics JSON object, computing cost from token usage times per-model pricing.
3. **Render.** `build_stats_html.py --out session-stats.html` injects the metrics into the dark template and writes a standalone document. Pipe the two stages, or run them separately.
4. **Report.** State the output path; the page opens in any browser.

#### 🚀 How to use it

Two ways to invoke:

**Slash command:**

```
/session-stats                       ← current session → session-stats.html
/session-stats path/to/session.jsonl ← a specific transcript
```

**Natural language** (auto-triggers via the skill):

> *"render my session stats as HTML"*, *"make an HTML stats card of my session"*, *"session stats html"*, *"export session metrics to a dark HTML page"*, *"session stats dashboard"*

The full skill instructions live at [`session-stats/skills/session-stats/SKILL.md`](session-stats/skills/session-stats/SKILL.md), the slash command at [`session-stats/commands/session-stats.md`](session-stats/commands/session-stats.md), and the scripts and template under [`session-stats/scripts/`](session-stats/scripts/) and [`session-stats/assets/template.html`](session-stats/assets/template.html).

---

## Repo layout

```
.
├── .claude-plugin/
│ └── marketplace.json ← marketplace manifest
├── jq/ ← plugin
│ ├── commands/
│ │ └── jq.md ← /jq slash command (3-field AskUserQuestion intake)
│ └── skills/
│ └── jq/
│ └── SKILL.md ← persona + 6-step workflow + cookbook + output format + quality gates
├── kubernetes-architect/ ← plugin
│ ├── commands/
│ │ └── kubernetes-architect.md ← /kubernetes-architect slash command (4-field AskUserQuestion intake)
│ └── skills/
│ └── kubernetes-architect/
│ ├── SKILL.md ← persona + scope lock + inputs + 4-step workflow + silent pre-delivery validation
│ └── references/
│ └── prompt-template.md ← authoritative master prompt with {{placeholders}} + Deployment skeleton
├── docker-compose-architect/ ← plugin
│ ├── commands/
│ │ └── docker-compose-architect.md ← /docker-compose-architect slash command (4-field AskUserQuestion intake)
│ └── skills/
│ └── docker-compose-architect/
│ ├── SKILL.md ← persona + scope lock + inputs + 4-step workflow + silent output validation
│ └── references/
│ └── prompt-template.md ← authoritative master prompt with {{placeholders}}
├── powershell-script-engine/ ← plugin
│ ├── commands/
│ │ └── powershell-script-engine.md ← /powershell-script-engine slash command (5-field AskUserQuestion intake)
│ └── skills/
│ └── powershell-script-engine/
│ ├── SKILL.md ← persona + scope lock + inputs + 4-step workflow + silent self-check
│ └── references/
│ └── prompt-template.md ← authoritative master prompt with {{placeholders}}
├── tech-blog-article/ ← plugin
│ ├── commands/
│ │ └── tech-blog-article.md ← /tech-blog-article slash command (5-field AskUserQuestion intake)
│ └── skills/
│ └── tech-blog-article/
│ ├── SKILL.md ← persona + scope lock + inputs + 4-step workflow + silent output gate
│ └── references/
│ └── prompt-template.md ← authoritative master prompt with {{placeholders}}
├── contract-framework/ ← plugin
│ ├── commands/
│ │ └── draft-contract.md ← /draft-contract slash command (6-field AskUserQuestion intake)
│ └── skills/
│ └── contract-framework/
│ ├── SKILL.md ← persona + scope lock + inputs + 4-step workflow + silent output validation
│ └── references/
│ └── prompt-template.md ← authoritative master prompt with {{placeholders}}
├── html-to-wordpress-theme/ ← plugin
│ ├── commands/
│ │ └── html-to-wordpress-theme.md ← /html-to-wordpress-theme slash command
│ └── skills/
│ └── html-to-wordpress-theme/
│ ├── SKILL.md
│ └── references/
│ ├── rules.md
│ ├── phase-1-analysis.md
│ ├── phase-2-implementation.md
│ └── phase-3-audit.md ← 79-item audit
├── html-design-styles/ ← plugin
│ ├── commands/
│ │ └── html-design-styles.md ← /html-design-styles slash command
│ └── skills/
│ └── html-design-styles/
│ ├── SKILL.md
│ └── references/
│ ├── common.md
│ └── styles/ ← one file per style (53 total)
├── accessibility-audit/ ← plugin (command only, no skills/ by design)
│ ├── commands/
│ │ ├── accessibility-audit.md ← /accessibility-audit slash command (two-round AskUserQuestion intake + 4 mode workflows)
│ │ └── a11y-audit.md ← /a11y-audit alias, reads the canonical command file
│ └── references/
│ ├── wcag-rules.md ← 8 priority rule categories + before/after fixes + ARIA patterns
│ ├── tooling.md ← axe-core, jest-axe, contrast, keyboard, pa11y, CI, report generator
│ └── manual-checklist.md ← keyboard, screen reader, visual, cognitive checks + per-widget key tables
├── wp-builder-pro/ ← plugin
│ ├── commands/
│ │ └── wp-builder-pro.md ← /wp-builder-pro slash command (4-field AskUserQuestion intake + target routing)
│ └── skills/
│ └── wp-builder-pro/
│ ├── SKILL.md ← persona + when-to-use + 6-step workflow + patterns + constraints + quality gates
│ └── references/
│ ├── theme-development.md ← templates, hierarchy, child themes, FSE
│ ├── plugin-architecture.md ← structure, activation, settings API, updates
│ ├── gutenberg-blocks.md ← block dev, patterns, dynamic blocks, FSE
│ ├── hooks-filters.md ← actions, filters, custom hooks, priorities
│ └── performance-security.md ← caching, query tuning, hardening, backups
├── wordpress-plugin/ ← plugin
│ ├── commands/
│ │ └── wordpress-plugin.md ← /wordpress-plugin slash command
│ └── skills/
│ └── wordpress-plugin/
│ └── SKILL.md ← intake + full WP plugin tree generator
├── wordpress-architect-review/ ← plugin
│ ├── commands/
│ │ └── wordpress-architect-review.md ← /wordpress-architect-review slash command
│ └── skills/
│ └── wordpress-architect-review/
│ └── SKILL.md ← detection rules + output format + scorecard + rubric
├── unslop/ ← plugin
│ └── skills/
│ └── unslop/
│ ├── SKILL.md ← trigger rules + pass-by-pass workflow
│ ├── references/
│ │ └── full-ruleset.md ← 17-rule (Rule 0-16), 19-language, 24-framework ruleset
│ └── scripts/
│ └── verify.sh ← post-edit grep verification
├── vgademo/ ← plugin
│ ├── commands/
│ │ └── vgademo.md ← /vgademo slash command (4-round intake)
│ └── skills/
│ └── vgademo/
│ ├── SKILL.md ← persona + scope lock + demoscene rules + output format
│ └── references/
│ └── examples.md ← 256b XOR-plasma + 512b boot sector + anti-pattern
├── app-blueprint/ ← plugin
│ ├── commands/
│ │ └── blueprint.md ← /blueprint slash command (5-input intake)
│ └── skills/
│ └── app-blueprint/
│ ├── SKILL.md ← 5 inputs + 11-section workflow + consistency rules
│ └── references/
│ └── prompt-template.md ← authoritative 11-section spec + validation table
├── refactoring-analyst/ ← plugin
│ ├── commands/
│ │ └── refactor.md ← /refactor slash command (path + focus + scope + depth intake)
│ └── skills/
│ └── refactoring-analyst/
│ ├── SKILL.md ← workflow (Step 0 access → Step 1 SCALE → Step 2 emit → Step 3 summary → Step 4 self-validate)
│ └── references/
│ ├── sections.md ← 16-section template + titles + per-section content
│ ├── constraints.md ← hard constraints, SCALE RULE, FOCUS_AREAS RULE, STEP 17 checklist
│ └── summary.md ← Top 5 Critical, File Impact Matrix, Issue Summary Table specs
├── docblock-rewrite/ ← plugin
│ ├── commands/
│ │ └── docblock-rewrite.md ← /docblock-rewrite slash command (path + flags)
│ ├── skills/
│ │ └── docblock-rewrite/
│ │ └── SKILL.md ← rule set + few-shot examples + engine-pick logic
│ └── scripts/
│ ├── docblock-rewrite.sh ← bash runner (walk + per-symbol claude --print + validate)
│ ├── extract-docblocks.pl ← parses /** ... */ + next declaration → JSON pairs
│ └── apply-plan.pl ← right-to-left byte-splice + .bak backup
├── codebase-to-mermaid/ ← plugin
│ ├── commands/
│ │ └── codebase-to-mermaid.md ← /codebase-to-mermaid slash command (path arg or picker: cwd vs custom)
│ └── skills/
│ └── codebase-to-mermaid/
│ ├── SKILL.md ← 5-phase procedure (Discover → Classify → Draft → Validate → Emit) + constraints
│ └── references/
│ ├── framework-signals.md ← grep cheat sheet across 19+ languages and 30+ frameworks
│ ├── archetype-table.md ← archetype → signals → best diagram (30+ rows)
│ └── examples.md ← 24 worked archetype → diagram walkthroughs
├── explain-my-code/ ← plugin
│ ├── commands/
│ │ └── explain-my-code.md ← /explain-my-code slash command (path arg or picker: cwd vs custom)
│ └── skills/
│ └── explain-my-code/
│ └── SKILL.md ← 5-phase procedure (Scope → Identify → Traverse → Write → Verify) + 13-section output contract
├── changelog-generator/ ← plugin
│ ├── commands/
│ │ └── changelog-generator.md ← /changelog-generator slash command (repo path arg or current dir)
│ └── skills/
│ └── changelog-generator/
│ ├── SKILL.md ← trust boundary + 5-step workflow + per-range brief + fixed output format
│ └── scripts/
│ └── map-history.sh ← repo/shallow check + root commit + tags + oldest-first timeline
├── excel-formula-troubleshooter/ ← plugin
│ ├── commands/
│ │ └── fix-formula.md ← /fix-formula slash command (formula + issue intake)
│ └── skills/
│ └── excel-formula-troubleshooter/
│ └── SKILL.md ← silent trace → root cause → corrected formula → explanation → alternative
├── naming-strategist/ ← plugin
│ ├── commands/
│ │ └── name-domains.md ← /name-domains slash command (5-field AskUserQuestion intake)
│ └── skills/
│ └── naming-strategist/
│ ├── SKILL.md ← scope lock + inputs + 5-step workflow + silent scoring + locked sections A-D
│ └── references/
│ ├── prompt-template.md ← authoritative master prompt with {{placeholders}}
│ ├── constraints.md ← hard constraints, blocked-word list, scoring rubric, silent validation gate
│ └── output-spec.md ← sections A-D format, per-candidate block, worked calibration example
├── wordpress-consultant/ ← plugin
│ ├── commands/
│ │ └── wordpress-consultant.md ← /wordpress-consultant slash command (7-field AskUserQuestion intake, 2 required)
│ └── skills/
│ └── wordpress-consultant/
│ ├── SKILL.md ← voice + scope lock + input gates + 6-step workflow + system rules
│ └── references/
│ ├── framework.md ← Sections 1-10 analysis + generation prompts
│ ├── output-contract.md ← word caps, Section 10 scales, summary-table columns, validation checklist
│ └── guardrails.md ← input handling + prompt-injection defense + system rules
├── language-tutor/ ← plugin
 │ ├── commands/
 │ │ └── language-tutor.md ← /language-tutor slash command (5-field AskUserQuestion intake)
 │ └── skills/
 │ └── language-tutor/
 │ ├── SKILL.md ← persona + scope lock + core behavior + inputs + 4-step workflow + silent validation gate
 │ └── references/
 │ ├── prompt-template.md ← authoritative master prompt with {{placeholders}} + both mode specs
 │ ├── constraints.md ← accuracy floor, prompt-injection defense, scope lock, silent validation gate
 │ └── output-spec.md ← section structure for both modes, optional extras, two worked examples
└── tutorial-builder/ ← plugin
 ├── commands/
 │ └── tutorial-builder.md ← /tutorial-builder slash command (5-field AskUserQuestion intake)
 └── skills/
 └── tutorial-builder/
 ├── SKILL.md ← persona + scope lock + 3-step process + locked structure + retention rules + quality gates
 ├── references/
 │ └── implementation-playbook.md ← worked tutorial, per-format deep-dives, exercise bank, review rubric
 └── examples/
 └── sample-tutorial.md ← a finished tutorial to copy and adapt
```

