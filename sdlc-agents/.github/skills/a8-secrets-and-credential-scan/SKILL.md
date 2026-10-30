---
name: a8-secrets-and-credential-scan
description: "Secrets and credential scan: produces Scan report. Use when A8 runs it in the Verify stage."
---
# A8.05 Secrets and credential scan

## Owner
A8

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
Diff, config files, logs

## Steps
1. Run the secret scanner on the diff and config.
2. List each hit by file and line.
3. Block the PR on any hit

## Output (writes)
Scan report

## Save path
`docs/sdlc/review/<PR>-secrets.md`

## Verification
Scanner output is attached; zero hits or blocked

## Checkpoints raised
- none
