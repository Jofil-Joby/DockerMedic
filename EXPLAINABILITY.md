# Explainability Contract: DockerMedic

## Decision

DockerMedic decides whether a recognizable Dockerfile exists when evaluating container configuration. Missing evidence is reported as a container-readiness signal with a conditional recommendation.

## Inputs

It uses the repository file list and checks for a Dockerfile artifact. The rule intentionally avoids assuming that every project must use containers.

## Limits

It does not judge image security, multi-stage optimization, runtime permissions, registry policy, or whether another container build system is appropriate. External build pipelines are not inspected.
