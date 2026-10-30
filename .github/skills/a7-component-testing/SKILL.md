---
name: a7-component-testing
description: "Component testing: produces Component test files. Use when A7 runs it in the Verify stage."
---
# A7.03 Component testing

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
Component specs and source

## Steps
1. Render each component alone.
2. Test each listed state.
3. Test each label and role

## Output (writes)
Component test files

## Save path
`frontend/tests/components/`

## Verification
Each state has a test

## Checkpoints raised
- none
