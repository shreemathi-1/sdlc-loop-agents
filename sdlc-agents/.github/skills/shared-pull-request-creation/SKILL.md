---
name: shared-pull-request-creation
description: "Pull request creation: produces PR description. Use when any of A5,A6 runs it in the Build stage."
---
# S.08 Pull request creation

## Owner
Shared (used by: A5,A6)

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Commits, task ID, test results

## Steps
1. Write the summary, test notes and linked task ID.
2. Attach the task gate result.
3. Open the PR

## Output (writes)
PR description

## Save path
`docs/sdlc/build/pr-<task-ID>.md`

## Verification
CI is green before review starts

## Checkpoints raised
- none
