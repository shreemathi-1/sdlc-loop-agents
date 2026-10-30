---
name: a2-epic-decomposition
description: "Epic decomposition: produces Feature list with IDs and source reference. Use when A2 runs it in the Understand stage."
---
# A2.02 Epic decomposition

## Owner
A2

## Stage
Understand

## Phase
1

## Checkpoint
—

## Input (reads)
Epic text from the manifest

## Steps
1. Read the epic.
2. Split into features by user goal.
3. Give each feature an ID (US-001…).
4. List features that the epic does not state as TBD

## Output (writes)
Feature list with IDs and source reference

## Save path
`docs/sdlc/stories/<ID>/features.md`

## Verification
Every feature cites a sentence of the epic

## Checkpoints raised
- none
