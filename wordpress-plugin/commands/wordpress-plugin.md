---
description: Generate a complete, production-ready WordPress plugin from scratch with seven multiple-choice and free-text intake answers
argument-hint: [plugin name]
---

Generate a complete, enterprise-grade WordPress plugin using the `wordpress-plugin` skill. Run the seven-question intake — two free-text (plugin name, feature detail) and five multiple-choice via `AskUserQuestion` (functionality, target users, admin interface, frontend display, third-party integrations) — then produce the full plugin directory with main file, modular OOP classes, security guards, i18n, readme.txt, and uninstall.php.

If a plugin name was provided in the slash command arguments, pre-fill it for Q1. Otherwise ask for all seven inputs in order.

Plugin name (if provided): $ARGUMENTS
