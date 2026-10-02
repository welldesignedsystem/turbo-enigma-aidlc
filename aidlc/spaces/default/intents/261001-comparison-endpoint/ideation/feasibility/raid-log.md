# RAID Log

## Risks

| ID | Risk | Likelihood | Impact | Response | Owner |
|---|---|---|---|---|---|
| R-01 | Python execution may miss the inherited 10,000-element, p99-under-2-seconds target for the run service. | Medium | High | Benchmark worst-case inputs before finalizing limits; adjust the limit or target only with measured evidence. | Development / Quality |
| R-02 | The documented run-retrieval interface or result store may not exist in an implementable form when integration begins. | High | High | Confirm or build the Python service and storage boundary before endpoint integration. | Architecture / Development |
| R-03 | Comparing records with different inputs, algorithm sets, or step-counting versions could imply a misleading comparison. | Medium | High | Define compatibility and missing-result behavior before freezing the API contract. | Product / Architecture |
| R-04 | Unauthenticated access could expose stored input arrays or allow unbounded compute use if the service is reachable outside its intended internal audience. | Medium | High | Confirm exposure; add transport, access, and request controls before any public deployment. | Security / Operations |
| R-05 | Unspecified retention and traffic volume could cause unexpected storage growth or operating cost. | Medium | Medium | Set retention and expected-volume assumptions before capacity planning. | Product / Operations |

## Assumptions

| ID | Assumption | Validation |
|---|---|---|
| A-01 | The comparison endpoint will read two previously stored run records by their IDs. | Confirm in Requirements Analysis and contract design. |
| A-02 | Run retrieval returns the original stored record and does not recompute metrics. | Preserve the documented immutable retrieval behavior in the implementation contract. |
| A-03 | Python is the selected language for the application. | Confirm framework and project conventions when the repository is initialized. |
| A-04 | The first deployment is intended for internal users. | Confirm the hosting boundary before deployment design. |

## Issues

| ID | Issue | Status | Next action |
|---|---|---|---|
| I-01 | The application repository has no source code, build configuration, test suite, or implemented run store. | Open | Establish the executable Python service foundation and verify the retrieval path. |
| I-02 | The project docs are drafts and their stated technical targets have not been measured. | Open | Review the load-bearing API and NFR assumptions before implementation. |
| I-03 | The comparison response has no defined policy for unlike runs or detailed output diffs. | Open | Resolve the response behavior in Requirements Analysis. |

## Dependencies

| ID | Dependency | Needed for | Status |
|---|---|---|---|
| D-01 | Python application runtime and HTTP framework | Registering and serving the endpoint | Not established |
| D-02 | Run repository or retrieval service backed by persistent storage | Loading both records by `run_id` | Described in draft docs; not implemented |
| D-03 | Decisions on input, algorithm-set, and step-counting-version compatibility | A non-misleading comparison contract | Pending requirements analysis |
| D-04 | Intended hosting and access boundary | Security and operational planning | Undecided |

## Sources

- `intent-statement` and confirmed answers in `feasibility-questions.md`.
- `turbo-enigma-knowledge-base/api/run-retrieval-endpoint.md`, `architecture/data-model.md`, `nfr/performance.md`, `nfr/security.md`, and `nfr/scalability.md`.
- `competitive-analysis`, `market-trends`, and `build-vs-buy` were not available because `market-research` was skipped.