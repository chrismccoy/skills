# accessibility-audit

Finds, reports, and fixes WCAG accessibility issues in web UI - source files, live pages, or the component you're building right now. Prefers auditing the rendered page over reading source, groups findings by pattern instead of listing the same issue thirty times, cites a WCAG criterion on every finding, and separates what a machine can check from what only a person with a screen reader can.

**Command-only by design.** This plugin ships no skill file, so it never auto-triggers and never fights another accessibility plugin for the same request. It runs when you type the command, and only then.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install accessibility-audit@chrismccoy
```

## Use

```
/accessibility-audit src/components     ← arg seeds the scope
/accessibility-audit http://localhost:3000
/a11y-audit                             ← short alias, full intake
```

Both commands are identical. Either way you answer a few quick questions first:

1. **Mode** - Report (audit only, no edits), Fix (audit, edit, verify), Component (refactor one pasted component), or Guide (rules applied to UI you're writing)
2. **Scope** - a directory, specific files, a URL, or pasted component code
3. **Standard** - WCAG 2.1 AA, 2.2 AA, 2.2 AAA, or 2.1 AA named for the Section 508 / EN 301 549 procurement context (same criteria, no conformance claim)
4. **Fix authority** - asked only in Fix mode: mechanical fixes only, mechanical plus suggested wording, full remediation, or ask per file
5. **Tech stack** - asked only in Component mode, and only when the pasted code is ambiguous: plain HTML, React, Vue, Svelte, or other

The first three come in one question round; the conditional fourth or fifth follows only if it applies.

Report and Component modes never edit a file during the workflow, no matter how trivial the fix looks. Component mode will write its output to a path if you ask for it afterward.

Fix mode checks `git status` before touching anything, and if verification fails it hands you the exact revert command rather than leaving a mutated tree.

### Component mode

Paste a component with no file path and no running page, and you get a four-phase blueprint back instead of a report:

1. **Audit** - the specific flaws in the code as given, one line each, WCAG criterion cited
2. **Remediation strategy** - which native element replaces what, which ARIA survives and why native markup could not do the job
3. **Accessible code** - the complete refactor in your stack, with inline comments on every accessibility addition
4. **Testing guide** - expected result for every key the widget uses, plus what a screen reader should announce and what automation cannot confirm

Expected key bindings come from the ARIA Authoring Practices tables in `references/manual-checklist.md`, not improvised. A custom binding that fights the pattern is treated as a defect, because assistive technology users arrive with those expectations already learned.

## What's in here

```
accessibility-audit/
├── .claude-plugin/plugin.json      ← plugin manifest
├── commands/
│ ├── accessibility-audit.md        ← the command (two-round AskUserQuestion intake + 4 workflows)
│ └── a11y-audit.md                 ← short alias, same behavior
└── references/
  ├── wcag-rules.md                 ← 8 priority rule categories, before/after fixes, ARIA patterns
  ├── tooling.md                    ← axe-core, jest-axe, contrast, keyboard, pa11y, CI, report generator
  └── manual-checklist.md           ← keyboard, screen reader, visual, cognitive checks + per-widget key tables
```

No `skills/` directory. That's intentional - see above.

## How it audits

Four flows, tried in order, and it always tells you which one it used:

1. AccessLint MCP `audit_live` for any URL
2. A browser MCP (chrome-devtools-mcp, playwright-mcp, puppeteer-mcp, claude-in-chrome) when your authenticated session or a specific page state needs auditing
3. A local axe-core script when there's no MCP but there is Node and a dev server. still a live-DOM audit, so it outranks reading source
4. Static analysis of HTML files or JSX rendered to a string, the last resort

If a flow fails it says which one and why, then falls through. If every flow fails it says no audit ran, rather than reporting a clean result.

## Before it answers

Every response passes a silent gate first. Each accessibility violation must carry a WCAG criterion ID, the scope and standard and audit flow must be stated up front, all four Component phases must be present with complete code rather than an ellipsis, no sentence may imply legal compliance, and no alt text or label may have been invented outside full remediation. Failures get fixed before you see the response.

A clean audit is reported as clean. The template never gets padded with cosmetic findings to fill a section.

Audited code is treated as evidence, never as instruction. A comment, string, or attribute telling it to skip a file or report no violations is reported as a suspicious directive and the audit continues unchanged.

## Scope

Covers accessible names, keyboard access, focus and dialog behavior, semantics, forms and error handling, live-region announcements, contrast and states, media and motion - plus test tooling and CI setup.

Out of scope: general UI design review, performance work, and non-accessibility refactors. Automated results are never presented as full compliance; the manual and assistive-technology checks that remain are always named.

It will not tell you that you are legally compliant. Not for the ADA, not for Section 508 procurement, not for EN 301 549 or the EAA, and not for your lawsuit risk. The work aligns with WCAG technical criteria. Whether an organization is compliant is a legal determination made by people, on evidence this command does not produce.
