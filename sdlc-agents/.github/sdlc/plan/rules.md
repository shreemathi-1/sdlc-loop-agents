# Rules

- **R1 Traceability.** Every output item cites its source: input ID, file, line, screenshot region or Figma node.
- **R2 No invented values.** A value the source does not give is written TBD and raised as a CP-07 checkpoint. Never guessed.
- **R3 Humans decide.** Agents propose options. A named person records each decision with a date in the checkpoint file.
- **R4 Fresh-context verification.** Before every handoff, S.04 runs in a new chat and compares output with input.
- **R5 Checkpoints are human.** No agent sets a checkpoint to APPROVED. A1 writes OPEN and blocks the item until a human answers.
- **R6 Loop limit.** Fix loops stop at the limit in config.yml (PROPOSED 3) and raise CP-06.
- **R7 Tool over opinion.** Lint, tests, scans and linters decide. Their output is attached to the handoff.
- **R8 Visible uncertainty.** Every output file ends with a 'Checkpoints raised' section, even if empty.
- **R9 Separation of duties.** The agent that reviews a change does not approve its release; a developer does not merge its own PR.
- **R10 Labeled proposals.** A default chosen by an agent is marked PROPOSED with a reason until a checkpoint approves it.
- **R11 Token-optimized development.** A skill reads only the files named in its INPUT, never a whole folder. It writes only the template fields, cites files by path instead of pasting them, and keeps each output under the length set in config.yml. Shared skills load only when called. One stage per chat; verification runs in a fresh chat with only the input and output files.
