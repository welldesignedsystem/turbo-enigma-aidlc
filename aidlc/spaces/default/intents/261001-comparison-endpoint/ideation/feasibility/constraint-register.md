# Constraint Register

## Constraints

| ID | Constraint | Evidence and effect | Handling / owner |
|---|---|---|---|
| C-01 | The confirmed implementation language is Python, but the application repository has no implementation or Python project setup. | The workspace scan found no language or build system; `turbo-enigma/` contains only `.git/`. | Establish the application runtime and HTTP framework before implementation; delivery team. |
| C-02 | The endpoint depends on retrieving two stored runs by ID. | `GET /v1/runs/{run_id}` and a write-once result store are described in draft documents, but no running service or store adapter exists yet. | Confirm the persisted schema and lookup contract before integration; architecture/development. |
| C-03 | Comparison semantics for unlike runs are undefined. | Draft runs can differ by input digest, algorithm set, and `step_counting_version`; no comparison rules cover these cases. | Specify reject/annotate/partial-compare behavior and algorithm pairing in Requirements Analysis; product/architecture. |
| C-04 | Output-difference detail is not defined. | The confirmed need is to show output differences, but no response shape or granularity has been selected. | Define equality and difference representation before contract design; product/architecture. |
| C-05 | Existing run-service performance targets may not hold for Python. | The draft sets p99 under 2 seconds at 10,000 elements and notes this assumes compiled execution; bubble sort can perform 49,995,000 comparisons. | Benchmark worst-case inputs and decide whether to retain the limit and target; development/quality. |
| C-06 | The current security posture is internal and unauthenticated. | Draft security notes say anyone who can reach the service may submit work or read a run with a known ID; persisted runs include input arrays. | Confirm deployment exposure; do not treat opaque IDs as access control. Add appropriate controls before public exposure; security/operations. |
| C-07 | Hosting and operational requirements are undecided. | No AWS account, region, hosting platform, or operating constraints were provided. | Defer infrastructure feasibility until a hosting target is selected; product/operations. |
| C-08 | Capacity, retention, and cost cannot be estimated. | Request volume, retention period, and storage capacity are unspecified; records contain inputs and results. | Establish expected volume and retention before sizing the store; product/operations. |
| C-09 | Research inputs are absent. | `market-research` was skipped; `competitive-analysis`, `market-trends`, and `build-vs-buy` are unavailable. | Do not base technical or product feasibility claims on market evidence; product. |

## Assumptions Requiring Confirmation

- The documented run-retrieval contract and stored `Run` shape remain the intended integration boundary.
- Run records are immutable and retrieval must not execute algorithms again.
- The service remains internal unless a later decision adds authentication, authorization, and per-caller protections.