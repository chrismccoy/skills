# html-design-styles

A catalog of 53 named design styles for frontend interfaces. bento, brutalist, glassmorphism, vaporwave, kawaii, cyberpunk, swiss, art deco, neumorphism, and many more.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace. Full description, categorized style list, usage examples, and "what each style spec includes" in the [marketplace root README](../README.md#html-design-styles).

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install html-design-styles@chrismccoy
```

## Use

```
/html-design-styles ← asks you to pick a style
/html-design-styles brutalist ← starts straight into Brutalist
/html-design-styles brutalist landing page for my SaaS
 ← pre-fills both style + project
```

Or just describe what you want. the skill auto-triggers on style names like *"build me a vaporwave landing page"* or *"make this dashboard look brutalist"*.

## What's in here

```
.claude-plugin/plugin.json ← plugin manifest
commands/html-design-styles.md ← /html-design-styles slash command
skills/html-design-styles/
├── SKILL.md ← entrypoint with 53-style picker, workflow, init gate
└── references/
 ├── common.md ← cross-cutting patterns (font loading, focus rings,
 │ marquees, scrollbars, accessibility). load once
 └── styles/ ← one file per style. load only the chosen one
 ├── bento.md
 ├── pure-brutalist.md
 ├── glassmorphism.md
 ├── vaporwave.md
 └── … (53 total)
```

## How it works

1. **Identify the style**: match the user's request against the 53-item catalog (or ask them to pick if ambiguous)
2. **Get project context**: full page, single component, restyling existing markup, what content goes in
3. **Load references**: `common.md` once per session, then `styles/<slug>.md` for the chosen style's complete spec
4. **Apply faithfully**: exact color values, typography stack, shadow recipes, and component patterns. no "similar" substitutions

Output: a single self-contained HTML file with CDN Tailwind plus inline custom CSS for the style's signature mechanics. No build step.

