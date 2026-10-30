---
name: a6-validation-and-error-responses
description: "Validation and error responses: produces Validation layer. Use when A6 runs it in the Build stage."
---
# A6.03 Validation and error responses

## Owner
A6

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Contract error schema and validation rules from stories

## Steps
1. Validate each field against the story rule.
2. Return the contract error for each failure.
3. Log no personal data

## Output (writes)
Validation layer

## Save path
`backend/src/validation/`

## Verification
Each rule has a test that fails on bad input

## Checkpoints raised
- none
