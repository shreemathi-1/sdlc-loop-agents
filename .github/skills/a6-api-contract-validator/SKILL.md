---
name: a6-api-contract-validator
description: "API contract validator: produces Contract validation report. Use when A6 runs it in the Verify stage."
---
# A6.06 API contract validator

## Owner
A6

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
openapi.yaml and running backend responses

## Steps
1. Run the OpenAPI linter on the contract.
2. Call each endpoint with a test request.
3. Compare each response with its schema

## Output (writes)
Contract validation report

## Save path
`docs/sdlc/tests/contract-<run>.md`

## Verification
Linter and response checks both pass

## Checkpoints raised
- none
