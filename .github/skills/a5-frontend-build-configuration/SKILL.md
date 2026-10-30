---
name: a5-frontend-build-configuration
description: "Frontend build configuration: produces Build config and build log. Use when A5 runs it in the Build stage."
---
# A5.06 Frontend build configuration

## Owner
A5

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Stack from the ADR, environment variable list

## Steps
1. Set build tool settings for the stack.
2. Add env variable names with no values.
3. Run the build

## Output (writes)
Build config and build log

## Save path
`frontend/ (build config files)`

## Verification
Build succeeds on a clean checkout

## Checkpoints raised
- none
