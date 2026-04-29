# explain-my-code

Point it at any codebase. Get back one self-contained Markdown document that anyone new to the project can read cover-to-cover and actually understand the system, no guesswork.

## Slash command

```
/explain-my-code <absolute-path-to-repo>
```

Omit the path and you'll get a picker (current working directory or a specific path).

## What it does

- **Reads the whole project.** Globs the tree, reads manifest files first (`package.json`, `composer.json`, `go.mod`, `Cargo.toml`, `pom.xml`, `pyproject.toml`, `*.csproj`, Dockerfile, CI configs), then walks folder-by-folder.
- **Figures out the shape.** Tech stack, languages, frameworks, and whether you're looking at a monolith, microservices, or a modular setup.
- **Traces how it actually runs.** Entry points, startup sequence, request lifecycle, auth flow, and data flow from input → processing → storage.
- **Names real things.** Every component, class, and function in the doc is a real symbol from your repo - no `MyApp`, no `FooService` placeholders.
- **Draws the diagrams.** Embeds Mermaid `graph TD` for architecture and `sequenceDiagram` for flows, right inside the document.
- **Writes one file.** Saves `CODEBASE_DOCUMENTATION.md` to your repo root and tells you the path.

## What you'll get back

A single `CODEBASE_DOCUMENTATION.md` with 13 sections, always in this order:

1. **Project Overview** - what it does and who it's for
2. **System Architecture** - the big picture, with a diagram
3. **Repository Structure** - what every major folder is for
4. **Tech Stack & Dependencies** - languages, frameworks, libraries
5. **Core Components / Services** - responsibilities and how they talk to each other
6. **Application Flow** - startup, request, auth, and data flow (with a sequence diagram)
7. **Key Design Patterns** - what patterns are used, where, and why
8. **Database & Models** - schema and entity relationships
9. **External Integrations** - APIs, third-party services, queues, caches
10. **Configuration & Environment** - env vars and config files
11. **Build & Deployment** - how it's built and shipped
12. **Observations & Risks** - code smells, tight coupling, scalability concerns
13. **Suggestions for Improvement** - where to go next

## Hard rules

- **No skipped sections.** If something doesn't apply (say, there's no database), the heading stays and it says `Not applicable - <reason>`.
- **No invented symbols.** Every file, class, and function named in the doc is verifiable in your repo.
- **No silent guessing.** When behavior is undocumented, it's inferred out loud - the assumption is stated in the text.
- **Skips the noise.** `node_modules`, `vendor`, `dist`, and `build` are excluded and noted as skipped.
- **Stays in its lane.** Refuses line-by-line code review, bug hunts, refactor plans, and diagram-only output - those are different skills.

## Big repo? No problem

If the project is too large to read in one pass, it analyzes in chunks - manifests and entry points first, then module by module - and is honest about anything it sampled rather than read in full.

## Layout

```
explain-my-code/
├── .claude-plugin/plugin.json
├── commands/explain-my-code.md
├── README.md
└── skills/explain-my-code/
    └── SKILL.md
```
