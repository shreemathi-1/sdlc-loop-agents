---
description: Stage 4 Verify, review. Act as A8: code review, severity summary, checklist, secrets scan, design review, fix loop; request CP-06 only at the loop limit.
agent: A8-reviewer-release
---
Act as `.github/agents/A8-reviewer-release.agent.md`. Read `.github/copilot-instructions.md` first. Requires CP-04 GO in `docs/sdlc/tests/quality-summary-<ID>.md`.

## Read
- The PR diff and CI results
- `docs/sdlc/architecture/adr/ADR-*.md`, `docs/sdlc/design/<ID>/tokens.json`, `docs/sdlc/design/<ID>/components.md`
- `.github/sdlc/config.yml` (limits.fix_loop_max)
- Template: `.github/sdlc/templates/review-summary.md`

## Run, in order
1. `.github/skills/a8-pr-code-review/SKILL.md` (A8.01)
2. `.github/skills/a8-secrets-and-credential-scan/SKILL.md` (A8.05)
3. `.github/skills/a8-ui-and-design-standards-review/SKILL.md` (A8.06)
4. `.github/skills/a8-review-checklist-enforcement/SKILL.md` (A8.03)
5. `.github/skills/a8-review-summary-with-severity/SKILL.md` (A8.02)
6. `.github/skills/a8-defect-fix-loop/SKILL.md` (A8.04) — until no blocker or major is open, or the limit is reached

## Write
docs/sdlc/review/<PR>-review.md, <PR>-summary.md, <PR>-checklist.md, <PR>-secrets.md, <PR>-design.md, <PR>-loops.md.

## Checkpoint
CP-06 Fix-loop limit reached, through A1.05, only when the loop count reaches limits.fix_loop_max. Stop when the checkpoint is OPEN. Do not merge the PR.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
