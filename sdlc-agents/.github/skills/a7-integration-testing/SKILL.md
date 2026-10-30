---
name: a7-integration-testing
description: "Integration testing: produces Integration test files. Use when A7 runs it in the Verify stage."
---
# A7.04 Integration testing

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
API contract, data model, running backend

## Steps
1. Test each endpoint with real storage in a test database.
2. Test error paths.
3. Test the wiring from API client to screen

## Output (writes)
Integration test files

## Save path
`backend/tests/integration/`

## Verification
Each operation has a passing test and each error has one

## Checkpoints raised
- none
