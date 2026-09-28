---
name: ba-extract
description: Extract facts, goals, problems, needs, requirements, rules, assumptions, questions, risks, dependencies and contradictions from the client files in the active project's inputs folder, and add them to items.md as AI-DRAFT items with sources and quotes.
argument-hint: "[file-name | all]"
disable-model-invocation: true
allowed-tools: Read Write Edit Glob Grep
---

# /ba-extract — turn client inputs into items

Work on the active project (`projects/active.md`). If it is not set, ask which project to use.

## 1. Pick the inputs

- If `$ARGUMENTS` names a file, extract only that file from `inputs/`.
- If `$ARGUMENTS` is `all`, re-read every input (useful after big changes), but never duplicate items that already exist.
- Otherwise, extract every file in `inputs/` whose "Extracted on" is empty in the **Input log** of `control.md`. Add any file in `inputs/` that is missing from the log first.
- If nothing is new, say so and stop.
- If a file cannot be read (for example a `.docx`), tell the user to save it as PDF or paste the text, and skip it.

## 2. Load the context

Read, in this order: `profile.md`, `method/labels-and-statuses.md`, `method/requirement-standard.md`, and the existing `items.md` (so you can link to and avoid duplicating existing items).

## 3. Extract

Read each input carefully, section by section. For every relevant statement, decide:

| If the input… | Create |
| --- | --- |
| States why the project exists or what success looks like | GOAL |
| Describes something broken, slow, costly or painful | PRB |
| Says someone needs to be able to do or know something | NEED |
| Says the product must do or be something | REQ |
| States a condition, limit, price, approval or permission rule | RULE |
| Names a feature, screen or module | FEAT (with `scope` left as `unknown` unless the input says) |
| Implies something without stating it | ASM |
| Leaves something important unclear | Q (and an UNKNOWN item if the gap matters for scope) |
| Mentions a threat to success | RISK |
| Depends on a person, system or decision outside the team | DEP |
| Contradicts another input or an existing item | CONFLICT-labelled item + a Q to resolve it |

Rules while extracting:

1. **Quote, don't paraphrase, for KNOWN items.** Every `KNOWN` item carries a short verbatim `quote` copied exactly from the input, and a `source` with the file name and page, heading or line.
2. If you are inferring, the label is `ASSUMPTION` and `why` says what you inferred it from.
3. **Solution-first requests** ("we need an app") become a NEED or REQ labelled `ASSUMPTION` plus a Q asking what problem the solution should solve.
4. Vague roles ("users", "staff", "admin") become a Q asking which real roles and permissions exist.
5. Vague words (fast, easy, modern, flexible) become a Q asking for a measurable target.
6. Set `parent` to the most likely existing item. If there is none yet, use `none` and say so in `why`.
7. Draft `acceptance` for REQ items only when the input gives enough to test; otherwise add a Q.
8. Do not create a separate item for every sentence. Merge statements that say the same thing, listing all sources.
9. Never invent numbers, names, dates or features that are not in the inputs.

## 4. Number and write

- Find the highest existing number for each prefix in `items.md` and continue from there.
- Add each item at the end of its group in `items.md`, in the format from `method/labels-and-statuses.md`.
- Every new item: `status: AI-DRAFT`, `flags: none`, and a history line `<date> created by /ba-extract from <file>`.
- Update the **Input log** in `control.md`: set "Extracted on" to today for each file processed.

## 5. Report back

In under 15 lines:

- Files processed.
- Count of new items by type, and by label.
- The three most important open questions (IDs and one line each).
- Any CONFLICT items found.
- Next step: review the new items in `items.md` (Cursor's Source Control panel shows exactly what was added), then run `/ba-check`.
