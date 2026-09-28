# Items, Labels and Statuses

Every tracked thing in a project is an **item** in `items.md`. Each item has an ID, a type, a label, a status, a source and (usually) a parent. Traceability, registers and quality checks all come from these fields.

## Item types

| Prefix | Type | Parent is usually | Notes |
| --- | --- | --- | --- |
| GOAL | Business goal or outcome | none | Include a success measure when known |
| PRB | Problem or root cause | GOAL | Separate the symptom from the cause |
| NEED | User or business need | PRB | Who needs what, and why |
| REQ | Requirement | NEED | Follows `method/requirement-standard.md` |
| RULE | Business rule | REQ | Eligibility, pricing, approval, permission, cancellation… |
| FEAT | Feature or scope unit | REQ | Carries a `scope` field |
| ASM | Assumption | the item it supports | Carries `risk-if-wrong` and `validate-by` |
| Q | Open question | the item it blocks | Carries `ask` (who to ask) and, once answered, `answer` |
| RISK | Risk | the item it threatens | Carries `probability`, `impact`, `mitigation` |
| DEP | Dependency | the item that waits on it | Carries `owner` and `needed-by` |

IDs are numbered per project with three digits: `REQ-001`, `REQ-002` … Never reuse a number, even for rejected items.

Decisions (`DEC`), changes (`CHG`) and gate records (`GATE`) are events, not things. They live in `decisions.md`.

## Labels — how sure are we?

| Label | Meaning | Rule |
| --- | --- | --- |
| `KNOWN` | Stated in a source | Must have `source` and a verbatim `quote` |
| `ASSUMPTION` | Believed but not confirmed | Must say why it is believed |
| `UNKNOWN` | A gap we know about | Usually paired with a `Q` item |
| `CONFLICT` | Two sources disagree | Must cite both sources in `sources` |

"Evidence" from the original BA-OS brief is not a separate label: it is the `source` and `quote` fields on every item.

## Statuses — who has checked it?

```
AI-DRAFT → AI-CHECKED → REVIEWED → CONFIRMED → APPROVED
                                  (plus REJECTED and SUPERSEDED at any point)
```

| Status | Set by | Meaning |
| --- | --- | --- |
| `AI-DRAFT` | AI or you | Proposed, nobody has checked it |
| `AI-CHECKED` | `/ba-check` only | The critic checklist found no problem |
| `REVIEWED` | You, via `/ba-approve` | You read it and accept the wording |
| `CONFIRMED` | You, via `/ba-approve`, recording the client's answer | The client or stakeholder agreed |
| `APPROVED` | You, via `/ba-approve` | Part of the baseline; changes now need a `CHG` |
| `REJECTED` | You, via `/ba-approve` | Not accepted; keep it for the record with a reason |
| `SUPERSEDED` | You or AI | Replaced by a newer item (`superseded-by`) |

`CONFIRMED` is optional: items that do not need client confirmation can go from `REVIEWED` to `APPROVED`.

Mapping to the original brief's words: "AI generated" = `AI-DRAFT`; "AI checked" = `AI-CHECKED`; "Evidence verified" = you checking the `source` and `quote` while reviewing; "BA reviewed" = `REVIEWED`; "Client / stakeholder confirmed" = `CONFIRMED`.

### Stage-file sections

Each section of a stage file (`01-intake.md` … `06-deliver-learn.md`) has a `status:` line under its heading:
`empty` → `AI-DRAFT` → `REVIEWED` → `APPROVED`. AI may set `AI-DRAFT` when it writes a section; only `/ba-approve section …` sets `REVIEWED` or `APPROVED`. The profile follows the same rule (`/ba-approve profile`).

## Item format in `items.md`

Each item is a level-3 heading followed by a short field list. Leave out optional fields that do not apply.

```markdown
### REQ-014 · Guests can cancel a booking online
- type: REQ
- label: ASSUMPTION
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-brief.pdf p.2
- quote: "customers should be able to manage their bookings themselves"
- why: The brief asks for self-service booking management; cancellation is assumed to be part of it.
- blocked-by: Q-007
- priority: MVP
- rules: RULE-005
- acceptance:
  - Given a paid booking more than 48 hours away, when the guest cancels, then the booking shows Cancelled and a refund request is created.
- flags: none
- history:
  - 2026-09-28 created by /ba-extract
```

### Field reference

| Field | Required | Values / format |
| --- | --- | --- |
| `type` | Yes | One of the prefixes above |
| `label` | Yes | `KNOWN`, `ASSUMPTION`, `UNKNOWN`, `CONFLICT` |
| `status` | Yes | One of the statuses above |
| `parent` | Yes except GOAL | One item ID, or `none` with a reason in `why` |
| `source` | Yes | `inputs/<file> <page or section>`, `research/<file> F-00x`, `meeting <date> (inputs/<file>)`, `client answer <date>`, or `BA reasoning` (only with label `ASSUMPTION`) |
| `sources` | CONFLICT only | Two or more sources, each with its own quote |
| `quote` | KNOWN only | Short verbatim text from the source, in double quotes |
| `why` | ASSUMPTION, UNKNOWN | One sentence of reasoning |
| `priority` | REQ, FEAT | `MVP`, `SHOULD`, `COULD`, `WONT` |
| `scope` | FEAT | `MVP`, `IN`, `OUT`, `PHASE-2`, `OPTIONAL`, `FUTURE` |
| `acceptance` | REQ | One or more Given / When / Then lines |
| `rules` | Optional | RULE IDs |
| `blocked-by` | Optional | Q or DEP IDs |
| `risk-if-wrong`, `validate-by` | ASM | One line each |
| `ask`, `answer`, `answered-on` | Q | Who to ask; the answer in the client's words; the date |
| `probability`, `impact` | RISK | `low`, `medium`, `high` |
| `mitigation` | RISK | One line |
| `owner`, `needed-by` | DEP | Name or role; date or phase |
| `superseded-by` | SUPERSEDED | Item ID |
| `reason` | REJECTED | One line |
| `flags` | Set by `/ba-check` | Finding IDs from the latest check, or `none` |
| `history` | Yes | One dated line per change: what changed and which command or person did it |

## Research finding format in `research/<topic>.md`

```markdown
### F-001 · Most regional hotel sites offer free cancellation up to 24 hours
- question: What cancellation policies are standard for the client's market?
- finding: (one or two sentences)
- kind: verified fact | source-supported finding | interpretation | hypothesis | unknown
- source: https://… (title of the page)
- read-on: 2026-09-28
- confidence: high | medium | low
- business-implication: (one line)
- product-implication: (one line)
```

Never write a finding without a source URL you actually opened. If nothing reliable was found, write a finding with `kind: unknown`.
