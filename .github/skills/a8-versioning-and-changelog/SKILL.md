---
name: a8-versioning-and-changelog
description: "Versioning and changelog: produces CHANGELOG entry. Use when A8 runs it in the Release stage."
---
# A8.09 Versioning and changelog

## Owner
A8

## Stage
Release

## Phase
1

## Checkpoint
—

## Input (reads)
Merged PRs since the last release

## Steps
1. Choose the version bump from change types.
2. Write changelog entries from PR titles.
3. Link each entry to its PR

## Output (writes)
CHANGELOG entry

## Save path
`CHANGELOG.md`

## Verification
Every entry links to a PR

## Checkpoints raised
- none
