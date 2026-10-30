---
name: a5-component-codegen-from-spec
description: "Component codegen from spec: produces Component source files. Use when A5 runs it in the Build stage."
---
# A5.02 Component codegen from spec

## Owner
A5

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Component spec (A3.05) and tokens.json (A3.04)

## Steps
1. Create each component from its spec.
2. Use tokens by name only.
3. Implement every listed state

## Output (writes)
Component source files

## Save path
`frontend/src/components/<Name>/`

## Verification
No colour, size or spacing value is hard-coded outside tokens

## Checkpoints raised
- none
