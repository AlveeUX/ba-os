# Requirement Standard

A requirement (REQ) says what the product must do or be, for whom, and why. It must be **clear, testable, traceable and supported by a source or an explicit assumption.**

## Lite fields (every REQ)

These go in the item's field list in `items.md`.

| Field | What to write |
| --- | --- |
| Title (heading) | One line in plain language: who can do what. "Guests can cancel a booking online." |
| `parent` | The NEED (or GOAL in lite mode) it serves |
| `source` / `quote` | Where it came from (see `method/labels-and-statuses.md`) |
| `why` | The business reason, if not obvious from the parent |
| `priority` | `MVP`, `SHOULD`, `COULD`, `WONT` |
| `acceptance` | At least one Given / When / Then line |

## Full fields (standard and deep depth, MVP requirements)

Add these under the lite fields when the phase depth is `standard` or `deep`:

| Field | What to write |
| --- | --- |
| `user` | The role (from the roles list in `03-define.md`) |
| `trigger` | What starts it |
| `preconditions` | What must be true first |
| `main-flow` | Numbered steps |
| `alternative-flows` | Other valid paths |
| `exceptions` | Failures, invalid data, timeouts, permission denied, partial completion |
| `rules` | RULE IDs |
| `permissions` | Which roles can and cannot do this |
| `dependencies` | DEP IDs or other REQ IDs |

## Quality checklist

A requirement fails the check if any answer is "no":

1. Does it describe **one** thing? ("and" in the title is a warning sign.)
2. Is it free of design decisions that belong to UX (for example "a blue button")?
3. Could a tester decide pass or fail from the acceptance criteria alone?
4. Does it avoid vague words: *fast, easy, user-friendly, modern, flexible, etc., and so on, some, appropriate*?
5. Does it have a parent, so we know why it exists?
6. Are business rules separate RULE items, not buried in the text?
7. Are the exceptions covered (at standard and deep depth)?
8. Is the source real, and does the quote say what the item claims?

## Writing acceptance criteria

Use Given / When / Then:

- **Given** the starting situation
- **When** the user or system does something
- **Then** the observable result

Write at least one success case and, at standard depth or deeper, at least one failure case.

## Solution-first requests

When a client asks for a solution ("we need a mobile app"), record it as a `NEED` or `REQ` with label `ASSUMPTION` and create a `Q` item asking what problem it solves. Do not scope the solution until the underlying need is known.
