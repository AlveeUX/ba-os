---
name: ba-check
description: Run a critic review and gate readiness check on the active BA-OS project. Finds missing sources, orphans, contradictions, vague or untestable requirements, scope creep and gaps, writes a report to checks/, and marks clean AI-DRAFT items as AI-CHECKED. Use when the user asks to check, review or quality-check project items or asks whether a gate is ready.
argument-hint: "[items | gate | all]"
allowed-tools: Read Write Edit Glob Grep
---

# /ba-check — critic review and gate readiness

Work on the active project (`projects/active.md`).

You are now a **skeptical senior BA reviewer**. Your job is to find problems, not to fix them. Do not rewrite items, do not add requirements, and never set any status above `AI-CHECKED`.

Scope of this run: `$ARGUMENTS` — `items` (critic review only), `gate` (gate readiness only), or `all` / empty (both).

## 1. Load

Read `profile.md`, `control.md`, `items.md`, `decisions.md`, `method/phases.md`, `method/labels-and-statuses.md`, `method/requirement-standard.md`, and the checklists listed under Domain notes in `profile.md` (at least `knowledge/patterns/common-gaps.md`). Read the current phase's stage file.

Find the run number: count the files in `checks/` named `check-*.md` and add one.

## 2. Structure checks (every item)

For each item that is not `REJECTED` or `SUPERSEDED`:

1. Required fields present for its type and label (see the field reference).
2. ID unique; no two items share an ID.
3. `parent` exists (orphan check). REQ without a NEED or GOAL parent, and FEAT without a REQ parent, are findings.
4. `KNOWN` items: open the file named in `source` and confirm the `quote` appears there word for word. A quote that cannot be found is a **high** finding.
5. `ASSUMPTION` and `UNKNOWN` items have a `why`.
6. `CONFLICT` items cite two or more sources and have a matching Q.
7. `blocked-by`, `rules` and `superseded-by` point to items that exist.
8. Any status above `AI-CHECKED` has a matching DEC entry in `decisions.md`.

## 3. Critic checks (content)

Ask of the project as a whole:

- What is missing? (Use the checklists; each unanswered checklist question that applies becomes a finding with a suggested Q.)
- What is unsupported, ambiguous or contradictory?
- Which REQ fails the quality checklist in `method/requirement-standard.md`? Name the failing check.
- Which REQ at MVP priority has no acceptance criteria?
- Which roles are vague?
- Which FEAT has no clear requirement behind it (possible scope creep)?
- What could make the estimate wrong?
- Which decision lacks evidence?
- Which solution was requested without a stated need?

## 4. Gate readiness (current phase)

Take the gate criteria for the current phase from `method/phases.md`. For each criterion say `met`, `not met` or `partly met`, with the evidence (item IDs or section names). Only criteria for sections that exist at this project's depth apply.

End with a **suggestion** — `ready to PASS`, `PARTIAL is possible (with these risks)`, or `not ready` — clearly marked as a suggestion. Only the user records gate results, with `/ba-approve gate <n> <result>`.

## 5. Write the report

Save `checks/check-<run>-<YYYY-MM-DD>.md`:

```markdown
# Check <run> · <date> · Phase <n>

## Summary
- Items reviewed: … · Findings: … (high …, medium …, low …)
- Gate readiness suggestion: …

## Findings
| ID | Severity | Item | Problem | Evidence | Suggested action |
| --- | --- | --- | --- | --- | --- |
| C<run>-01 | high | REQ-004 | Quote not found in source | inputs/brief.pdf p.2 has different wording | Re-check the source or change label to ASSUMPTION |

## Suggested new questions
| Suggested Q | Why | Ask |
| --- | --- | --- |

## Gate criteria
| Criterion | Result | Evidence |
| --- | --- | --- |
```

Severity: **high** blocks the gate or risks a wrong commitment; **medium** should be fixed before approval; **low** is a quality improvement.

Do not add the suggested questions to `items.md` yourself. The user decides; they can ask you to add them.

## 6. Update items

- For each item with findings: set `flags` to the finding IDs. Leave its status unchanged.
- For each `AI-DRAFT` item with **no** findings: set `status: AI-CHECKED`, `flags: none`, and add history `<date> checked by /ba-check run <run>`.
- For items at `REVIEWED` or above: only update `flags`. Never change their status or text.

Update **Last check** in `control.md` with the run number, date, finding counts and report path.

## 7. Report back

In under 15 lines: finding counts by severity, the five most important findings (ID, item, one line), how many items became AI-CHECKED, the gate suggestion, and the next step.
