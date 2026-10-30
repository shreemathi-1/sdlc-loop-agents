---
name: a5-screen-implementation
description: "Screen implementation: produces Screen source files. Use when A5 runs it in the Build stage."
---
# A5.03 Screen implementation

## Owner
A5

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Layout plan, navigation map, UX spec and states

## Steps
1. Build each screen from its layout plan.
2. Implement loading, empty, error and permission-denied states.
3. Use the navigation map for routes

## Output (writes)
Screen source files

## Save path
`frontend/src/screens/<Name>/`

## Verification
Each screen implements every state from A2.07

## Checkpoints raised
- none
