# excel-formula-troubleshooter

Debug, fix, and optimize broken Excel and Google Sheets formulas. Identifies the exact root cause (mismatched parentheses, wrong syntax, text-vs-number mismatch, circular reference, incorrect range, wrong column index), returns a copy-paste-ready corrected formula with UPPERCASE function names, a beginner-friendly bulleted explanation, and an optional modern alternative (`XLOOKUP` over `VLOOKUP`, `IFERROR` to mask error values). Scope-locked to spreadsheet-formula troubleshooting.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install excel-formula-troubleshooter@chrismccoy
```

## Use

Slash command:

```
/fix-formula =VLOOKUP(A2,Sheet2!A:B,3,0) | returns #REF!   # formula | issue
/fix-formula =VLOOKUP(A2,Sheet2!A:B,3,0)                   # asks for the issue
/fix-formula                                               # full intake (formula + issue)
```

Or auto-triggers on natural language:

- *"fix my Excel formula"*
- *"debug this spreadsheet formula"*
- *"why does my formula return #REF!"*
- *"troubleshoot a Google Sheets formula"*
- *"my VLOOKUP isn't working"*
- *"correct this formula"*

## What's in here

```
excel-formula-troubleshooter/
├── .claude-plugin/plugin.json              ← plugin manifest
├── commands/
│ └── fix-formula.md                        ← /fix-formula slash command (formula + issue intake)
└── skills/excel-formula-troubleshooter/
  └── SKILL.md                              ← workflow (silent trace → root cause → fix → explain → alternative)
```

## Inputs

- `broken_formula` - the formula that isn't working.
- `issue` - what's going wrong (error code, wrong result, expected behavior).

If the issue is missing, the command asks rather than guessing.

## Output structure (locked)

```
### ❌ The Issue
[why the original formula failed]

### ✅ Corrected Formula
```excel
[the exact corrected formula]
```

### 🛠️ How the Fix Works (maximum 4 bullets)
- [bullet]
- [bullet]

### 🚀 Better Alternative (optional)
[modern/efficient alternative, or omitted if none applies]
```

## Scope lock

Spreadsheet-formula troubleshooting and data analysis only. Questions outside that scope are refused.

## License

MIT.
