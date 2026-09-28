# Phases, Stages and Gates

BA-OS runs the 15-stage BA formula grouped into **six working phases**. Each stage is a different kind of thinking; each phase ends in **one gate** that you judge.

The method never changes between projects. **The depth changes** (see `method/depth-by-size.md`).

## The six phases

| Phase | Stages inside it | Stage file | Gate question |
| --- | --- | --- | --- |
| 1. Intake | Qualify | `01-intake.md` | Is this worth analysing? Proceed, pause or ask for more information |
| 2. Discover | Understand, Research | `02-discover.md` | Is the current state known and are the unknowns listed? |
| 3. Define | Frame, Model | `03-define.md` | Are the problem, users, flows and rules agreed? |
| 4. Shape | Solve, Validate, Scope | `04-shape.md` | Is there a scope baseline with explicit in and out? |
| 5. Commit | Estimate, Commercialize, Align | `05-commit.md` | Is there a ranged estimate and a proposal you signed off? |
| 6. Deliver and learn | Deliver, Verify, Learn, Loop | `06-deliver-learn.md` | Are outcomes traced to requirements and lessons filed? |

## What each stage is for

| Stage | Reasoning function | Main outputs |
| --- | --- | --- |
| Qualify | Decide whether deeper analysis is worth it | Opportunity summary, first risks, first questions, proceed/pause decision |
| Understand | Build a current-state picture | Stakeholders, current workflows, systems, constraints; KNOWN vs UNKNOWN |
| Research | Answer specific questions that affect decisions | Findings with source, confidence and implication |
| Frame | Turn information into a problem definition | Problem statement, root causes, goals, success measures, non-goals |
| Model | Describe the system before designing it | Roles, permissions, journeys, rules, data, integrations, exceptions |
| Solve | Compare solution directions | 2–3 options with trade-offs; your choice recorded as a decision |
| Validate | Test the chosen direction | Business, user, UX, technical, integration, localization, accessibility, security, commercial checks |
| Scope | Fix what is in and out | Product → module → feature → flow → requirement; scope classification |
| Estimate | Size the work honestly | Work breakdown, ranges, confidence, assumptions, unknowns |
| Commercialize | Turn scope into an engagement | Phases, deliverables, team, payment structure, change rules |
| Align | Create shared understanding | Handoff pack, walkthrough notes, sign-offs |
| Deliver | Guard requirements during build | Change classification and impact analysis |
| Verify | Prove the build meets the need | Trace from goal to outcome; UAT results |
| Learn | Capture what happened | Lessons, wrong assumptions, estimate accuracy |
| Loop | Improve BA-OS itself | Updated templates, checklists and skills |

## Gate criteria

A gate passes because the **quality of information and reasoning is enough**, not because a file exists.
Gate results: `PASS`, `PARTIAL` (proceed with named risks), `FAIL` (go back), `BLOCKED` (waiting on someone else).

### Gate 1 — Intake
- The business reason for the project is stated in the client's words (a `KNOWN` GOAL or PRB).
- The requested solution is recorded separately from the underlying need.
- First risks, assumptions and questions exist as items.
- Size and depth in `profile.md` are reviewed by you.
- Decision recorded: proceed, pause or request information.

### Gate 2 — Discover
- Every input in `inputs/` has been extracted.
- Stakeholders and current workflows are described (at the profile's depth).
- No `CONFLICT` item is left without a matching `Q` item.
- Questions that block Define are marked `priority: MVP` or answered.
- Research findings, if any, carry sources and confidence.

### Gate 3 — Define
- Problem statement and at least one GOAL with a success measure are `REVIEWED`.
- Every NEED has a parent PRB or GOAL.
- User roles and permissions are listed; no role is described only as "users" or "staff".
- Key journeys include at least one exception or failure path each.
- Business rules are separate RULE items, not hidden inside requirement text.

### Gate 4 — Shape
- The chosen solution direction is a recorded decision with alternatives considered.
- The validation checklist in `04-shape.md` is completed at the profile's depth.
- Every FEAT has a parent REQ and a `scope` value.
- Every MVP REQ has acceptance criteria.
- `OUT` scope is written explicitly, not implied.
- No MVP item is still `UNKNOWN` or `CONFLICT`.

### Gate 5 — Commit
- Every MVP FEAT appears in the work breakdown.
- Every estimate line has a range, a confidence level and its assumptions; you entered or accepted every number.
- Dependencies and client responsibilities are listed in the proposal.
- The baseline items are `APPROVED`.

### Gate 6 — Deliver and learn
- Every change after baseline has a `CHG` entry with impact and decision.
- Every MVP REQ is traced to a test or UAT result.
- Lessons are written to `knowledge/lessons.md`.

## Going back

A `FAIL` sends work back to the phase that caused the problem. Common loop-backs:

- Estimating reveals a missing requirement → back to Define or Shape.
- Validation shows the chosen option does not solve the problem → back to Shape (Solve).
- A client answer contradicts an approved item → create a `CHG` and go back to the phase that owns the item.

Every loop-back is recorded in `decisions.md` as a `GATE` entry with result `FAIL` and the phase you return to.

## Next-action rules (used by `/ba-status`)

Suggest the first rule that applies:

0. `profile.md` is still `status: AI-DRAFT` → review it and run `/ba-approve profile`.
1. A file in `inputs/` has not been extracted → run `/ba-extract`.
2. There are `AI-DRAFT` items with no check since they were created → run `/ba-check`.
3. There are open findings from the last check → resolve the top findings (list them).
4. There are unanswered `Q` items that block the current phase → send them to the client (list them).
5. There are `AI-CHECKED` items → review them and run `/ba-approve`.
6. The current phase's stage file has empty required sections → work on them (name them).
7. Everything above is clear → run `/ba-check` for a gate readiness check, then record the gate with `/ba-approve gate <n> <result>`.
