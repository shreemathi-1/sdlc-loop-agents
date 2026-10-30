---
name: shared-task-gate-and-commit
description: "Task gate (lint, types, unit tests) and commit: produces Task gate result file. Use when any of A5,A6 runs it in the Build stage."
---
# S.07 Task gate (lint, types, unit tests) and commit

## Owner
Shared (used by: A5,A6)

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Code changes for one task

## Steps
1. Run lint.
2. Run the type check.
3. Run the unit tests.
4. Commit only if all three pass

## Output (writes)
Task gate result file

## Save path
`docs/sdlc/build/task-gate-<task-ID>.md`

## Verification
All three results are recorded as pass

## Checkpoints raised
- none
