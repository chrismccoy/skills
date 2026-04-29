# html-to-wordpress-theme

Converts static HTML files into installable WordPress themes.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace. Full description, features list, and AI analysis verdict in the [marketplace root README](../README.md#html-to-wordpress-theme).

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install html-to-wordpress-theme@chrismccoy
```

## Use

```
/html-to-wordpress-theme ← starts the workflow
/html-to-wordpress-theme Brewline ← pre-fills the theme name
```

Or just describe what you want. the skill auto-triggers on natural language like *"convert this index.html and single.html into a WordPress theme called Brewline"*.

## What's in here

```
.claude-plugin/plugin.json ← plugin manifest
commands/html-to-wordpress-theme.md ← /html-to-wordpress-theme slash command
skills/html-to-wordpress-theme/
├── SKILL.md ← workflow + initialization gate + naming + self-check
└── references/
 ├── rules.md ← always-active escaping/i18n/PHP/a11y rules
 ├── phase-1-analysis.md ← HTML validation + structured analysis
 ├── phase-2-implementation.md ← chunk planning + template architecture
 └── phase-3-audit.md ← 79-item self-audit checklist
CHANGELOG.md ← release notes
```

## How it works

The skill walks the user through a 4-phase conversion with mandatory user approval gates between phases:

1. **Initialization**: confirm theme name, source HTML files (using the Source HTML → WordPress Template Mapping convention), and defaults
2. **Phase 1A. Critical Analysis**: HTML validation, source quality grading, template/navigation/content/design-token mapping, file manifest
3. **Phase 1B. Extended Analysis**: sidebars, interactive behavior, image handling, comments, theme.json
4. **Phase 2. Implementation**: generates every theme file in user-approved chunks
5. **Phase 3. Self-Audit**: 79-item evidence-cited checklist before delivery

The user approves at each gate. Nothing ships without sign-off.

