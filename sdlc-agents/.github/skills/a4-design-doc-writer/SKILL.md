---
name: a4-design-doc-writer
description: "Design doc writer: produces Design document. Use when A4 runs it in the Plan stage (checkpoint: CP-02, CP-03)."
---
# A4.08 Design doc writer

## Owner
A4

## Stage
Plan

## Phase
1

## Checkpoint
CP-02, CP-03

## Input (reads)
ADRs, navigation, API contract, data model, UI baseline

## Steps
1. Collect the approved parts.
2. Write one design doc with a section per part.
3. Add a section of TBD items

## Output (writes)
Design document

## Save path
`docs/sdlc/architecture/design-doc-<ID>.md`

## Verification
Every section cites its source file

## Checkpoints raised
- none
