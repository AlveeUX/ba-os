---
name: ba-learn
description: Learn from a project and improve BA-OS. Reads a BA-OS project (or a project done outside BA-OS) — decisions, gate records, every check report, superseded and rejected items, conflicts and wrong assumptions — drafts lessons into knowledge/lessons.md, and proposes changes to checklists, templates and skills for the user to accept. Can run at any gate, not only at the end.
argument-hint: "[project-id | path to an outside project folder]"
disable-model-invocation: true
allowed-tools: Read Write Edit Glob Grep
---

# /ba-learn — turn a project into lessons and BA-OS improvements

This is the **Learn** and **Loop** stage (`method/phases.md`). It can run at any gate, and should run whenever a project stops early (lost bid, paused, cancelled, or a practice exercise) — not only in Phase 6. Lessons it writes start as `AI-DRAFT`; only the user approves them with `/ba-approve lesson …`.

The user typed: `$ARGUMENTS`

## 1. Choose the source

- **Empty:** the active project (`projects/active.md`).
- **A project ID:** that folder in `projects/` or `projects/_confidential/`.
- **A path to a folder outside `projects/`** (for example a project done before BA-OS, or a portfolio repository): treat it as an **outside project**. Read it only; never edit, move or delete anything in it.

If the source cannot be found, list the project folders and stop.

## 2. Read

**BA-OS project:** `profile.md`, `items.md`, `decisions.md`, every report in `checks/` (oldest first), every stage file, and the Input log in `control.md`.

**Outside project:** its README and every text document (`.md`, `.txt`, `.csv`); skip binary files and say which were skipped. There are no items or checks, so evidence will cite file paths.

**Always:** `knowledge/lessons.md` and every file in `knowledge/patterns/`, so you do not repeat a lesson or a question that already exists.

## 3. Look for lessons

Look for evidence of these, and note the item, finding, decision or file that shows it:

| Look for | Where it shows |
| --- | --- |
| Assumptions that turned out wrong | ASM items `SUPERSEDED` or `REJECTED`; labels changed from `ASSUMPTION` |
| Questions asked too late | A Q created in a late check that a checklist question would have caught at Intake |
| Problems that kept coming back | The same finding in three or more check reports |
| Risks carried from gate to gate | The same `open-risks` in several `PARTIAL` GATE entries |
| Answers or contacts that never arrived | Q or DEP items open across two or more client rounds |
| Sources that disagreed | `CONFLICT` items, and how they were settled |
| Scope that moved | `CHG` entries; requirements that changed priority; superseded REQ items |
| Estimate accuracy | Estimated range versus actual effort, if known |
| Gaps in BA-OS itself | Work the user had to do by hand because no template, section or command covered it; a gate recorded while its stage file was still empty |

Keep only lessons that would **change what BA-OS does next time**. Usually three to seven per run. A finding about this one project's content is not a lesson; a pattern that a checklist question, template section or command rule would have caught is.

## 4. Draft the lessons

Add each lesson at the bottom of `knowledge/lessons.md`, numbered after the highest existing `L-` number, in the format at the top of that file:

- `status: AI-DRAFT`.
- `evidence`: the project ID with item, finding, DEC or GATE IDs; for an outside project, a short description and the file paths.
- `check-question`: one question `/ba-check` can ask on a future project to catch this early.
- `proposed-change`: the exact BA-OS file and the text to add or change.
- `change made to BA-OS`: `none yet`.
- `history`: `<date> drafted by /ba-learn from <source>`.

**Privacy:** never write client names, company names, people's names, prices, budgets or personal data into `knowledge/`. Describe them by role ("the owner", "the client's accountant") and by type ("a multi-hotel booking site"). Check every lesson for this before saving; if the source project is `confidential`, check twice.

If a lesson already exists that says the same thing:
- If it is `AI-DRAFT`, add the new evidence to it.
- If it is `APPROVED`, do not change its text. Add one line to its `evidence` and one `history` line, and tell the user.

## 5. Propose changes to BA-OS

Show the user a numbered list, one row per proposed change:

| # | Lesson | File | Change (exact text, or the section to add) |
| --- | --- | --- | --- |

Typical targets: `knowledge/patterns/common-gaps.md`, a domain file in `knowledge/patterns/` (new or existing), a file in `templates/`, a file in `method/`, or a skill in `.claude/skills/`.

Ask: **"Which of these should I apply? (numbers, all, or none)"**. Apply only what the user chooses. For each change applied, fill the lesson's `change made to BA-OS` with the file and date. Never change anything inside `projects/` as part of this command.

## 6. Report back

In under 12 lines: the source, how many lessons were drafted (IDs and titles), which changes were applied, and the next step: review the lessons in `knowledge/lessons.md`, then approve them with `/ba-approve lesson <IDs> approved`. `/ba-start` and `/ba-check` use only `APPROVED` lessons.
