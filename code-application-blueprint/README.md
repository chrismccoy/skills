# code-application-blueprint

Generates a complete technical project specification — detailed enough for both human developers and AI coding assistants to implement directly.

Part of the [`chrismccoy-skills`](../README.md) Claude Code marketplace. Full description and usage examples in the [marketplace root README](../README.md#code-application-blueprint).

## Install

```
/plugin marketplace add github:chrismccoy/skills
/plugin install code-application-blueprint@chrismccoy-skills
```

## Use

```
/code-application-blueprint                              ← walks through all five questions
/code-application-blueprint "A time-tracking SaaS app"  ← pre-fills the project description
```

Or just describe what you want — the skill auto-triggers on natural language like *"create a project blueprint for my app"*, *"generate a technical spec for a REST API"*, or *"architect a new project for me"*.

## What's in here

```
commands/code-application-blueprint.md          ← /code-application-blueprint slash command
skills/code-application-blueprint/
├── SKILL.md                                    ← initialization gate + execution workflow
└── references/
    └── blueprint-spec.md                       ← 10-section output structure and rules
CHANGELOG.md                                    ← release notes
```

## How it works

1. **Initialization Gate** — five required questions, all collected via `AskUserQuestion` before any generation begins:
   - Project description (free text)
   - Technology stack (multiple choice: Node/Express, Next.js, FastAPI, Django, Go, Rails, Laravel, React+Node, Vue+Node, or custom)
   - Interfaces (multiple choice: REST API, GraphQL, Web UI, CLI, WebSocket, gRPC, combinations, or custom)
   - Project scale (multiple choice: MVP, Startup, Enterprise)
   - Constraints (free text — budget, timeline, regulatory, etc., or "none")
2. **Conflict check** — if any answers conflict (e.g. constraints contradict the description), flags the conflict and proposes a resolution before proceeding
3. **Generation** — produces all 10 sections in order: Project Overview, Scope Contract, Architecture Overview, Dependency Map, Directory Structure, File Contracts, Data Models, Risk and Failure Map, Testing Strategy, Setup and Run
4. **Consistency check** — verifies every file in the directory structure has a corresponding file contract and every architectural decision traces to specific files before delivering
5. **Delivery** — single markdown document, no TBD, no placeholders, no unresolved items

## Changelog

See [`CHANGELOG.md`](CHANGELOG.md) for release history.

## License

GPL-2.0-or-later. See the [LICENSE](../LICENSE) file at the repo root.
