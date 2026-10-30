---
name: a7-test-results-writer
description: "Test results writer: produces Test results report. Use when A7 runs it in the Verify stage."
---
# A7.08 Test results writer

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
Test runner output

## Steps
1. Count passed, failed, skipped.
2. Link each failure to a defect.
3. Write the report

## Output (writes)
Test results report

## Save path
`docs/sdlc/tests/results-<run>.md`

## Verification
Totals match the runner output

## Checkpoints raised
- none
