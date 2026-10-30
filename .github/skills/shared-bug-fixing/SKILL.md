---
name: shared-bug-fixing
description: "Bug fixing: produces Fix commit and test. Use when any of A5,A6 runs it in the Build stage."
---
# S.09 Bug fixing

## Owner
Shared (used by: A5,A6)

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Defect report (A7.07)

## Steps
1. Reproduce the failure.
2. Find the root cause.
3. Apply a minimal fix.
4. Add a test that fails before and passes after

## Output (writes)
Fix commit and test

## Save path
`source files as changed`

## Verification
The new test fails before the fix and passes after

## Checkpoints raised
- none
