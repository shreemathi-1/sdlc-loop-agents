# Folder tree

| Path | Kind | Purpose | Who writes | When |
|---|---|---|---|---|
| `.github/copilot-instructions.md` | file | Workspace rules every chat sees: R1–R10, checkpoint rule, folder map, never write kanban.md except A1 | Build once | Phase 1 build |
| `.github/agents/A1-orchestrator.agent.md … A8-reviewer-release.agent.md` | 8 files | One custom agent per role: name, role, stage, inputs, outputs, permissions, cannot-do list, skills it owns, which checkpoints it requests | Build once | Phase 1 build |
| `.github/skills/<id>-<slug>/SKILL.md` | 117 agent-owned folders (67 in phase 1) | One skill per folder: frontmatter (name, description), inputs, steps, output, save path, verification, checkpoint, phase | Build per phase | Each phase |
| `.github/skills/shared-*/SKILL.md` | 13 shared folders (10 in phase 1); 130 total, 77 in phase 1 | Skills used by two or more agents (S.01–S.13); agent files reference them by name | Build per phase | Each phase |
| `.github/prompts/sdlc-intake.prompt.md, sdlc-understand.prompt.md, sdlc-plan-design.prompt.md, sdlc-plan-architecture.prompt.md, sdlc-build-backend.prompt.md, sdlc-build-frontend.prompt.md, sdlc-verify-tests.prompt.md, sdlc-verify-review.prompt.md, sdlc-release.prompt.md, sdlc-verify-output.prompt.md` | 10 files | One prompt per stage: which agent to act as, which files to read, which skills to run in order, which files to write, which checkpoint to request. sdlc-verify-output runs S.04 in a fresh chat | Build once | Phase 1 build |
| `.github/instructions/sdlc-docs.instructions.md (applyTo docs/sdlc/**), frontend.instructions.md (applyTo frontend/**), backend.instructions.md (applyTo backend/**), tests.instructions.md (applyTo tests/**)` | 4 files | Path-scoped rules: TBD and PROPOSED labels in docs, tokens-only styling in frontend, no secrets in backend, traceability IDs in tests | Build once | Phase 1 build |
| `.github/sdlc/config.yml` | file | Team values the skills read: fix-loop limit, approver roles per checkpoint, Definition of Ready, coverage threshold, test runner, lint command, kanban columns and exit criteria, estimation scale | Human fills | Before first run |
| `.github/sdlc/templates/` | folder | Templates for: checkpoint, handoff, story, acceptance criteria, ADR, design doc, test plan, defect, review summary, release checklist | Build once | Phase 1 build |
| `.github/sdlc/README.md` | file | How to install the folder in a new repo, how to start a story, how checkpoints work, the stage order | Build once | Phase 1 build |
| `.github/sdlc/plan/ (skills.csv, agents.md, checkpoints.md, stage_flow.md, board.png)` | folder | The Claude Code input pack: this plan as CSV, markdown and PNG. Claude Code reads these to build the agents and skills | Me, after CP-00 | Before phase 1 build |
| `docs/sdlc/plan/ (SDLC_Agent_Project_v2.pptx, SDLC_Agent_Skills_Plan_v2.xlsx, PROJECT_UNDERSTANDING_v2.md)` | folder | The plan for people: deck, workbook, understanding doc. Claude Code does not read these | Human | Before phase 1 build |
| `docs/sdlc/kanban.md` | file (per project) | The board. Columns table with exit criteria, items, History. Written only by A1 | A1 at every move | Runtime |
| `docs/sdlc/inputs/<ID>/` | folder (per project) | Where a human drops the story, epic, screenshots or Figma link | Human | Runtime |
| `docs/sdlc/{stories,design,architecture,build,tests,review,release,checkpoints,handoffs,logs}/` | folders (per project) | All agent outputs, one folder per stage, so a new teammate can read the trail | Agents | Runtime |
