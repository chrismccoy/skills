# wordpress-plugin

Generates complete WordPress plugins from scratch - full directory structure, security guardrails, internationalization, and a complete uninstall script. Guided intake (five multiple-choice + two free-text) drives every file in the output tree. For changes to an existing plugin, use wp-builder-pro instead; this skill scaffolds a brand-new plugin only.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace. Full description and usage examples in the [marketplace root README](../README.md#wordpress-plugin).

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install wordpress-plugin@chrismccoy
```

## Use

```
/wordpress-plugin ← walks through all seven questions
/wordpress-plugin "Acme Bookings" ← pre-fills the plugin name
```

Or just describe what you want - the skill auto-triggers on natural language like *"build me a WordPress plugin for time-slot bookings"*, *"scaffold a WP plugin with a settings page and a REST endpoint"*, *"create a custom post type plugin for testimonials"*, or *"I need a Gutenberg block plugin for newsletter signups"*.

## What's in here

```
commands/wordpress-plugin.md ← /wordpress-plugin slash command
skills/wordpress-plugin/
└── SKILL.md ← intake + file generation rules + security/standards/uninstall
```

## How it works

1. **Intake**: five picker prompts via `AskUserQuestion` plus two free text:
 - Plugin name (free text)
 - Functionality categories (multi-select: CPTs, settings page, blocks, shortcodes, REST, WP-CLI, cron, custom tables, roles, email, forms, dashboard widget, import/export, logging, user meta)
 - Specific feature detail (free text. 2-4 sentences)
 - Target users (single-select: admins / editors / frontend visitors / developers / multisite network admins / mixed)
 - Admin interface components (multi-select: top-level menu, settings submenu, tools submenu, meta boxes, list tables, dashboard widget, admin notices, help tabs, none)
 - Frontend display surfaces (multi-select: shortcodes, blocks, widgets, template tags, `the_content` filter, REST SPA, custom page templates, none)
 - Third party integrations (multi-select: WooCommerce, BuddyPress, ACF, Elementor, external REST API, Stripe/PayPal, Mailchimp, GA, OAuth providers, webhooks)
2. **Inference**: slug, text domain, constant prefix, PHP namespace, main file name, and singleton class name are all derived from the plugin name. No follow-up questions about tech choices.
3. **Generation**: produces the full plugin directory with conditionally-skipped files for unselected features (no Gutenberg `blocks/` folder if blocks weren't picked, no `class-rest-controller.php` if REST wasn't picked, etc.).
4. **Delivery**: writes to `./{plugin-slug}/` by default; falls back to `./{plugin-slug}-new/` if the first already exists.

## Quality guarantees

- `defined( 'ABSPATH' ) || exit;` on every PHP file
- Nonce verification on every form, AJAX request, and REST mutation
- Capability checks before every privileged action
- Sanitization on every input, escaping on every output, prepared statements on every `$wpdb` query
- WordPress Coding Standards (WPCS) compliant
- Internationalization with text domain and a populated `.pot` file
- `dbDelta()` for custom tables with charset/collation and indexes
- Object-cache-aware queries with transients where appropriate
- Conditional asset enqueueing - no admin CSS/JS on the frontend
- `readme.txt` in WordPress.org format with all required headers populated
- `uninstall.php` removes every artefact the plugin creates: options, tables, user meta, post meta, scheduled events, registered roles, registered capabilities
- Multisite-aware activation, deactivation, and uninstall when the multisite audience is selected
- Zero `TODO`, `TBD`, or unfilled `{placeholder}` text in any file

