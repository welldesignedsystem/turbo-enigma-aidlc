# Team Availability Assessment

## Team Summary

One developer will own delivery with dedicated capacity and occasional reviews from others. The only confirmed available skill is Python application or API development. No external partner or contractor is planned. The product owner decides scope or priority, and engineering is consulted.

## Availability and Capacity

| Role | Availability | Capacity | Notes |
|---|---|---|---|
| Developer | One developer owns delivery | Dedicated; hours and duration not quantified | Python application/API development is confirmed. |
| Product owner | Decision-maker for scope or priority | Not specified | Engineering is consulted. |
| Engineering reviewer | Occasional review from others | No named reviewer or cadence provided | Engineering skill availability is not confirmed beyond consultation. |
| QA / testing | Not confirmed among contributors | Not specified | Identify who will provide independent review or test-design support before implementation. |
| Security / operations | Not confirmed among contributors | Not specified | Hosting and operational requirements remain undecided. |

No competing initiative or quantified utilization limit was reported. Dedicated capacity is planned, but the allocation has no stated hours, duration, or end date.

## RACI

R = Responsible, A = Accountable, C = Consulted, I = Informed. Assignments are by role because no individual names were supplied.

| Activity | Product owner | Developer | Engineering |
|---|---|---|---|
| Scope and priority decisions | A | C | C |
| Comparison behavior and acceptance criteria | A | R | C |
| Python API delivery | I | R/A | C |
| Validation and test evidence | A for acceptance | R | C; QA availability not confirmed |
| Hosting and operational decisions | A for product exposure | C | C; operational owner not confirmed |

## Capacity Allocation Agreement

- One developer is planned with dedicated capacity for this feature.
- Capacity is not expressed as hours, dates, or a percentage allocation; no schedule estimate is implied here.
- Reviews will be occasional. Reviewer identity, review points, and cadence remain to be agreed.
- No external support is planned. Revisit only if the internal skill review finds a material gap that cannot be covered internally.

## Risks and Open Decisions

- The Python/API capability is confirmed, but ownership of storage/retrieval integration and test design is not.
- Security and operations ownership cannot be assigned until the hosting and exposure boundary is known.
- Scope still requires a decision on how to handle runs with different algorithm sets; this is recorded in `scope-document.md` and should be settled before implementation.
- Time-zone and location arrangements are not applicable or remain unknown; no coordination constraint is assumed.

## Sources

- Confirmed answers in `team-formation-questions.md`.
- `scope-document.md`, `intent-backlog.md`, `feasibility-assessment.md`, and `constraint-register.md`.
- `intent-capture/stakeholder-map.md` for product-owner and engineering decision roles.