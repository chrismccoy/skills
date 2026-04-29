# readme-builder

A senior technical writer that scans a real repository and writes one beginner friendly `README.md` for it. It reads the important files first (entry points, config, main scripts, existing docs), then writes a fixed set of sections in plain English: title, description, feature list, a file by file explanation, a folder tree, and usage steps. Accuracy over polish: every claim matches what is really in the repo, with no invented features. Enforces a banned marketing word list and banned punctuation (no long dashes, fancy arrows, or curly quotes), then runs a final quality gate pass before output.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install readme-builder@chrismccoy
```

## Use

Slash command:

```
/readme-builder                 # documents the current directory
/readme-builder ./my-project    # arg seeds the target folder
```

Or triggers automatically on natural language:

- *"write a README for this repo"*
- *"generate a README.md"*
- *"document this project"*
- *"make a beginner friendly README"*
- *"explain this repo in a README"*

## What's in here

```
readme-builder/
├── .claude-plugin/plugin.json      ← plugin manifest
├── commands/
│ └── readme-builder.md             ← /readme-builder slash command (target + write/print intake)
└── skills/readme-builder/
  └── SKILL.md                      ← persona, five step workflow, section order, banned lists, quality gates
```

## Scope

Covers reading a repository and producing a single beginner friendly `README.md` in a fixed section order, with a plain English tone, a banned marketing word list, banned punctuation, and a final quality gate pass.

Out of scope: API reference docs, architecture deep dives with diagrams (use `explain-my-code`), and code review (use a review skill).
