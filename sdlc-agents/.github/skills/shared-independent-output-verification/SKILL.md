---
name: shared-independent-output-verification
description: "Independent output verification: produces Verification record: item, PASS/FAIL, reason. Use when any agent runs it in any stage."
---
# S.04 Independent output verification

## Owner
Shared (used by: All)

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
An output file and the input it used

## Steps
1. Open a new chat with no prior context.
2. Compare the output with the input.
3. Mark each item PASS or FAIL with the reason.
4. Do not fix anything

## Output (writes)
Verification record: item, PASS/FAIL, reason

## Save path
`docs/sdlc/logs/verify-<file>.md`

## Verification
Every item has PASS or FAIL

## Checkpoints raised
- none
