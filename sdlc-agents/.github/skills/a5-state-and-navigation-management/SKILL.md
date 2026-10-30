---
name: a5-state-and-navigation-management
description: "State and navigation management: produces State and routing modules. Use when A5 runs it in the Build stage."
---
# A5.04 State and navigation management

## Owner
A5

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Architecture ADR for state and routing

## Steps
1. Apply the chosen state pattern from the ADR.
2. Apply the chosen routing pattern.
3. Do not mix patterns

## Output (writes)
State and routing modules

## Save path
`frontend/src/state/, frontend/src/routes/`

## Verification
Lint rule set from config shows no mixed pattern

## Checkpoints raised
- none
