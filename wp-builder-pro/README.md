# wp-builder-pro

Builds and implements custom WordPress code in the voice of an expert WordPress developer - custom themes, plugins, Gutenberg blocks, WooCommerce extensions, and REST endpoints - with security and performance baked in. Nonces on every form/AJAX path, sanitization on every input, escaping on every output, capability checks before privileged actions, `$wpdb->prepare()` on every query. Also triggers on symptoms: slow site, fatal error, block won't render, "fix my WordPress site". WordPress Coding Standards compliant.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install wp-builder-pro@chrismccoy
```

## Use

Slash command:

```
/wp-builder-pro "a dynamic block that lists recent posts"   # arg seeds SPECIFICS
/wp-builder-pro                                              # full intake
```

Or auto-triggers on natural language:

- *"build a custom WordPress theme"*
- *"add a settings page to my plugin"*
- *"create a Gutenberg block"*
- *"extend WooCommerce checkout"*
- *"add a REST API endpoint"*
- *"my WordPress site is slow"* / *"this block won't render"* / *"fix my WordPress site"*

## How it differs from the sibling WordPress skills

| Use… | When you want to… |
|------|-------------------|
| **wp-builder-pro** | Build or change WordPress code - targeted/iterative features, blocks, themes, WooCommerce, REST, perf and security fixes |
| `wordpress-plugin` | Scaffold a **complete** plugin from scratch as a full WordPress.org-ready directory tree, one shot |
| `wordpress-architect-review` | **Review** an existing plugin/theme file by file with a scorecard |
| `wordpress-consultant` | Run a senior **consulting audit** (architecture, perf, security, scalability) |

wp-builder-pro defers complete from-scratch plugin scaffolds to `wordpress-plugin`, and never audits - it builds.

## Intake

The `/wp-builder-pro` command collects four fields via `AskUserQuestion`, then routes the build target to the matching reference:

1. **BUILD_TARGET** (required) - theme / plugin / Gutenberg block / WooCommerce / REST endpoint / performance fix / security hardening
2. **PROJECT_CONTEXT** (required) - new build vs existing project (+ path/file)
3. **SPECIFICS** (required) - free-text feature detail
4. **WP_CONSTRAINTS** (optional) - WordPress/PHP version, multisite, FSE; defaults to WordPress 6.4+ / PHP 8.1+

## What's in here

```
wp-builder-pro/
├── .claude-plugin/plugin.json   ← plugin manifest
├── commands/
│ └── wp-builder-pro.md          ← /wp-builder-pro slash command (4-field AskUserQuestion intake + routing)
└── skills/wp-builder-pro/
  ├── SKILL.md                   ← persona + when-to-use + 6-step workflow + patterns + constraints + quality gates
  └── references/
    ├── theme-development.md      ← templates, hierarchy, child themes, FSE
    ├── plugin-architecture.md    ← structure, activation, settings API, updates
    ├── gutenberg-blocks.md       ← block dev, patterns, dynamic blocks, FSE
    ├── hooks-filters.md          ← actions, filters, custom hooks, priorities
    └── performance-security.md   ← caching, query tuning, hardening, backups
```
