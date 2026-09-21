# DockerMedic

> Portable agent for detecting projects without a recognizable Dockerfile.

## What it does

DockerMedic checks project structure for a Dockerfile and reports when one is absent. It is designed for repositories where containerization may be part of the intended delivery path.

### Diagnostic fingerprint

**Container artifact discovery → packaging signal → evidence → next action**

## Why this agent is distinct

DockerMedic does not assume that every project needs containers. It reports a missing Dockerfile as a diagnostic condition and frames the recommendation as conditional on container deployment needs.

## Workflow

```text
Project
   ↓
Dockerfile detector
   ↓
Containerization rule
   ↓
Evidence
   ↓
Conditional improvement plan
```

## Verification

The repository includes an OpenGAP passport, Docker-focused fixture coverage, four framework portability adapters, explainability contracts, and automated adapter tests.

OpenGAP validation passed and all four generated framework exports have been exercised successfully.

## Design principle

**Recommendations respect context.** DockerMedic separates observable absence from the assumption that Docker is mandatory.

## Medic family

DockerMedic is the containerization-focused member of a portable engineering-agent family.