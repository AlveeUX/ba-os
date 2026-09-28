# Glossary

| Term | Meaning in BA-OS |
| --- | --- |
| Active project | The project named in `projects/active.md`; every `/ba-` command works on it |
| Baseline | The set of `APPROVED` items at the end of Shape and Commit; changes after it need a `CHG` |
| CHG | A change-log entry in `decisions.md` |
| Check | A run of `/ba-check`: a critic review plus a gate readiness check, saved in `checks/` |
| DEC | A decision-log entry in `decisions.md` |
| Depth | How much of a phase is done: `skip`, `light`, `standard`, `deep` |
| Evidence | The `source` and `quote` on an item; there is no separate evidence register |
| Finding (check) | A problem reported by `/ba-check`, numbered `C<run>-<n>`, for example `C3-07` |
| Finding (research) | A research result in `research/`, numbered `F-001` |
| Gate | The quality decision at the end of a phase: `PASS`, `PARTIAL`, `FAIL`, `BLOCKED` |
| GATE | A gate record in `decisions.md` |
| Item | Anything tracked in `items.md`: GOAL, PRB, NEED, REQ, RULE, FEAT, ASM, Q, RISK, DEP |
| Label | How sure we are: `KNOWN`, `ASSUMPTION`, `UNKNOWN`, `CONFLICT` |
| Lite mode | The Simple-size setup with fewer stage files and fields |
| Orphan | An item whose `parent` is missing or points to an item that does not exist |
| Phase | One of the six working phases: Intake, Discover, Define, Shape, Commit, Deliver and learn |
| Profile | `profile.md`: type, size, depth, privacy, domain notes for one project |
| Skill | A `/ba-` command, defined in `.claude/skills/<name>/SKILL.md` |
| Stage | One of the 15 reasoning steps (Qualify … Loop) inside the phases |
| Status | Who has checked an item: `AI-DRAFT` → `AI-CHECKED` → `REVIEWED` → `CONFIRMED` → `APPROVED` |
| Trace chain | GOAL → PRB → NEED → REQ → FEAT, followed through `parent` fields |
