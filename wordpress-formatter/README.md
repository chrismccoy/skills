# wordpress-formatter

Set up WordPress Coding Standards formatting for a theme and apply the
auto-fixable formatting - tabs, spacing, array style, alignment - without
changing how any page renders. It installs the tools, writes the config, runs
the fixer, and checks the result. It never touches escaping or behavior.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install wordpress-formatter@chrismccoy
```

## Use

```
/wordpress-formatter ← formats the current theme
/wordpress-formatter ./wp-content/themes/mytheme ← formats a specific theme
```

Or just describe what you want - the skill auto-triggers on natural language
like *"format my WordPress theme to the coding standard"*, *"run phpcbf on my
templates"*, *"fix the indentation and spacing in my theme"*, *"set up phpcs
for this theme"*, or *"convert my theme files to tabs"*.

It asks five short questions first, then does the rest.

## What it asks

1. **Scope** - just the template files and partials, or every PHP file in the theme.
2. **Strictness** - formatting only (recommended), or the full standard that also flags escaping and translations.
3. **Yoda checks** - whether to reorder conditions like `$x == 'y'` to `'y' == $x`. Off by default.
4. **Theme name** - used in the config file.
5. **Files to skip** - for example a standalone landing page that is not a normal template.

Answer "just do it" and it uses the safe defaults.

## What it does

1. **Checks first.** Confirms the folder is a WordPress theme. If it is not, it stops and says so.
2. **Installs the tools.** Adds PHP_CodeSniffer and the WordPress Coding Standards as Composer dev dependencies. Skips this if they are already there.
3. **Writes the config.** Creates a `phpcs.xml.dist` scoped to your answers, with `vendor`, `node_modules`, and (by default) `lib`, `inc`, `assets`, and `functions.php` left out.
4. **Fixes the formatting.** Runs `phpcbf` twice, since some fixes unlock others.
5. **Checks the result.** Runs `php -l` on every changed file. If any file breaks, it stops and tells you.
6. **Reports what is left.** Lists the remaining items and what it did with each.

## What it will not change

Some items the standard flags can change how the code runs, so the formatter
reports them but leaves them alone:

| Item | Why it is left alone |
|---|---|
| Loose `==` changed to strict `===` | Can change the result of a comparison |
| `array_search` strict flag | Can change what matches |
| `extract()` | A rewrite, not formatting |
| Escaping and translations | Only shown in the strict mode, and adding them can change output |

The one optional exception is Yoda conditions, which only reorder the two sides
of a comparison and are safe. Those are applied only if you say yes.

## Two safe stops

- No `composer.json`? It asks whether to create one instead of doing it silently.
- The install fails? It stops and shows the exact error and command, rather than guessing.

## Requirements

- `php` on the `PATH`
- `composer` on the `PATH`

Everything else is installed for you into the theme's local `vendor/` folder.
Nothing is installed globally.

## Layout

```
wordpress-formatter/
├── .claude-plugin/plugin.json
├── commands/wordpress-formatter.md ← /wordpress-formatter slash command
└── skills/wordpress-formatter/
    └── SKILL.md ← intake, workflow, triage table, report format
```
