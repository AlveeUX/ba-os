# Depth by Project Size

The method is the same for every project. What changes is **how deep each phase goes**.
`/ba-start` suggests a size and a depth per phase; you accept or change them in `profile.md`.

## Sizing signals

Look at these signals together. Do not add them up into a score; describe which ones drive the size.

| Signal | Simple | Moderate | Complex | Enterprise |
| --- | --- | --- | --- | --- |
| User roles | 1–2 | 3–4 | 5–8 | 9+ or per-tenant roles |
| Modules | 1–3 | 4–6 | 7–12 | 13+ |
| Integrations | 0–1 | 2–3 | 4–6 | 7+ or legacy systems |
| Business rules | Few, obvious | Some pricing or approval logic | Many interacting rules | Regulated or per-region rules |
| Data | Simple content | Some records and states | Many related entities | Multiple systems of record |
| Stakeholders | 1 decision maker | 2–3 | Several teams | Several organizations |
| Locations / markets | 1 | 1–2 | Several | Multi-country |
| Security / regulation | Low | Personal data | Payments or sensitive data | Compliance obligations |
| Technical uncertainty | Known tech | Some unknowns | New integrations | Unknown legacy or scale |

## Depth levels

| Depth | Meaning |
| --- | --- |
| `skip` | Phase not run; its stage file is not created |
| `light` | Only the sections marked **[light]** in the stage file |
| `standard` | Sections marked **[light]** and **[standard]** |
| `deep` | Every section, including **[deep]** |

## Suggested depth per size

| Phase | Simple (lite mode) | Moderate | Complex | Enterprise |
| --- | --- | --- | --- | --- |
| 1. Intake | light | light | standard | deep |
| 2. Discover | light | standard | standard | deep |
| 3. Define | skip | light | standard | deep |
| 4. Shape | light | standard | deep | deep |
| 5. Commit | light | standard | standard | deep |
| 6. Deliver and learn | light | light | standard | deep |

## Lite mode (simple projects)

Lite mode is for small, well-understood work such as a brochure website or a landing page.

- Stage files created: `01-intake.md`, `02-discover.md`, `04-shape.md`, `05-commit.md`, `06-deliver-learn.md`.
- Item types used: GOAL, REQ, FEAT, ASM, Q, RISK. (PRB, NEED, RULE and DEP only if they clearly appear.)
- REQ items use the **lite** fields in `method/requirement-standard.md`.
- In lite mode a REQ may have a GOAL as its parent.
- Gates still apply, but only their criteria for sections that exist.

If a lite project turns out bigger than expected, change the size in `profile.md`, record a decision, and ask Claude to create the missing stage files.

## Changing depth later

Depth is a decision, not a setting. Any change to size or depth is recorded in `decisions.md` with a reason.
