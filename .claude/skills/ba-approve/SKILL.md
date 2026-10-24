---
name: ba-approve
description: Record the BA's human decision in the active BA-OS project — review, confirm, approve or reject items, record client answers, approve the profile or a stage-file section, record a gate result, or approve or reject a lesson in knowledge/lessons.md — and log it.
argument-hint: "<IDs> <reviewed|confirmed|approved|rejected> [note]  |  gate <n> <pass|partial|fail|blocked> [reason]  |  profile  |  section <file> <heading> <reviewed|approved>  |  lesson <L-IDs> <approved|rejected> [note]"
disable-model-invocation: true
allowed-tools:
  - Read
  - Write
  - Edit
  - Glob
  - Grep
  - Bash(git status*)
  - Bash(git add *)
  - Bash(git commit *)
---

# /ba-approve — record a human decision

This is the only command that may set `REVIEWED`, `CONFIRMED`, `APPROVED` or `REJECTED`, or record a gate result. Only the user can run it. Work on the active project (`projects/active.md`).

The user typed: `$ARGUMENTS`

## 1. Understand the request

Match it to one of these forms. If it matches none, or anything is ambiguous, show the forms below with one example each and stop.

| Form | Example |
| --- | --- |
| Items | `/ba-approve REQ-014 REQ-015 reviewed` |
| Items with a note | `/ba-approve REQ-020 rejected "Client dropped online payments"` |
| A client answer | `/ba-approve Q-007 confirmed "Refunds allowed up to 48 hours before check-in"` |
| A gate | `/ba-approve gate 2 partial "Two roles still unconfirmed"` |
| The profile | `/ba-approve profile` |
| A stage-file section | `/ba-approve section 03-define "Problem statement" reviewed` |
| A section of an export | `/ba-approve section exports/rfp-response "Scope of work" reviewed` |
| Lessons | `/ba-approve lesson L-001 L-002 approved` |
| A lesson with a reason | `/ba-approve lesson L-003 rejected "Too specific to one client"` |

IDs can be separated by spaces or commas. A range such as `REQ-010..REQ-015` is allowed.

**Limit:** at most 10 items per run. If more are given, say that approving in small batches keeps reviews honest, and ask the user to split them.

## 2. Check before writing

Read `items.md` and `decisions.md`. For each item:

- It must exist and not be `SUPERSEDED`.
- `approved` on an item that is still `AI-DRAFT`: if it has open `flags`, warn that `/ba-check` found problems (list the finding IDs); if it has none, warn that it has not been checked yet. Ask the user to confirm either way.
- `approved` on an item labelled `UNKNOWN` or `CONFLICT`: warn that it is not settled and ask to confirm.
- `confirmed` requires the client's answer or confirmation text. For a Q item, the note is the answer. If no note is given, ask for it.
- `rejected` requires a reason. If no note is given, ask for it.

For a **lesson**: it must exist in `knowledge/lessons.md` and be `AI-DRAFT`. `rejected` requires a reason. Before approving, re-read the lesson for client names, people's names, prices and personal data; if any are present, say so and stop.

**Reason:** if the user gave no reason for a decision (items, a section, the profile, a gate, a lesson), ask once: *"One line on why? (press Enter to skip)"*. Use their words. Write `not stated` only if they skip.

For a **gate**: read the latest report in `checks/`. If there is no check since the last change to `items.md`, suggest running `/ba-check gate` first, and ask whether to continue anyway. `partial` needs the risks being accepted; `fail` needs the phase to go back to; `blocked` needs who or what it is waiting on. Ask for anything missing.

Then show the user one short summary of exactly what will change (item, old status → new status, note) and ask **"Record this? (yes / no)"**. Continue only on yes.

## 3. Write the changes

**Items**
- Set the new `status`.
- `confirmed` on a Q: add `answer: "<note>"` and `answered-on: <date>`. If the answer settles a label, do **not** change other items automatically; list the items that are `blocked-by` this Q so the user can decide what to update next.
- `confirmed` on another item: add the note as `confirmed-by: "<note>" (<date>)`.
- `rejected`: add `reason: <note>`.
- Add a history line: `<date> <old> → <new> by the BA via /ba-approve (DEC-<n>)`.

**Profile**: change `status: AI-DRAFT` at the top of `profile.md` to `status: APPROVED`.

**Section**: change the `status:` line under that heading in the stage file (or the file in `exports/`). Check the heading exists first.

**Lesson**: in `knowledge/lessons.md`, set the lesson's `status`, add `reason: <note>` if rejected, and add a history line `<date> AI-DRAFT → <new> by the BA via /ba-approve`. Lessons belong to BA-OS, not to one project, so no `DEC` entry is written; the history line is the record.

**Gate**: update the Gates table in `control.md` (result and date). If `fail`, set the current phase back to the phase named.

**decisions.md** — always add one entry, numbered after the highest existing number of its kind:

- Items, profile or section → a `DEC` entry under "Decision log".
- Gate → a `GATE` entry under "Gate records", with `check-report` set to the latest report file.
- Lesson → no entry (see above).

Use the formats shown in the comments in `decisions.md`. `decided-by`: the BA. Write the reason in the user's words (asked for in step 2); write `not stated` only if they chose to skip.

## 4. Save a history point

If the folder is a Git repository (run `git status`; if it fails, skip this step silently), save a snapshot:

```
git add -A
git commit -m "<project ID>: <DEC or GATE id> <one-line summary>"
```

For a lesson, use `knowledge: <L-IDs> <approved or rejected>` as the message.

Confidential projects are ignored by Git, so only the shared BA-OS files are committed; that is expected.

## 5. Report back

Two or three lines: what was recorded, the decision ID, and the next step (for gates: the next phase and its stage file). After a gate, also mention that `/ba-learn` can capture lessons so far — especially after a `PARTIAL`, `FAIL` or `BLOCKED` result, or if the project is stopping.
