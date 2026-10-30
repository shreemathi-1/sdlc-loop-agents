---
name: a1-handoff-recorder
description: "Handoff recorder: produces Handoff file linking input and output files. Use when A1 runs it in any stage."
---
# A1.06 Handoff recorder

## Owner
A1

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
Output of a finished agent step and its verification result (S.04)

## Steps
1. Check the verification result is PASS.
2. Write the handoff file: from, to, input files, output files, open checkpoints.
3. Add the handoff path to the item in kanban.md

## Output (writes)
Handoff file linking input and output files

## Save path
`docs/sdlc/handoffs/<ID>-<from>-to-<to>.md`

## Verification
Every output file listed exists at its path

## Checkpoints raised
- none
