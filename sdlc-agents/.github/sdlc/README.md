# SDLC agent system (phase 1)

Copilot customization files that run a story through Understand → Plan → Build → Verify → Release with eight agents and human checkpoints. Rules: `.github/copilot-instructions.md`. Plan: `.github/sdlc/plan/`.

## 1. Install

1. Copy the whole `.github/` folder into the root of the target repository.
2. Open the repository in VS Code with GitHub Copilot Chat. Agents appear from `.github/agents/`, prompts from `.github/prompts/`, skills from `.github/skills/`.
3. Do not create `docs/sdlc/` by hand; the bootstrap prompt does it.

## 2. Fill the config

Edit `.github/sdlc/config.yml`. Replace every `TBD` you can: `project.name`, `project.platform`, approver names per checkpoint. `stack`, `commands` and `coverage_threshold` stay TBD until CP-03. Agents read this file and never write it.

## 3. Run bootstrap

In a new chat, run `/sdlc-bootstrap` (`.github/prompts/sdlc-bootstrap.prompt.md`). It acts as A1 and creates `docs/sdlc/` with `kanban.md` and the stage folders. It stops if a required config value is missing.

## 4. Run intake

1. Drop the input in `docs/sdlc/inputs/<ID>/` (`story.md`, `epic.md`, `screenshots/*.png`). A sample is `.github/sdlc/plan/sample_story_T-01.md`.
2. In a new chat, run `/sdlc-intake`. A1 adds the item to Backlog and routes it to A2.
3. In a new chat, run `/sdlc-understand`. A2 writes `docs/sdlc/stories/<ID>/` and requests CP-01.
4. Continue one stage per chat: `/sdlc-plan-design`, `/sdlc-plan-architecture`, `/sdlc-build-backend`, `/sdlc-build-frontend`, `/sdlc-verify-tests`, `/sdlc-verify-review`, `/sdlc-release`.
5. Before every handoff, run `/sdlc-verify-output` in a fresh chat on the output file (R4).

## 5. How checkpoints work

- A checkpoint is a human decision. Agents only request one; A1 writes the file `docs/sdlc/checkpoints/<CP-ID>-<name>.md` with Status `OPEN` from `.github/sdlc/templates/checkpoint.md`.
- The item is blocked while the file is `OPEN`. The approver named in `config.yml` reads the evidence paths in the file, then writes `APPROVED` or `REJECTED`, their name, the date and the decision. No agent ever writes `APPROVED`.
- After the decision, start the next stage prompt in a new chat. A `REJECTED` checkpoint sends the item back to the author skill.
- CP-07 is raised for every `TBD` an agent finds. The value stays `TBD` and dependent items stay blocked until it is answered.
- The full checkpoint table is `.github/sdlc/plan/checkpoints.md`; the stage order and kanban exit criteria are `.github/sdlc/plan/stage_flow.md`.
