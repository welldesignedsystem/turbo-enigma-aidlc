# Scope Definition

## Intended Value

Internal users and developers can inspect two previously saved algorithm runs together for teaching and learning. The comparison presents the recorded outputs and metrics without ranking algorithms or recommending a winner.

## In Scope

- Compare exactly two existing runs identified by their run IDs.
- Use the documented run retrieval and result-store boundary; do not run the algorithms again as part of comparison.
- Include both stored output arrays, all available per-run metrics, and an indication of whether the outputs match.
- Permit comparisons when the input digests differ; do not add a special input-difference warning.
- Reject comparisons when the runs have different `step_counting_version` values.
- Use Python as the selected implementation language. Framework and hosting choices remain for later design.

## Out of Scope

- Creating new runs as part of a comparison; callers select existing run IDs.
- Ranking or recommending algorithms, including sorting results by any metric.
- Element-level output-difference detail in the first useful response.
- Comparing more than two runs in one request.
- Run listing or historical search.

## Priorities

### Must Have

- Retrieve and compare two stored runs by ID.
- Return both outputs and all available per-run metrics, with an output-match indicator.
- Reject a pair whose step-counting versions differ.
- Allow differing input digests without a special warning.

### Should Have

- Define behavior for runs whose selected algorithm sets differ before the comparison contract is finalized. The current decisions do not specify whether unmatched algorithms reject the request or appear as one-sided results.

### Could Have

- Element-level output-difference detail, beyond returning both arrays and indicating whether they match.

### Won't Have in This Scope

- Metric-based ranking or an overall performance score.
- New run execution, run browsing, or multi-run comparison.

## Value Stream

An internal user selects two saved run IDs; the service retrieves both immutable run records; the comparison presents each run's outputs and metrics plus whether the outputs match; the user inspects the evidence without being given a ranking or recommendation.

## Delivery Sequence and Dependencies

1. Close the remaining comparison-contract question about runs with different algorithm sets, while preserving the confirmed input-digest and step-counting-version rules.
2. Confirm that the application can retrieve both stored run records through the documented boundary.
3. Deliver the two-run comparison response with full outputs, available metrics, and the output-match indicator.

The response contract depends on the run retrieval boundary. Implementation follows closure of the remaining comparison rules, as selected in the delivery-priority answer.

## Success Criteria

- A request naming two retrievable runs returns both stored outputs and their available metrics.
- The response indicates whether the two output arrays match.
- Runs with different input digests are not rejected solely for that difference and receive no special input-difference warning.
- Runs with different `step_counting_version` values are rejected.
- Results are not ordered by metrics and contain no winner recommendation.

## Assumptions and Open Questions

- Run IDs address immutable stored records as described by the existing retrieval draft.
- Behavior when the two runs contain different algorithm sets remains open and must be settled before implementation.
- Hosting, exposure, retention, and operational requirements remain undecided, as recorded in feasibility.

## Sources

- `intent-statement` and the confirmed Scope Definition answers in `scope-definition-questions.md`.
- `feasibility-assessment.md` and `constraint-register.md`.
- `turbo-enigma-knowledge-base/api/run-retrieval-endpoint.md` and `architecture/data-model.md` (draft contracts).