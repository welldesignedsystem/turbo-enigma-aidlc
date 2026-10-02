# Ideation Decision Log

## Confirmed Product Decisions

| Decision | Outcome | Source |
|---|---|---|
| Intended user and purpose | Internal users and developers compare algorithm runs for teaching and learning. | `intent-capture/intent-statement.md` |
| Run selection | Compare two existing runs by run ID; use the documented retrieval/store boundary. | `feasibility/feasibility-questions.md` |
| Comparison contents | Show both outputs and available metrics, with an output-match indicator; do not rank or recommend. | `scope-definition/scope-definition-questions.md` |
| Different input digests | Permit comparison without a special input-difference warning. | `scope-definition/scope-definition-questions.md` |
| Different step-counting versions | Reject the comparison. | `scope-definition/scope-definition-questions.md` |
| Language | Python. Framework and hosting remain undecided. | `feasibility/feasibility-questions.md` |
| UI scope | API-only; Rough Mockups was skipped because there is no user-facing UI. | `scope-document.md`; stage applicability decision |
| Team | One developer, dedicated capacity, occasional reviews; no external partner. | `team-formation/team-formation-questions.md` |
| Delivery ordering | Resolve comparison rules for unlike runs before implementation. | `scope-definition/scope-definition-questions.md` |
| Handoff posture | Proceed to Inception with algorithm-set behavior and storage/testing ownership tracked for resolution before implementation. | `approval-handoff/approval-handoff-questions.md` |

## Open Decisions and Conditions

| Item | Status | Required before |
|---|---|---|
| Behavior for differing algorithm sets | Open; product/engineering decision required. | Implementation and final comparison contract |
| Storage/retrieval integration owner | Not confirmed; identify owner and verify draft contract against implementation. | Implementation |
| Test-design / QA coverage | Not confirmed; assign developer or reviewer responsibility. | Implementation completion criteria |
| Hosting and exposure boundary | Undecided; public exposure would change required security controls. | Deployment design |
| Python run-service performance against inherited targets | Unmeasured; benchmark with real implementation. | Finalizing limits and performance claims |
| Retention, request volume, and capacity | Unspecified. | Store sizing and operating-cost estimates |

## Explicitly Not Established

- Market validation: Market Research was skipped; no competitive-analysis, trend, or build-vs-buy evidence is available.
- UI design: Rough Mockups was skipped because the approved initiative is API-only.
- Delivery date, budget, named reviewers, and quantified capacity: none were supplied.
- Draft API and NFR documents in the sibling knowledge base are not independently validated or implemented evidence.