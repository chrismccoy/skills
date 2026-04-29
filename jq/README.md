# jq

Expert `jq` usage for querying, filtering, transforming, and aggregating JSON in real shell pipelines, in the voice of a senior CLI engineer. Inspects the actual JSON shape before writing filters, builds them one pipe stage at a time, and delivers a single copy-paste-ready `jq` command with a one-line explanation per filter stage. Enforces `-r` for shell consumption, `--arg`/`--argjson` over string interpolation, single-quoted filters, and `null`/empty edge-case handling.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install jq@chrismccoy
```

## Use

Slash command:

```
/jq 'curl -s https://api.github.com/repos/owner/repo/issues'   # arg seeds JSON_SOURCE
/jq                                                            # full intake
```

Or auto-triggers on natural language:

- *"parse this JSON"*
- *"extract X from this output"*
- *"pull the field with jq"*
- *"filter this API response"*
- *"reshape this JSON"*
- *"aggregate these records"*
- *"explain this jq filter"*
- pasting raw JSON or CLI output (curl, kubectl, aws, gh, docker) and asking to filter, transform, or summarize it

## What's in here

```
jq/
├── .claude-plugin/plugin.json   ← plugin manifest
├── commands/
│ └── jq.md                      ← /jq slash command (3-field AskUserQuestion intake)
└── skills/jq/
  └── SKILL.md                   ← overview + 6-step workflow + cookbook + output format + quality gates
```

## Scope

Covers basic and nested selection, `select()` filtering, `map`/transform, `reduce` and `group_by` aggregation, string interpolation and `@csv`/`@tsv`/`@base64`/`@uri` formatting, key and path manipulation, conditionals and `try`/`catch`, and shell integration (`--arg`/`--argjson`, `-r`, `-c`, `-s`).

Out of scope: writing JSON, JSON Schema validation, jsonnet, non-jq shell scripting.
