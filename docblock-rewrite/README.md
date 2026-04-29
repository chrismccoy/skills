# docblock-rewrite

Convert PHPDoc and JSDoc `/** ... */` blocks into one-line `//` comments
a non-technical reader can understand. Strip tech jargon. Keep all
behavior unchanged.

## Two engines, same rules

| Engine | When | Tools |
|---|---|---|
| **Skill (interactive)** | 1-20 files, prompt tuning, edge cases | Model uses Read / Edit / Bash |
| **Script (bulk)** | 20+ files, repeat runs, CI / unattended | `bash` + `perl` + `claude --print` |

Both engines apply the same prompt rules: banned-word list, 100-char cap,
file-level detection, opt-out tags.

## Slash command

```
/docblock-rewrite <path> [flags]
```

| Flag | Default | Effect |
|---|---|---|
| `--dry-run` | off | Print unified diffs, write nothing |
| `--concurrency N` | 3 | Files in flight at once |
| `--model NAME` | `claude-haiku-4-5-20251001` | Override model |
| `--no-backup` | off | Skip `.bak` files |
| `--include-vendor` | off | Do not skip vendor/node_modules/etc. |
| `--strict` | off | Exit non-zero (2) if any block was skipped (CI gate) |

## Skill invocation

Drop the slash command and just ask:

> Rewrite the docblocks in `src/` to plain English.
> Convert all my PHPDoc blocks to friendly one-line comments.
> Strip jargon from the comments in `formatting.php`.

The model loads the `docblock-rewrite` skill, picks the right engine
based on file count, and runs.

## Rules summary

Replace each `/** ... */` block with one line:

```
// <plain-English summary>.
```

- Plain English only - no `array`, `callback`, `instantiate`, etc.
  (full banned-word list in `skills/docblock-rewrite/SKILL.md`).
- Describe what it does for the user, not how it works.
- Functions: start with a present-tense verb.
- Classes / files / properties / constants: noun phrase.
- ≤100 characters total.
- Capitalize, end with a period.
- Never include `@param`, `@return`, `@throws`, types, or tags.
- If meaning is genuinely unclear: `// TODO: describe purpose.`

## Opt-outs

Doc blocks containing `@internal`, `@deprecated`, or `@ignore` are left
alone.

## Skip list

Files under `vendor`, `node_modules`, `dist`, `build`, `coverage`,
`__tests__`, `.git`, `.svn`, `.hg`, `.next`, `.nuxt`, `out`, `tmp` are
skipped, along with `*.min.js` and `*.generated.*`, unless
`--include-vendor` is passed.

## Requirements (script only)

- `bash` 4+ (`brew install bash` on macOS)
- `jq`
- `perl` with `MIME::Base64`
- `claude` CLI on `PATH` (Claude Code subscription auth, no API key
  required)

On Windows, run via WSL or Git Bash - the script does not run in native
PowerShell. Without either, use the skill's inline engine (Read/Edit, no
extra tools needed).

## Rolling back

`.bak` files are created next to every modified file. This restores the most
recent run:

```bash
find <path> -name '*.bak' -exec sh -c 'mv "$1" "${1%.bak}"' _ {} \;
```

On repeat runs older backups rotate to `.bak.1`, `.bak.2`, … (highest number =
oldest/true original). To undo all runs, restore the highest-numbered `.bak.N`
per file instead.

## Layout

```
docblock-rewrite/
├── .claude-plugin/plugin.json
├── commands/docblock-rewrite.md
├── skills/docblock-rewrite/SKILL.md
└── scripts/
    ├── docblock-rewrite.sh
    ├── extract-docblocks.pl
    ├── apply-plan.pl
    └── system-prompt.txt
```
