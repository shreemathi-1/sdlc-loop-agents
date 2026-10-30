---
name: a6-api-endpoint-implementation
description: "API endpoint implementation: produces Endpoint handlers. Use when A6 runs it in the Build stage."
---
# A6.02 API endpoint implementation

## Owner
A6

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
OpenAPI contract (A4.05) and data model

## Steps
1. Implement each operation in the contract.
2. Validate input.
3. Return the contract error shape

## Output (writes)
Endpoint handlers

## Save path
`backend/src/api/`

## Verification
Each handler matches its contract operation

## Checkpoints raised
- none
