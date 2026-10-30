---
name: shared-decision-request
description: "Decision request (human): produces Decision request in a checkpoint file. Use when any agent runs it in any stage (checkpoint: All CP)."
---
# S.03 Decision request (human)

## Owner
Shared (used by: All)

## Stage
All

## Phase
1

## Checkpoint
All CP

## Input (reads)
Options with trade-offs

## Steps
1. Write each option with its trade-off.
2. Give the PROPOSED default and reason.
3. Stop until a named person decides

## Output (writes)
Decision request in a checkpoint file

## Save path
`docs/sdlc/checkpoints/CP-xx-<name>.md`

## Verification
Request names who decides and what file they read

## Checkpoints raised
- none
