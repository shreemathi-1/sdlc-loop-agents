---
name: a8-build-and-deploy-automation
description: "Build and deploy automation: produces Deploy workflow file. Use when A8 runs it in the Release stage."
---
# A8.08 Build and deploy automation

## Owner
A8

## Stage
Release

## Phase
1

## Checkpoint
—

## Input (reads)
Build config, deploy config, environment names

## Steps
1. Write the build step.
2. Write the deploy step with secret references.
3. Run a dry-run deploy

## Output (writes)
Deploy workflow file

## Save path
`.github/workflows/deploy.yml`

## Verification
Dry-run deploy passes

## Checkpoints raised
- none
