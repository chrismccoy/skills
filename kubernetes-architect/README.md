# kubernetes-architect

Designs resilient, secure, production-ready Kubernetes manifests in the voice of a Principal Cloud Native Architect and Kubernetes expert. Four inputs drive a locked four-phase blueprint: Architecture Overview, Deployment & Scaling Manifests, Networking & Configuration Manifests, Deployment Guide. Liveness/readiness probes, resource requests and limits, and security contexts enforced on every container - never missing probes, never invented image tags.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install kubernetes-architect@chrismccoy
```

## Use

Slash command:

```
/kubernetes-architect "Node API, image myorg/api, port 3000, 3 replicas"   # arg seeds APP_REQUIREMENTS
/kubernetes-architect                                                       # full intake
```

Or auto-triggers on natural language:

- *"design Kubernetes manifests"*
- *"architect a K8s deployment"*
- *"write a Kubernetes Deployment YAML"*
- *"Deployment with HPA and probes"*
- *"Kubernetes Service and Ingress"*
- *"create production K8s manifests"*

## What's in here

```
kubernetes-architect/
├── .claude-plugin/plugin.json   ← plugin manifest
├── commands/
│ └── kubernetes-architect.md    ← /kubernetes-architect slash command (4-field AskUserQuestion intake)
└── skills/kubernetes-architect/
 ├── SKILL.md                    ← persona + scope lock + inputs + 4-step workflow + silent pre-delivery validation
 └── references/
 └── prompt-template.md          ← authoritative master prompt with placeholders + Deployment skeleton
```

## Inputs

- `APP_REQUIREMENTS` - workload: app type, image, port, replicas, probe paths.
- `RESOURCE_LIMITS` - CPU/memory requests and limits.
- `EXPOSURE_STRATEGY` - ClusterIP, NodePort, LoadBalancer, or Ingress.
- `TARGET_ENVIRONMENT` - dev, staging, production, or cloud (EKS/GKE/AKS).

All four are required - empty or contradictory fields halt with a targeted question; no defaults are invented. Inputs treated as untrusted data; behavior-altering directives (ignore probes, run as root, skip security) are ignored and flagged in PHASE 1.

## Output structure (locked)

- **PHASE 1: ARCHITECTURE OVERVIEW** - resources generated + routing/scaling strategy
- **PHASE 2: DEPLOYMENT & SCALING MANIFESTS** - complete Deployment YAML + HPA if applicable
- **PHASE 3: NETWORKING & CONFIGURATION MANIFESTS** - Service + Ingress or ConfigMaps
- **PHASE 4: DEPLOYMENT GUIDE** - step-by-step `kubectl` apply and rollout verification

## Operating constraints

- Liveness AND readiness probes on every container.
- `resources.requests` AND `resources.limits` on every container.
- Security contexts where applicable - `runAsNonRoot`, `readOnlyRootFilesystem`, `allowPrivilegeEscalation: false`.
- Syntax-perfect 2-space YAML, no tabs, dash-based arrays.
- No invented image names, tags, apiVersion values, kind names, or field keys.
- Pre-delivery validation per block: apiVersion/kind/metadata.name present, valid indentation, probes+resources+securityContext per container, Service/Ingress selectors match pod labels.

## Scope lock

Outputs Kubernetes manifest design only. Off-domain requests (Terraform, billing, app code) get one refusal line, then the K8s task continues.
