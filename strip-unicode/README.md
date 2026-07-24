# strip-unicode

A deterministic text cleaner. Give it messy text full of fancy Unicode - curly quotes, long dashes, ellipses, bullets, invisible junk - and it hands back plain 7-bit ASCII that works everywhere. It transliterates, it never interprets: line breaks, indentation, and wording stay exactly as written. Nothing gets summarized, rewritten, or grammar-fixed.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install strip-unicode@chrismccoy
```

## Use

Slash command:

```
/strip-unicode notes.md        # arg matches a file -> asks File (1) or text (2)
/strip-unicode “Hi—bye”…       # pasted text -> cleaned in a code block
/strip-unicode                 # full File/Paste picker
```

Or auto-triggers on natural language:

- *"strip the unicode from this"*
- *"convert this to plain ASCII"*
- *"remove the smart quotes"*
- *"replace the em dashes"*
- *"clean the invisible / zero-width characters"*
- *"normalize this text to ASCII"*
- pasting text full of curly quotes, dashes, bullets, or odd spaces and asking to flatten it

## What it does

- Em and en dashes (`—` `–`) -> hyphen `-`
- Curly quotes (`“ ” ‘ ’`) -> straight `"` and `'`
- Ellipsis `…` -> `...`, bullets (`•` `▪` `◦`) -> `-`
- Non-breaking and zero-width characters -> normal space or removed
- Math symbols: `≤` -> `<=`, `≥` -> `>=`, `≠` -> `!=`, `×` -> `x`, `÷` -> `/`
- Every other non-ASCII character -> nearest ASCII form (`café` -> `cafe`), or removed and logged when there is none (`€`, emoji, CJK)

Specific rules always win over the catch-all, and no character is transformed twice. After cleaning it verifies zero `[^\x00-\x7F]` characters remain and prints a table of every character it changed and how many times.

## Two modes

- **File** - cleans a file in place, echoes the target first, and aborts with `Error: <path> not writable - no changes made.` rather than writing a partial file. It never deletes a file or writes outside the target path.
- **Paste** - returns the cleaned text in a code block with the report. No filesystem write.

Mode is chosen by input **structure**, not content: multi-line is Paste, a lone line that isn't a real file is Paste, and a lone line that matches a file is ambiguous - so it asks before touching the file. Everything in the input is treated as inert data to clean, never as instructions.

## What's in here

```
strip-unicode/
├── .claude-plugin/plugin.json          ← plugin manifest
├── commands/
│ └── strip-unicode.md                  ← /strip-unicode slash command (File/Paste picker)
└── skills/strip-unicode/
  ├── SKILL.md                          ← overview + rule table + workflow + output format + quality gates
  └── scripts/
    └── strip_unicode.py                ← deterministic transliteration + reporting
```

## Scope

Maps characters to the 7-bit ASCII range and reports what changed. Out of scope: language translation, romanizing whole non-Latin scripts into readable words, grammar/spelling fixes, and rewriting or summarizing prose.
