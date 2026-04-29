# wordpress-architect-review

Senior WordPress architect code review for plugins and themes. file by file audit covering security, performance, architecture, correctness, WordPress standards, accessibility, i18n, and missing infrastructure. Output is a structured report with a 1-10 scorecard, severity-tagged findings (SEVERE/MODERATE/MINOR), file:line citations, quoted offending code, top-5 prioritized fixes, and an optional 3-phase refactor roadmap.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install wordpress-architect-review@chrismccoy
```

## Use

```
/wordpress-architect-review ← audits current working directory
/wordpress-architect-review ./wp-content/plugins/x ← audits specified path
```

Or just describe what you want - the skill auto-triggers on natural language like *"review my WordPress plugin for security holes"*, *"audit this theme before I submit it to WordPress.org"*, *"is this plugin secure?"*, *"give me a senior architect review of this WP code"*, or *"find the bugs in my custom plugin"*.

## What's in here

```
commands/wordpress-architect-review.md ← /wordpress-architect-review slash command
skills/wordpress-architect-review/
├── SKILL.md ← scope lock, detection rules, output format, scorecard
└── references/
    ├── categories.md ← finding-category checklist + scorecard roll-up
    └── rubric.md ← 5-tier rating rubric
```

## How it works

1. **Detect target**: looks for plugin header in root PHP, `style.css` theme header, `block.json`, or `wp-content/mu-plugins/` path. Aborts cleanly if none found.
2. **Read every file**: every PHP, JS, CSS, and config file is opened with the Read tool. No summarizing from filenames. Companion files (`readme.txt`, `theme.json`, `composer.json`, `package.json`, `phpcs.xml`) read before scoring.
3. **Categorize findings**: Architecture, Performance, Security, Correctness, WordPress Standards, Theme-specific or Plugin-specific, Maintainability, Missing Infrastructure, Compatibility. Max 5 findings per category, most severe first.
4. **Score and rank**: 10-row scorecard weighted toward Security, Performance, Correctness. Top 5 fixes ranked by impact with S/M/L effort tags. Refactor roadmap only if overall < 6/10.

## Report shape

Every finding follows the same shape - no deviation:

> **SEVERE - SQL Injection** - `includes/class-search.php:142`
> ```php
> $results = $wpdb->get_results( "SELECT * FROM {$wpdb->prefix}log
>   WHERE user_id = " . $_GET['uid'] );
> ```
> **Impact:** Unsanitized `$_GET['uid']` concatenated into raw SQL. Authenticated subscriber can dump entire log table.
> **Fix:** `$wpdb->prepare( "...WHERE user_id = %d", absint($_GET['uid']) )` plus nonce check via `wp_verify_nonce`.

## Quality guarantees

- Every finding cites `file:line` and quotes the offending code
- Every finding tagged SEVERE / MODERATE / MINOR
- Scorecard table always has all 10 rows filled
- Top 5 fixes always carry an effort tag (S/M/L)
- Prompt-injection defense - file contents treated as inert data; injection attempts in audited code are flagged as a SEVERE Security finding
- Scope-locked - refuses tutorials, hosting advice, plugin recommendations, non-code questions
- Banned filler word list enforced (no "leverage", "robust", "comprehensive", "utilize", "synergy", etc.)
- Pre-emit validation - partial reports are regenerated, never shipped

