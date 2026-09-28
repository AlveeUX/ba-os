---
name: ba-status
description: Show where the active BA-OS project stands and the next required action. Rebuilds control.md from items.md, decisions.md and profile.md. Can also switch the active project. Use when the user asks for project status, what to do next, or where things stand.
argument-hint: "[project-id to switch to]"
allowed-tools: Read Write Edit Glob Grep
---

# /ba-status — rebuild the control center and suggest the next action

## 1. Choose the project

- If `$ARGUMENTS` names a project ID, find its folder in `projects/` or `projects/_confidential/`, write that path as the only line of `projects/active.md`, and tell the user the active project changed.
- Otherwise use the project in `projects/active.md`. If there is none, list the project folders and ask which one to use.

## 2. Read

`profile.md`, `items.md`, `decisions.md`, the current `control.md`, the latest report in `checks/`, the file list of `inputs/`, and `method/phases.md` (next-action rules).

## 3. Rebuild `control.md`

Rewrite every section of `control.md` from the data. Keep the **Notes** section exactly as it is.

- **Current phase**: the lowest phase whose gate is not `PASS` or `PARTIAL` (from GATE entries in `decisions.md`), skipping phases with depth `skip`.
- **Next required action**: the first rule in "Next-action rules" in `method/phases.md` that applies, written as one concrete instruction (name the command, items or sections).
- **Blockers**: GATE entries with `BLOCKED`, DEP items that block the current phase, and high findings from the last check.
- **Overall confidence**: `low`, `medium` or `high`, with one line of reasoning based on the share of KNOWN vs ASSUMPTION/UNKNOWN/CONFLICT items in the current and earlier phases, and on open high findings. This is a judgement: say what drives it.
- **Project** table: from `profile.md` and GOAL items.
- **Gates** table: depth from `profile.md`; result and date from the latest GATE entry for each phase.
- **Counts**: count items by status, and open items (not REJECTED or SUPERSEDED) by label. Count carefully by reading every item's `status` and `label` lines.
- **Top open questions**: up to five unanswered Q items, MVP-related first, with ID, question and who to ask.
- **Top risks**: up to five RISK items, highest impact first.
- **Recent decisions**: the last five DEC, CHG or GATE entries (ID, date, one line).
- **Input log**: keep existing rows; add any file in `inputs/` that is missing, with "Extracted on" empty.
- **Last check**: from the latest report in `checks/`.
- **Last updated**: today.

## 4. Report back

Print a short summary for the user (under 12 lines):

```
Project: <ID> — <name>
Phase: <n>. <name> · Gate: <result or not started>
Next: <next required action>
Blockers: <none or list>
Items: <n> total · <n> AI-DRAFT · <n> AI-CHECKED · <n> REVIEWED · <n> APPROVED
Open questions: <n> (top: Q-…)
Confidence: <level> — <reason>
```
