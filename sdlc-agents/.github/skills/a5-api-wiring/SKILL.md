---
name: a5-api-wiring
description: "API wiring: produces API client and wired screens. Use when A5 runs it in the Build stage."
---
# A5.05 API wiring

## Owner
A5

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
OpenAPI contract (A4.05) and mock data (A6.05)

## Steps
1. Call only endpoints in the contract.
2. Map each response to the UI state.
3. Map each error to the error state.
4. Add no behaviour beyond the story

## Output (writes)
API client and wired screens

## Save path
`frontend/src/api/`

## Verification
Every call matches an operation in openapi.yaml

## Checkpoints raised
- none
