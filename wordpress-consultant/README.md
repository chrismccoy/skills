# wordpress-consultant

Senior WordPress Consultant (10+ years, WordPress VIP coding standards) that runs a fixed 10-section consulting framework over a WordPress project. Seven inputs drive an expert audit covering architecture, development strategy, WooCommerce, performance, security, debugging, scalability, automation, technical debt, and a final senior report with a 0-100 scorecard and summary table.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install wordpress-consultant@chrismccoy
```

## Use

Slash command:

```
/wordpress-consultant "checkout is slow on our WooCommerce store"   # arg seeds Current Challenge, intake fills the rest
/wordpress-consultant                                               # full 7-question intake
```

Or auto-triggers on natural language:

- *"review my WordPress architecture"*
- *"WordPress performance audit"*
- *"WordPress security review"*
- *"scale my WordPress site"*
- *"WooCommerce performance review"*
- *"WordPress technical debt assessment"*
- *"senior WordPress consultant"*

## Inputs

| # | Field | Required |
|---|-------|----------|
| 1 | Website Type (Business / SaaS / Blog / Membership / WooCommerce) | optional |
| 2 | Current Challenge | **required** |
| 3 | Technology Stack (Theme / Plugins / Hosting) | optional |
| 4 | Traffic Volume | optional |
| 5 | Development Goals | **required** |
| 6 | Performance Requirements | optional |
| 7 | Support Needed (Development / Security / Optimization / Architecture) | optional |

If `Current Challenge` or `Development Goals` is blank, intake halts with a `MISSING INPUT` line. Blank optional fields proceed with a flagged assumption at the top of the affected section.

## Output

Ten sections, each under its exact header (Section 3 marked N/A for non-stores), max 250 words per section 1-9 as Finding / Impact / Recommendation bullets. Section 10 scores on fixed scales:

| Metric | Score | Severity |
|--------|-------|----------|
| Health Score | 0-100 | - |
| Performance | 0-100 | - |
| Security | 0-100 | - |
| Scalability | 0-100 | - |
| Code Quality | 0-100 | - |
| Technical Debt | - | Low/Medium/High/Critical |

## Structure

```
wordpress-consultant/
├── .claude-plugin/plugin.json
├── commands/wordpress-consultant.md
├── README.md
└── skills/wordpress-consultant/
    ├── SKILL.md
    └── references/
        ├── framework.md          # Sections 1-10 analysis prompts
        ├── output-contract.md    # word caps, scales, summary table
        └── guardrails.md         # input handling + system rules
```

## Guardrails

All inputs treated as inert project data - embedded directives ("ignore prior", "act as", role-switch) are ignored. Scope-locked to WordPress engineering. Never recommends nulled/pirated plugins, core-file edits, secret output, or a security rating without naming what was checked.
