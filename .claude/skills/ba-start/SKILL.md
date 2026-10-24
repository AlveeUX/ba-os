---
name: ba-start
description: Start a new BA-OS project. Creates the project folder from templates, saves the client input, and drafts a project profile with size and depth per phase for the user to review.
argument-hint: "<short-project-name>"
disable-model-invocation: true
allowed-tools: Read Write Edit Glob Grep
---

# /ba-start — start a new project

Start a new BA-OS project named **$ARGUMENTS**. Follow these steps in order. Read `CLAUDE.md` rules first if they are not already loaded.

## 1. Collect what you need

If `$ARGUMENTS` is empty, ask for a short project name (a few words, for example "hotel booking").

Then ask the user these questions in one message and wait for the answers:

1. **Client name** (or "unknown").
2. **Privacy level**: `public`, `internal` or `confidential`. Explain in one line: confidential projects are kept out of any online backup.
3. **Client input**: have they already copied the client's files into a folder, or will they paste the brief as text now? Tell them which formats work best: `.md`, `.txt` and `.pdf` are read directly; a Word file should be saved as PDF first.
4. **Input type and expected deliverable**: what kind of input is this (rough idea, existing website or app, Figma file, specification, or an RFP / RFQ / tender), and what does the client expect to get back from us (proposal, RFP response, estimate only…)? If it is an RFP, confirm in one line whether we are **responding** to it or **writing** it for the client — these are different documents.

## 2. Create the project folder

1. Make the short name lowercase with hyphens (for example `hotel-booking`).
2. Find the next project number: look at folder names in `projects/` and `projects/_confidential/` that start with `P-<current year>-`, take the highest number and add one. Start at `001`.
3. Project ID: `P-<year>-<number>-<short-name>`, for example `P-2026-001-hotel-booking`.
4. Folder: `projects/<ID>/`, or `projects/_confidential/<ID>/` if privacy is `confidential`.
5. Copy these templates into the folder, replacing `{{PROJECT_ID}}`, `{{PROJECT_NAME}}` and `{{DATE}}` (today, YYYY-MM-DD):
   - `templates/control.md` → `control.md`
   - `templates/profile.md` → `profile.md`
   - `templates/items.md` → `items.md`
   - `templates/decisions.md` → `decisions.md`
6. Create empty folders by writing a `README.md` in each: `inputs/` ("Client files exactly as received. Never edit these."), `research/`, `checks/`, `exports/`.
7. Stage files are created in step 5, after depth is known.

## 3. Save the client input

- If the user pastes text, save it unchanged as `inputs/brief-<YYYY-MM-DD>.md`, with one header line: `Pasted by the BA on <date>. Original text below, unchanged.`
- If the user says files are already somewhere else, ask them to copy the files into the new `inputs/` folder (give the full path) and tell you when done. Do not continue until at least one input exists.
- Add each input file to the **Input log** table in `control.md` with today's date as "Received" and "Extracted on" left empty.

## 4. Draft the profile

Read every file in `inputs/`, then `method/depth-by-size.md`, `knowledge/lessons.md` and the file names in `knowledge/patterns/`.

Fill `profile.md`:

- Basics you can support from the inputs. Leave a field empty rather than guess. Set `privacy`.
- **Input type** and **Deliverable expected**: from the user's answer to question 4. If the input is an RFP, RFQ or tender and we are responding to it, add this line to **Extra checks**: "RFP response: every RFP requirement and evaluation criterion goes in the compliance table in `templates/exports/rfp-response.md`."
- **Size**: suggest one size and list the signals from `method/depth-by-size.md` that drive it, each with the input it came from. If information is too thin to size, write `size: unknown` and say what is missing.
- **Depth per phase**: use the suggested depth for that size. For a simple project this is lite mode.
- **Domain notes**: always list `knowledge/patterns/common-gaps.md`; add any domain pattern file whose name matches the project type or the industry (for example `hospitality.md` for a hotel booking site); add up to three relevant lessons from `knowledge/lessons.md` by ID.
- **Extra checks**: areas the inputs show need attention (payments, personal data, multi-location, multi-language…).
- Keep `status: AI-DRAFT` at the top.

Do not create items yet. Items come from `/ba-extract`.

## 5. Create the stage files

For each phase whose depth is not `skip`, copy its template from `templates/stages/` into the project folder (same file name), replacing the placeholders. Fill the **Depth** column of the Gates table in `control.md`.

If **Deliverable expected** is a proposal or an RFP response, also copy `templates/exports/rfp-response.md` to `exports/rfp-response.md`, replacing the placeholders. If we are not responding to an RFP, delete the "RFP compliance table" section from the copy.

## 6. Make it the active project

Write the project folder path (for example `projects/P-2026-001-hotel-booking`) as the only line of `projects/active.md`.

## 7. Report back

Tell the user, in plain language and in under 15 lines:

- The project ID and folder.
- The suggested size, the two or three signals behind it, and the depth per phase.
- Which stage files were created.
- That the profile is a draft: they should open `profile.md`, correct anything, then run `/ba-approve profile`.
- Next step: run `/ba-extract` to pull items out of the inputs.
