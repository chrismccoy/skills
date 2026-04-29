---
name: code-application-blueprint
description: This skill should be used when the user asks to "create a project blueprint", "generate a technical specification", "architect an application", "create an app spec", "plan a new project", "write a technical blueprint", or any request to produce a complete technical specification document for a new application or project. Produces a 10-section specification detailed enough for both human developers and AI coding assistants to implement directly — no follow-up questions required.
version: 0.1.0
---

# Code Application Blueprint

Generate a complete Technical Project Specification — the single source of truth for building a project. Every architectural decision, file responsibility, and integration point is defined precisely enough for direct implementation with zero ambiguity.

The full 10-section output structure, rules, and specification standards live in `references/blueprint-spec.md` — load it before generating anything.

---

## Initialization Gate

All five variables are required. Use `AskUserQuestion` to collect them sequentially. Do not skip any question and do not begin generating the blueprint until all five are answered.

If any answers conflict (e.g. constraints contradict the description or the stack has a gap that blocks the project), flag the conflict and propose a resolution before proceeding.

### Variable 1: Project Description

Use `AskUserQuestion` to ask: "Describe your project — what does it do, who is it for, and what problem does it solve?"

Free-text input. The user should provide enough detail to understand the domain, users, and core value proposition.

### Variable 2: Technology Stack

Use `AskUserQuestion` with these options:

- **Node.js / Express** — JavaScript backend, REST-friendly, large ecosystem
- **Next.js** — React full-stack, SSR/SSG, API routes, Vercel-native
- **Python / FastAPI** — async Python backend, auto-generated OpenAPI docs
- **Python / Django** — batteries-included Python, ORM, admin panel
- **Go** — compiled, high-performance, minimal dependencies
- **Ruby on Rails** — convention-over-configuration, rapid prototyping
- **Laravel / PHP** — full-stack PHP, Eloquent ORM, Blade templates
- **React + Node.js** — decoupled SPA frontend with Node backend
- **Vue.js + Node.js** — decoupled SPA frontend with Node backend
- **Custom** — free-text field to specify any other stack

### Variable 3: Interfaces

Use `AskUserQuestion` with these options:

- **REST API** — HTTP endpoints, JSON request/response
- **GraphQL API** — query language, single endpoint, typed schema
- **Web UI** — browser-based user interface
- **CLI tool** — command-line interface, flag-based or interactive
- **WebSocket** — real-time bidirectional communication
- **gRPC** — binary protocol, strongly typed, service-to-service
- **REST API + Web UI** — API backend with a frontend
- **GraphQL + Web UI** — GraphQL backend with a frontend
- **Custom / Multiple** — free-text field to describe a combination

### Variable 4: Project Scale

Use `AskUserQuestion` with these options:

- **MVP** — lean, fast to ship, minimal abstraction, single environment
- **Startup** — growth-ready, some abstraction, CI/CD, basic observability
- **Enterprise** — full observability, security hardening, scaling strategy, multi-environment

### Variable 5: Constraints

Use `AskUserQuestion` to ask: "What constraints apply to this project? (e.g. budget, timeline, team size, regulatory requirements, existing infrastructure, performance targets, or 'none')"

Free-text input. Required — enter "none" if there are no constraints.

---

## Execution

1. Load `references/blueprint-spec.md` for the full output structure, section requirements, and rules.
2. Generate all 10 sections in order using the collected variable values.
3. Before delivering, verify consistency: every file in the directory structure must have a corresponding file contract, and every architectural decision must trace to specific files.
4. Deliver the complete specification as a single markdown document.

---

## Additional Resources

- **`references/blueprint-spec.md`** — 10-section output structure, per-section requirements, and specification rules
