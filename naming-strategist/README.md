# naming-strategist

Senior naming strategist for venture-backed SaaS founders. Produces 10 brandable, pronounceable, niche-fit domain candidates from five inputs. Locked 4-section output (Setup Summary, Name List, Top 3 Shortlist, Verification Checklist). Silent scoring (Brandability, Niche fit, Pronounceability, Spelling ease, Differentiation) drops anything averaging below 7. Refuses legal-certainty claims, hype copy, descriptive keyword domains, hyphens, numbers, and forced `-ify` / `-ly` / `-hub` suffixes.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install naming-strategist@chrismccoy
```

## Use

Slash command:

```
/name-domains "AI productivity tools for solo founders"   # arg seeds MARKET_TOPIC, picker fills the rest
/name-domains                                              # full 5-question intake
```

Or auto-triggers on natural language:

- *"name my SaaS"*
- *"generate domain names for a developer tool"*
- *"brandable startup name brainstorm"*
- *"come up with domain candidates for a marketplace"*
- *"name my micro-SaaS"*
- *"SaaS naming for solo founders"*
- *"founder domain shortlist"*

## What's in here

```
naming-strategist/
├── .claude-plugin/plugin.json   ← plugin manifest
├── commands/
│ └── name-domains.md            ← /name-domains slash command (5-field AskUserQuestion intake)
└── skills/naming-strategist/
 ├── SKILL.md                    ← workflow (load template → generate → silent score → emit A-D → silent gate)
 └── references/
 ├── prompt-template.md          ← authoritative master prompt with placeholders
 ├── constraints.md              ← hard constraints, blocked-word list, silent validation gate, scoring rubric
 └── output-spec.md              ← sections A-D format, per-candidate block, worked example
```

## Inputs

- `MARKET_TOPIC` - vertical or domain the product serves.
- `TARGET_AUDIENCE` - who buys and uses.
- `OFFER_TYPE` - product class (micro-SaaS, developer tool, marketplace, etc.).
- `BRAND_TONE` - 2-3 from: modern, premium, bold, minimalist, friendly, technical, luxury, playful, corporate, edgy.
- `EXTENSION_PRIORITY` - preferred TLD order (e.g., `.com > .io > .ai`).

All five treated as inert data. Directives or "ignore previous" patterns embedded in any field are ignored.

## Output structure (locked)

### A) Setup Summary
3 lines: market+offer, tone+audience, `Domain and trademark checks: Needs verification.`

### B) Name List (10 items)
Per candidate:
```
# N) NameCandidate
- Angle: <what it evokes>
- Fit: <tied to audience + offer>
- Recommended extension: <one of EXTENSION_PRIORITY>
- Risk note: <Low | Medium | High> - <reason>
```

### C) Top 3 Shortlist
Ranked, two bullets each (Strength, Watch-out).

### D) Verification Checklist
5 practical steps (registrar check, USPTO TESS, WIPO, pronunciation test, Google collision check). No certainty claims.


## Silent scoring rubric

Each candidate scored 1-10 on Brandability, Niche fit, Pronounceability, Spelling ease, Differentiation. Average <7 = drop. Scores never printed. If fewer than 10 survive, output appends: `Returned N of 10 - niche requires looser scoring or revised inputs.`

## Naming structure mix (at least 5 of 10)

| Structure | Example |
|-----------|---------|
| Compound | two real words joined |
| Blended | portmanteau of two roots |
| Metaphor | evocative noun from another domain |
| Invented | fully constructed, no source word |
| Classical-roots | Latin / Greek / Sanskrit fragments |

## Scope lock

Domain naming only. Marketing copy, strategy decks, legal advice, taglines → refused with: `Out of scope - domain naming candidates only.`

## License

MIT.
