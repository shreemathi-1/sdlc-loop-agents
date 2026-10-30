---
name: a6-data-model-and-migrations
description: "Data model and migrations: produces Migration files. Use when A6 runs it in the Build stage (checkpoint: CP-03)."
---
# A6.01 Data model and migrations

## Owner
A6

## Stage
Build

## Phase
1

## Checkpoint
CP-03

## Input (reads)
Data model (A4.04)

## Steps
1. Write a migration per entity.
2. Add keys and constraints from the data model.
3. Run the migration on an empty database

## Output (writes)
Migration files

## Save path
`backend/migrations/`

## Verification
Migration runs on an empty database with no error

## Checkpoints raised
- none
