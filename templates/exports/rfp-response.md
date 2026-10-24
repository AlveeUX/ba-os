# Proposal / RFP Response — {{PROJECT_ID}}

The client-facing document we send back. Use it when `profile.md` says the deliverable is a **proposal** or an **RFP response**. It is assembled from the project's items and stage files, so every claim can be traced to an item ID.

Rules:

- Write for the client, in plain language. Item IDs go in the right-hand "Built from" notes or in comments, not in the client's reading flow, unless the client asked for traceability.
- Nothing here may say more than the items support. An `ASSUMPTION` is written as an assumption, an `UNKNOWN` as an open question.
- Prices and durations are ranges (CLAUDE.md rule 7), taken from `05-commit.md` after you entered or accepted them.
- Each section carries its own status line: `empty` → `AI-DRAFT` → `REVIEWED` → `APPROVED` (only `/ba-approve section exports/rfp-response …` sets the last two).
- The **RFP compliance table** at the end is required when the input is an RFP, RFQ or tender we are responding to. Leave it out otherwise.

## 1. Executive summary
status: empty

Built from: GOAL and PRB items, the chosen direction in `04-shape.md`, the estimate summary in `05-commit.md`.

Half a page: the client's problem in one line, what we propose, why we are a good fit, and the one open item that most affects the proposal.

## 2. Understanding of the problem
status: empty

Built from: `03-define.md` (Problem statement, Root causes, Goals and success measures).

The problem in our own words, showing we read and understood it: who has it, what it costs, the root cause, and what success looks like. Separate what the client told us from what we infer.

## 3. Proposed solution and approach
status: empty

Built from: `04-shape.md` (Solution options, Chosen direction — including build, buy or configure), the DEC that records the choice.

What we will build or configure, why this direction over the alternatives, and the principles of our approach.

## 4. Scope of work
status: empty

Built from: `04-shape.md` (Scope breakdown, Scope baseline, Screen inventory), `03-define.md` (User roles and permissions, Key journeys).

- Modules and features in scope (MVP and later phases).
- User roles and key user flows.
- Platforms and languages (for example web, mobile, Arabic right-to-left).
- **Out of scope, written explicitly** (every `OUT` FEAT).

## 5. Process and phases
status: empty

Built from: `05-commit.md` (Engagement structure).

For example: discovery → UX → UI → development → testing → launch → support. For each phase: what happens, what the client receives, and what the client must approve.

## 6. Timeline
status: empty

Built from: `05-commit.md` (Engagement structure, Cost range by phase).

Each phase with a duration range and its dependencies. State what the timeline assumes (for example client review times).

## 7. Team
status: empty

Built from: `05-commit.md` (Rate card, Engagement structure).

Roles (not names unless confirmed), what each is responsible for, and in which phases they are active. State any role that is not included.

## 8. Estimation and pricing
status: empty

Built from: `05-commit.md` (Work breakdown and estimate, Estimate summary, Rate card, Cost range by phase, Payment milestones).

| Phase | Effort (days, low–high) | Cost (low–high) |
| --- | --- | --- |
| | | |
| **Total** | | |

Payment milestones, what the price includes and excludes, and the assumptions that would change the number most.

## 9. Assumptions, risks and dependencies
status: empty

Built from: ASM, RISK and DEP items; open Q items that affect scope or price.

| Type | Item | If wrong or late, what changes | Owner |
| --- | --- | --- | --- |
| Assumption | | | |
| Risk | | | |
| Dependency | | | |

## 10. Next steps
status: empty

What we need from the client to move forward (clarification call, open answers, sign-off, contract), in order.

## RFP compliance table (RFP responses only)
status: empty

One row for every requirement and evaluation criterion in the client's RFP, in the RFP's own order and words, so the client can check that nothing was missed.

| RFP ref | Requirement or criterion as written | Our response (meets / partly / does not meet / alternative) | Where answered (section) | Item IDs |
| --- | --- | --- | --- | --- |
| | | | | |
