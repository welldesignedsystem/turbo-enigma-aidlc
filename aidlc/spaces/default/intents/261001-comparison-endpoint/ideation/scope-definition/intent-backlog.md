# Intent Backlog

## Prioritization Approach

MoSCoW prioritization is used because user reach, cost, and delivery capacity have not been quantified. The backlog stays at capability level; implementation breakdown follows after the comparison contract is closed.

## Backlog

| ID | Capability | Priority | Value | Dependency / sequencing |
|---|---|---|---|---|
| PB-1 | Finalize behavior when the two runs contain different algorithm sets. | Must | Prevent incomplete or ambiguous comparisons. | First; this compatibility case remains unresolved. The input-digest and step-counting-version decisions are already confirmed. |
| PB-2 | Compare two retrievable stored runs and present both outputs, all available metrics, and whether the outputs match. | Must | Delivers the requested teaching and learning comparison. | Depends on PB-1 and the run retrieval boundary. |
| PB-3 | Add element-level output-difference detail. | Could | Makes individual differences easier to inspect. | Deferred; the first useful response returns both arrays and an output-match indicator. |

## Dependency Flow

```text
PB-1 Comparison compatibility rules
  -> Confirm run retrieval boundary
  -> PB-2 Two-run comparison response
  -> PB-3 Element-level output detail (optional later)
```

## Scope Guardrails

- Compare exactly two existing run IDs; creating runs is separate.
- Different input digests are allowed without a special warning.
- Different `step_counting_version` values are rejected.
- Do not rank algorithms or recommend a winner.

## Assumptions and Open Questions

- The existing run retrieval contract can be implemented and returns immutable stored run records.
- Behavior for algorithm-set differences must be decided before PB-2 implementation.
- No user-provided deadline or delivery-capacity constraint is currently known.

## Sources

- `scope-document.md` and confirmed answers in `scope-definition-questions.md`.
- `feasibility-assessment.md` and `constraint-register.md`.
- `turbo-enigma-knowledge-base/api/run-retrieval-endpoint.md` and `architecture/data-model.md` (draft contracts).