---
name: a6-backend-container-and-deploy-config
description: "Backend container and deploy config: produces Dockerfile and deploy config. Use when A6 runs it in the Release stage."
---
# A6.08 Backend container and deploy config

## Owner
A6

## Stage
Release

## Phase
1

## Checkpoint
—

## Input (reads)
Backend build and env variable names

## Steps
1. Write a Dockerfile for the backend.
2. Write deploy config with secret references only.
3. Build the image locally

## Output (writes)
Dockerfile and deploy config

## Save path
`deploy/backend/`

## Verification
Image builds; no secret value appears in any file

## Checkpoints raised
- none
