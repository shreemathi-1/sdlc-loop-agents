---
name: a8-ci-pipeline-configuration
description: "CI pipeline configuration: produces CI workflow file. Use when A8 runs it in the Release stage."
---
# A8.07 CI pipeline configuration

## Owner
A8

## Stage
Release

## Phase
1

## Checkpoint
—

## Input (reads)
Repo build and test commands

## Steps
1. Write a workflow for lint, test and build on each PR.
2. Use secrets references only.
3. Run it on a test PR

## Output (writes)
CI workflow file

## Save path
`.github/workflows/ci.yml`

## Verification
Workflow passes on the test PR

## Checkpoints raised
- none
