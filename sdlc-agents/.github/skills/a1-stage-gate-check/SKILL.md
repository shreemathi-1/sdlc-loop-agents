---
name: a1-stage-gate-check
description: "Stage gate check: produces Gate result table: criterion, pass/fail, evidence path. Use when A1 runs it in any stage (checkpoint: CP-01..CP-05 trigger)."
---
# A1.03 Stage gate check

## Owner
A1

## Stage
All

## Phase
1

## Checkpoint
CP-01..CP-05 trigger

## Input (reads)
Item ID, current column, exit criteria (from kanban.md Columns table), evidence files

## Steps
1. Read the exit criteria for the column.
2. Find evidence for each criterion.
3. Mark each criterion pass or fail with the evidence path.
4. Return the result to A1.01

## Output (writes)
Gate result table: criterion, pass/fail, evidence path

## Save path
`docs/sdlc/logs/gate-<ID>-<column>.md`

## Verification
Each criterion has pass/fail and an evidence path

## Checkpoints raised
- none
