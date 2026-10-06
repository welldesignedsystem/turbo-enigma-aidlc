# Discovered Rules (Lead Draft)

Only explicit constraints from the approved project decisions and handoff are included. No additional team-wide practices have been confirmed.

## Mandated

- ALWAYS resolve the behavior for runs with different algorithm sets and confirm ownership of storage/retrieval integration and test design before implementation.
- ALWAYS compare exactly two stored runs identified by run ID, return both outputs and all available per-run metrics, and include an output-match indicator.
- ALWAYS reject comparisons when the runs have different `step_counting_version` values.

## Forbidden

- NEVER rank algorithms or recommend a winner.
- NEVER add a special input-difference warning when the runs have different input digests.