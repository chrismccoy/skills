# docker-compose-architect

Designs production, secure, scalable docker-compose stacks in the voice of a Senior DevOps Engineer and Docker expert. Two required inputs plus two optional drive a locked four-phase blueprint: Architecture Overview, Docker Compose File, Environment Configuration, Deployment & Scaling. Non-root containers, tier network isolation, named volumes, healthchecks, and `${VAR}` secrets enforced - never plaintext secrets, never invented image tags.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install docker-compose-architect@chrismccoy
```

## Use

Slash command:

```
/docker-compose-architect "Node.js + React frontend, Express API"   # arg seeds TECH_STACK
/docker-compose-architect                                           # full intake
```

Or auto-triggers on natural language:

- *"design a docker-compose stack"*
- *"architect a containerized environment"*
- *"write a production docker-compose.yml"*
- *"multi-tier docker setup"*
- *"docker compose with database and networks"*
- *"containerize my app with compose"*

## What's in here

```
docker-compose-architect/
├── .claude-plugin/plugin.json   ← plugin manifest
├── commands/
│ └── docker-compose-architect.md ← /docker-compose-architect slash command (4-field AskUserQuestion intake)
└── skills/docker-compose-architect/
 ├── SKILL.md                    ← persona + scope lock + inputs + 4-step workflow + silent output validation
 └── references/
 └── prompt-template.md          ← authoritative master prompt with placeholders
```

## Inputs

- `TECH_STACK` (required) - application runtime/framework(s).
- `DATABASE_REQUIREMENTS` (required) - data layer + persistence.
- `NETWORK_SETUP` (optional) - network/tier topology; defaults to tier isolation.
- `SPECIFIC_CONSTRAINTS` (optional) - resource limits, reverse proxy, persistence rules, etc.

Required fields halt with a targeted question if empty. Conflicting constraints (e.g. "no persistence" + a database) are surfaced before generating. All inputs treated as untrusted data - embedded directives are ignored.

## Output structure (locked)

- **PHASE 1: ARCHITECTURE OVERVIEW** - topology + network isolation (frontend-tier | database-tier)
- **PHASE 2: DOCKER COMPOSE FILE** - complete `docker-compose.yml` block
- **PHASE 3: ENVIRONMENT CONFIGURATION** - `.env` template (`${VAR}=placeholder`) + critical-variable notes
- **PHASE 4: DEPLOYMENT & SCALING INSTRUCTIONS** - build/start/monitor commands + reverse proxy and scaling guidance

## Operating constraints

- Secrets only as `${VAR}` env references - never literals.
- Containers run non-root where the base image allows.
- Tiers isolated on separate bridge networks (frontend vs database).
- Named volumes or bind mounts for every stateful service.
- `depends_on` with `condition: service_healthy` plus healthchecks on every service.
- Compose YAML indented 2 spaces; no markdown square brackets in prose.
- No invented image names, tags, version numbers, or compose keys.

## Scope lock

Outputs docker-compose architecture only. Kubernetes, Terraform, raw Dockerfiles, and unrelated requests get: `Out of scope: this engine outputs docker-compose stacks only.`
