---
name: shared-source-traceability-check
description: "Source traceability check: produces Traceability report. Use when any agent runs it in any stage."
---
# S.01 Source traceability check

## Owner
Shared (used by: All)

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
Any output file and its source IDs

## Steps
1. Check each item cites an input ID, file or line.
2. Flag each item with no source as TBD

## Output (writes)
Traceability report

## Save path
`docs/sdlc/logs/traceability-<file>.md`

## Verification
Zero untraced items, or each is flagged

## Checkpoints raised
- none
