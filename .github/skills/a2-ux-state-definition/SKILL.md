---
name: a2-ux-state-definition
description: "UX state definition: produces State matrix: screen \u00d7 state. Use when A2 runs it in the Understand stage."
---
# A2.07 UX state definition

## Owner
A2

## Stage
Understand

## Phase
1

## Checkpoint
—

## Input (reads)
Screen inventory and stories

## Steps
1. For each screen check loading, empty, error, offline, permission-denied.
2. Write the state text the source gives.
3. Mark unknown states TBD and add a checkpoint entry

## Output (writes)
State matrix: screen × state

## Save path
`docs/sdlc/stories/<ID>/ux-states.md`

## Verification
Every screen has all five states, each stated or TBD

## Checkpoints raised
- none
