---
name: a6-backend-environment-config-and-seed
description: "Backend environment config and seed: produces Config template and seed script. Use when A6 runs it in the Build stage."
---
# A6.07 Backend environment config and seed

## Owner
A6

## Stage
Build

## Phase
1

## Checkpoint
—

## Input (reads)
Environment variable names and seed data

## Steps
1. List variable names with no values.
2. Add a template env file with placeholders.
3. Add a seed script for synthetic data

## Output (writes)
Config template and seed script

## Save path
`backend/config/`

## Verification
Template holds no real values; seed script runs

## Checkpoints raised
- none
