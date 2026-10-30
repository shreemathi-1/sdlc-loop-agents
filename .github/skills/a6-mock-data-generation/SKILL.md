---
name: a6-mock-data-generation
description: "Mock data generation: produces Synthetic seed data. Use when A6 runs it in the Build stage."
---
# A6.05 Mock data generation

## Owner
A6

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Data model and API contract

## Steps
1. Generate rows that match the model.
2. Label every row SYNTHETIC.
3. Use no real personal data

## Output (writes)
Synthetic seed data

## Save path
`backend/seed/synthetic/`

## Verification
Every seed file has a SYNTHETIC label

## Checkpoints raised
- none
