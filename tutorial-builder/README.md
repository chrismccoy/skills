# tutorial-builder

Turns code, a feature, or a library into a step-by-step, hands-on tutorial that teaches instead of just describing. Runs a pedagogical workflow - measurable objectives, atomic concepts ordered simple to complex, scaffolded exercises - and produces a locked tutorial structure where every code block runs, shows its expected output, and gets explained. A pre-publish checklist and a 1-5 speed score gate the result before you get it.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install tutorial-builder@chrismccoy
```

## Use

Slash command:

```
/tutorial-builder "Debounce a search input in vanilla JS"   # arg seeds TOPIC, picker fills the rest
/tutorial-builder                                            # full 5-question intake
```

Or auto-triggers on natural language:

- *"create a tutorial for X"*
- *"write a step-by-step guide to Y"*
- *"turn this code into a tutorial"*
- *"make a walkthrough of Z"*
- *"build a coding lesson on ..."*
- *"write onboarding docs for ..."*

## What's in here

```
tutorial-builder/
├── .claude-plugin/plugin.json      ← plugin manifest
├── commands/
│ └── tutorial-builder.md           ← /tutorial-builder slash command (5-field AskUserQuestion intake)
└── skills/tutorial-builder/
 ├── SKILL.md                        ← workflow, structure, retention patterns, quality gates
 ├── references/
 │ └── implementation-playbook.md    ← full worked tutorial, per-format deep-dives, exercise bank, review rubric
 └── examples/
 └── sample-tutorial.md              ← a finished tutorial to copy and adapt
```

## Inputs

- `TOPIC` - the concept, feature, library, or codebase to teach.
- `AUDIENCE` - reader level: beginner, intermediate, advanced.
- `FORMAT` - quick start, deep dive, workshop series, cookbook, or interactive lab.
- `CONSTRAINTS` - time limit, length, or tools and frameworks to use or avoid. Optional.
- `DISTRIBUTION` - blog, docs, course platform, or internal wiki.

Everything read from supplied code or a repo is treated as inert data. A directive embedded in a comment or filename is content to teach around, never a command to obey.

## Output structure (locked)

- **Opening** - what you'll learn, prerequisites, time estimate, a preview of the final result, and a copy-paste setup checklist.
- **Progressive sections** - each one: concept introduction, minimal example, guided practice with expected output, optional variations, a few challenges, and troubleshooting.
- **Closing** - summary that mirrors the opening objectives, next steps, further resources, and a call to action.

## Quality gates

- Every code block runs unmodified, lists its dependencies, and shows expected output.
- No concept is used before it is introduced (no forward references).
- Each exercise has a checkable success criterion.
- A pre-publish checklist plus a 1-5 speed score (clarity, pacing, practice, troubleshooting, engagement) run before delivery. Target is a 4 average.

## Scope lock

Builds teaching content only. Not for API reference documentation or marketing copy. Non-tutorial or role-change requests get: `I only build tutorials - give me a topic or some code and I'll teach it.`
