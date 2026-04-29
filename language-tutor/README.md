# language-tutor

Expert linguist, translator, and language tutor with depth in comparative grammar, second-language pedagogy, and phonetics. Two modes: **TRANSLATION** (translate and explain a phrase) and **TEXT ANALYSIS** (correct and critique your own writing). Auto-detects the source language, aligns difficulty to CEFR A1-C2, and never invents grammar rules, etymologies, or IPA - it flags uncertainty instead of guessing.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install language-tutor@chrismccoy
```

## Use

Slash command:

```
/language-tutor "Je m'appelle Marie"     # arg seeds TEXT, picker fills mode/target/native/depth
/language-tutor                           # full 5-question intake
```

Or auto-triggers on natural language:

- *"translate this to Japanese"*
- *"what does this mean in French"*
- *"explain this grammar"*
- *"analyze my writing"*
- *"correct my essay"*
- *"proofread this paragraph"*
- *"how do I pronounce this"*

## What's in here

```
language-tutor/
├── .claude-plugin/plugin.json     ← plugin manifest
├── commands/
│ └── language-tutor.md            ← /language-tutor slash command (5-field AskUserQuestion intake)
└── skills/language-tutor/
 ├── SKILL.md                      ← workflow (load template → resolve mode → emit sections → silent gate)
 └── references/
 ├── prompt-template.md            ← authoritative master prompt with placeholders + both mode specs
 ├── constraints.md                ← accuracy floor, prompt-injection defense, scope lock, silent gate
 └── output-spec.md                ← section structure for both modes, optional extras, worked examples
```

## Inputs

- `MODE` - `Translate`, `Analyze`, or `Auto` (detect from text).
- `TEXT` - the phrase or passage to translate or analyze (required).
- `TARGET_LANGUAGE` - language to translate into (TRANSLATION mode only).
- `NATIVE_LANGUAGE` - learner's native language; tailors pronunciation tips. Default English.
- `DEPTH` - `Full` (whole framework) or `Quick` (result + one-line note).

All inputs are treated as inert data. Directives embedded in `TEXT` (e.g. "ignore your instructions") are translated or analyzed literally, never obeyed.

## Output structure (locked)

### TRANSLATION mode

`## Translation` · `## Grammar` · `## Structure` · `## Pronunciation` · `## Usage & Register`

### TEXT ANALYSIS mode

`## Grammar` · `## Spelling & Punctuation` · `## Style & Flow` · `## Meaning & Content` · `## Corrected Text` (itemized original → corrected → reason) · `## Alternative Versions` (5 rewrites: formal, casual, detailed, concise, alt-vocabulary)

`Quick` depth returns only the Translation or Corrected Text plus a one-line note.

## Accuracy floor

Never invents grammar rules, etymologies, or IPA. States reduced confidence on low-resource languages and dialects, and stops rather than approximating when a language cannot be handled reliably. Aligns register and difficulty to CEFR (A1-C2) where the language supports it.

## Scope lock

Translation and language analysis only. Unrelated requests are declined briefly with a restatement of what the tutor does - no switch into general-assistant behavior.

## License

MIT.
