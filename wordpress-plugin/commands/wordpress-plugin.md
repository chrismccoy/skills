---
description: Generate a complete, production-ready WordPress plugin from scratch with seven multiple-choice and free-text intake answers
argument-hint: [plugin name]
---

Generate a complete, enterprise-grade WordPress plugin using the `wordpress-plugin` skill. Run the seven-question intake per the skill's Intake section: two free-text (plugin name, feature detail) asked as plain prompts, and five multiple-choice (functionality, target users, admin interface, frontend display, third-party integrations). Each MC option list exceeds the `AskUserQuestion` 4-option cap, so present them as plain-text "select all that apply" checklists (target users is single-select), each with an `Other (specify)` escape. Then produce the full plugin directory with main file, modular OOP classes, security guards, i18n, readme.txt, and uninstall.php.

For an existing plugin (adding a feature, settings page, endpoint, or fix), this is the wrong skill - defer to wp-builder-pro. This command scaffolds a brand-new plugin only.

If a plugin name was provided in the slash command arguments, pre-fill it for Q1. Otherwise ask for all seven inputs in order.

Plugin name (if provided): $ARGUMENTS
