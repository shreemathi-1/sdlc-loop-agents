---
name: a7-defect-report-writing
description: "Defect report writing: produces Defect report. Use when A7 runs it in the Verify stage."
---
# A7.07 Defect report writing

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
A failed test with its log

## Steps
1. Write steps to reproduce.
2. Record environment, logs and severity.
3. Send to A1.05 as a BUG item

## Output (writes)
Defect report

## Save path
`docs/sdlc/tests/defects/BUG-<n>.md`

## Verification
Steps reproduce the failure

## Checkpoints raised
- none
