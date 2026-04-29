# codebase-to-mermaid

Point it at any codebase. Get a validated Mermaid diagram of how the code actually flows. Every node and edge is cited to a real `file:line`. No invented modules. No decorative arrows.

## Slash command

```
/codebase-to-mermaid <absolute-path-to-repo>
```

Omit the path and you'll get a picker (current working directory or specific path).

## What it does

- **Reads the whole project.** Globs the tree, reads manifest files (`package.json`, `composer.json`, `go.mod`, `Cargo.toml`, `pom.xml`, `pyproject.toml`, etc.), greps framework signals.
- **Classifies the archetype** automatically: HTTP service, CLI, data pipeline, SPA, Next.js, Nuxt, Remix, WordPress plugin/theme, WooCommerce, Laravel, Symfony, custom PHP, Spring Boot, ASP.NET Core, Go service/CLI, Rust web/CLI/WASM, Bash, WP-CLI, htmx, Alpine, Livewire, Vue SPA, C/C++/Qt/Unity, monorepo.
- **Picks the right diagram kind**: `flowchart TD` / `flowchart LR` / `sequenceDiagram` / `classDiagram`. Splits archetypes that pair (Laravel + Livewire, Go + htmx + Alpine, etc.).
- **Writes raw Mermaid** to `flow.mmd` (or `flow-<archetype>.mmd` for multi-diagram repos) directly into the target directory. The `.mmd` file has no fences, no prose - pipes straight into `mmdc -i flow.mmd -o flow.svg`.
- **Prints a Markdown report to chat**: diagram + legend (every node → `relative/path.ext:line`) + notes (external systems, async boundaries, anything skipped).
- **Caps each diagram at 40 nodes.** Bigger projects get an overview + zoomed sub-diagrams instead of one unreadable wall.
- **Flags destructive steps** (`wp db reset`, `wp search-replace`, `rm -rf`, `aws s3 rm --recursive`) with a distinct node style.

## Hard rules

- Every node carries a `file:line` citation. Unverifiable node = deleted node.
- Every edge corresponds to a real call, import, route, hook registration, or message send the model can `Grep` for. If you cannot cite it, delete the edge.
- The `.mmd` file contains only diagram source - no fences, no commentary.
- Never paraphrase the README. Read the code.
- Refuses code review, refactor proposals, bug hunts, security/performance audits, "explain this function" - those are different skills.

## Rendering the output

Two ways to view the saved `flow.mmd`:

**Online (no install):** paste contents into <https://mermaid.live>.

**On your machine (one command):**

```bash
npx -p @mermaid-js/mermaid-cli mmdc -i flow.mmd -o flow.svg
```

## What you'll get back

1. **One or more `.mmd` files** saved next to your code (`flow.mmd`, or `flow-request-lifecycle.mmd` + `flow-service-topology.mmd` for split diagrams).
2. **A diagram in chat** - rendered preview right there in Claude Code.
3. **A legend** - every node paired with its real file path and line number.
4. **A notes block** - external systems, async boundaries, anything that was too messy to map honestly.

## Layout

```
codebase-to-mermaid/
├── .claude-plugin/plugin.json
├── commands/codebase-to-mermaid.md
├── README.md
└── skills/codebase-to-mermaid/
    ├── SKILL.md
    └── references/
        ├── framework-signals.md   # exhaustive grep cheat sheet across all supported stacks
        ├── archetype-table.md     # archetype → signals → best diagram
        └── examples.md            # 24 worked archetype → diagram walkthroughs
```
