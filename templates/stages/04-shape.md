# 4. Shape — {{PROJECT_ID}}

Stages inside this phase: **Solve** (compare directions), **Validate** (test the chosen direction) and **Scope** (fix what is in and out).
Gate question: *Is there a scope baseline with explicit in and out?* (criteria: `method/phases.md`)

AI can propose options. You decide, and the choice is recorded as a DEC.

Section markers: **[light]** always done · **[standard]** at standard depth or deeper · **[deep]** at deep depth only.

## Solution options [standard]
status: empty

| Criterion | Option A | Option B | Option C |
| --- | --- | --- | --- |
| Summary | | | |
| Business value | | | |
| User value / UX quality | | | |
| Technical feasibility | | | |
| Complexity and cost | | | |
| Timeline | | | |
| Scalability and maintenance | | | |
| Risk and dependencies | | | |
| Operational impact | | | |

## Chosen direction [light]
status: empty

The option chosen and the DEC ID that records it.

## Validation checklist [light]
status: empty

At light depth complete the first four rows. At standard, all rows except the last two. At deep, all rows.

| Check | Question | Result | Items raised |
| --- | --- | --- | --- |
| Business | Does it solve the business problem? | | |
| User | Does it solve the user problem? | | |
| Technical | Is it feasible? | | |
| Commercial | Is it commercially realistic? | | |
| UX | Is the flow understandable? | | |
| Integration | Are dependencies realistic? | | |
| Security | Authentication, authorization, sensitive data, abuse cases | | |
| Localization | Currency, language, region, RTL/LTR, dates, addresses | | |
| Accessibility | Accessibility requirements and interaction limits | | |

## Scope breakdown [light]
status: empty

Product → module → feature → flow → requirement. Use FEAT and REQ IDs.

```
Product
├── Module
│   ├── FEAT-… (scope)
│   │   └── REQ-…
```

## Scope baseline [light]
status: empty

| Scope | FEAT IDs |
| --- | --- |
| MVP | |
| IN (after MVP, same engagement) | |
| PHASE-2 | |
| OPTIONAL | |
| FUTURE | |
| OUT (explicitly excluded) | |

Dependencies, assumptions and risks the baseline relies on (IDs):
