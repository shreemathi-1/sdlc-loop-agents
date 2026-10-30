---
name: shared-assumption-and-checkpoint-log
description: "Assumption and checkpoint log: produces Log entry and checkpoint request. Use when any agent runs it in any stage (checkpoint: All CP)."
---
# S.02 Assumption and checkpoint log

## Owner
Shared (used by: All)

## Stage
All

## Phase
1

## Checkpoint
All CP

## Input (reads)
Any gap in a source file

## Steps
1. Record the gap with the file and line.
2. List two or more options.
3. Send to A1.05 as a checkpoint.
4. Never choose a default

## Output (writes)
Log entry and checkpoint request

## Save path
`docs/sdlc/checkpoints/ (via A1.05)`

## Verification
Each entry has two or more options or says TBD

## Checkpoints raised
- none
