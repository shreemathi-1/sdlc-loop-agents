---
name: a8-review-summary-with-severity
description: "Review summary with severity: produces Severity summary. Use when A8 runs it in the Verify stage."
---
# A8.02 Review summary with severity

## Owner
A8

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
Review comments

## Steps
1. Group each finding as blocker, major, minor or nit.
2. Write the summary count

## Output (writes)
Severity summary

## Save path
`docs/sdlc/review/<PR>-summary.md`

## Verification
Every finding has a severity

## Checkpoints raised
- none
