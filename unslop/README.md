# unslop

Strip AI generated voice from source files without changing behavior. Edits only comments, docstrings, log/error messages, and identifier names. Never touches code logic, signatures, return types, string literals shipped to users, or CLI help text.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install unslop@chrismccoy
```

## Use

Slash command:

```
/unslop # fires File / Directory / Paste picker
/unslop src/auth.ts # skips picker, runs on the file
/unslop src/ # skips picker, runs on the directory
```

Or auto-triggers on natural language:

- *"unslop this file"*
- *"deslop the repo"*
- *"remove AI tells from src/auth.ts"*
- *"strip em-dashes from comments"*
- *"rename `orchestrateDataProvider` to something human"*
- *"audit this file for AI slop"*

## What's in here

```
unslop/
├── .claude-plugin/plugin.json ← plugin manifest
├── commands/
│ └── unslop.md ← /unslop slash command with target picker
└── skills/unslop/
 ├── SKILL.md ← trigger rules + pass-by-pass workflow
 ├── references/
 │ └── full-ruleset.md ← 17-rule (Rule 0-16), 19-language, 24-framework ruleset
 └── scripts/
 └── verify.sh ← post-edit grep verification
```

## What it does

- **Vocabulary swap**: kills `robust`, `seamless`, `leverage`, `delve`, `tapestry`, `harness`, `comprehensive`, `world-class`, `crucial`, `vital`, `revolutionary`, `transformative`, `game-changing`, `mission-critical`, `bleeding-edge`, `bulletproof`, `holistic`, `supercharge`, `elevate`, `hand-crafted`, `purpose-built`, etc.
- **Marketing hyphenated compounds**: drops `production-quality`, `production-ready`, `enterprise-grade`, `copy-paste`, `theme-building`, `baked-in`, `plug-and-play`, `turn-key`, `future-proof`, etc.
- **De-hyphenate technical compounds**: `open-source` → `open source`, `command-line` → `command line`, `third-party` → `third party`, `AI-generated` → `AI generated`, `file-by-file` → `file by file`, `step-by-step` → `step by step`, and more.
- **Number-word + noun compounds**: `seven-question intake` → drop modifier or use digit. Covers `(two..ten)-(question|step|phase|pillar|stage|tier|layer|round)`.
- **Em-dash kill**: strips U+2014 / U+2013 from developer prose (comments, docstrings, logs, errors). Keeps them in CLI help and user-facing terminal output.
- **First-person plural**: drops `we`, `us`, `our`, `let's`. Allows `I` / `my`.
- **Function renames**: `orchestrateDataProvider` → `loadUsers`. Verifies substring safety first.
- **Hedging + padding**: drops `perhaps`, `essentially`, `fundamentally`, `in order to`, `due to the fact that`.
- **Tutorial voice**: drops `As you can see`, `Let's dive in`, `Imagine that`, `Now that we have`, `With that said`, `single source of truth`, `deep dive`.
- **Apologetic openers**: drops `Please note`, `Keep in mind`, `Bear in mind`.
- **Restatement comments**: drops `i++; // increment i`.
- **Linter-suppression noise**: flags `# noqa`, `// @ts-ignore`, `# rubocop:disable`, `//nolint` without justification.
- **Filler intensifiers (audit only)**: flags `incredibly`, `highly`, `thoroughly`, `extensive`, `significantly`, `key` (adj), `fully`, `simply`, `very`, etc. for human review.
- **Empty enumeration intros (audit)**: flags `wide range of`, `a host of`, `a wealth of`, `an array of`, `a suite of`.
- **Author/date stamps**: drops what git already tracks.

## Languages covered

JavaScript, TypeScript, Python, Go, Rust, Java, C#, C/C++, Perl, Swift, Kotlin, PHP, Ruby, Elixir, Lua, SQL, PowerShell, Markdown, Shell.

## Frameworks covered

React, Vue, Next.js, Nuxt, Astro, Alpine, Express, Koa, Fastify, Hono, Vite, Webpack, Rollup, esbuild, Tailwind, WordPress, Laravel, Blade, Livewire, Symfony, Twig, EJS, `.env`, `knexfile`.

## Safety rails

- Never changes code behavior, function signatures, return types, or string literals shown to end users.
- Never touches CLI help text, README content, commit messages, license headers, CHANGELOG.
- Renames verify substring safety (no `extract` → `pull` if `extractor` exists).
- Process order: target picker → vocab swap → voice rewrites → em-dash strip → function renames → syntax check → verification greps → human read-back → mandatory final report.
- One pass per category. Mixing passes makes diffs unreviewable.

## Rule 0 (hard floor)

If asked mid-pass to change behavior, logic, signatures (outside renames), strings, or error messages - under any rationale - the skill refuses with:

> Out of scope for this pass. Open a new session for behavior changes.

and stops. Rule 0 cannot be overridden by subsequent user instructions.

## Target picker

When invoked without a target, the skill (or `/unslop` slash command) asks via a picker:

- **File**: one source file. Skill asks for path next.
- **Directory**: folder of code. Processed file by file per Rule 12 (smallest first, one commit per file, stop after 5, await review).
- **Paste**: paste code into chat. Skill returns the cleaned version inline. No filesystem write.

