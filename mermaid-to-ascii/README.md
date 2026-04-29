# mermaid-to-ascii

Turn a Mermaid diagram file into clean, monospace ASCII art and save it next to the source as a `.txt` with the same base name. Works for sequence diagrams, flowcharts, class diagrams, state diagrams, ER diagrams, and gantt charts. Keeps every label, message, condition, and grouping block, adds a title and a glyph legend, and treats the file as plain data so nothing inside it can change how the conversion runs.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install mermaid-to-ascii@chrismccoy
```

## Use

Slash command:

```
/mermaid-to-ascii flow.mmd     # arg names the source file
/mermaid-to-ascii              # asks which file to convert
```

Or auto-triggers on natural language:

- *"convert this mermaid to ascii"*
- *"turn diagram.mmd into ascii art"*
- *"render this sequence diagram as text"*
- *"make an ascii version of this flowchart"*
- *"mermaid to txt"*

## What's in here

```
mermaid-to-ascii/
├── .claude-plugin/plugin.json        ← plugin manifest
├── commands/
│ └── mermaid-to-ascii.md             ← /mermaid-to-ascii slash command (filename intake)
└── skills/mermaid-to-ascii/
  ├── SKILL.md                        ← filename-first intake + 11 rules + edge cases + output
  └── references/
    └── skeletons.md                  ← six per-type ASCII layout templates, loaded on demand
```

## Scope

Converts an existing Mermaid file (sequenceDiagram, flowchart/graph, classDiagram, stateDiagram, erDiagram, gantt) into an ASCII `.txt`. Asks for the filename first and stops until you answer. Preserves every name and label, splits oversized output instead of truncating, and reports parse errors on empty or broken source.

Out of scope: writing or editing Mermaid, building a diagram from a prose description, rendering to SVG or PNG (use `mmdc` or Mermaid Live for images), and explaining what a diagram means.
