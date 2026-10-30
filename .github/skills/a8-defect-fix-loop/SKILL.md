---
name: a8-defect-fix-loop
description: "Defect fix loop: produces Loop record with count. Use when A8 runs it in the Verify stage (checkpoint: CP-06)."
---
# A8.04 Defect fix loop

## Owner
A8

## Stage
Verify

## Phase
1

## Checkpoint
CP-06

## Input (reads)
Findings and the developer's fix

## Steps
1. Send findings to the developer.
2. Re-review the fix.
3. Count each loop.
4. At the limit in config, request CP-06 from a human

## Output (writes)
Loop record with count

## Save path
`docs/sdlc/review/<PR>-loops.md`

## Verification
Loop count never exceeds the config limit

## Checkpoints raised
- none
