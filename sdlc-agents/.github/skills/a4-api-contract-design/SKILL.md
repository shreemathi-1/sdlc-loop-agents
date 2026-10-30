---
name: a4-api-contract-design
description: "API contract design (OpenAPI): produces openapi.yaml. Use when A4 runs it in the Plan stage (checkpoint: CP-03)."
---
# A4.05 API contract design (OpenAPI)

## Owner
A4

## Stage
Plan

## Phase
1

## Checkpoint
CP-03

## Input (reads)
Data model, user flows from the UX spec

## Steps
1. List endpoints required by each flow.
2. Write request and response schemas.
3. Define error responses.
4. Save as OpenAPI 3

## Output (writes)
openapi.yaml

## Save path
`docs/sdlc/architecture/api/openapi.yaml`

## Verification
Contract passes the linter (A6.06)

## Checkpoints raised
- none
