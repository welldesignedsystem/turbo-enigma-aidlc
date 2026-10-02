# Scope Definition Questions

## Confirmed Context

- Compare two existing runs by run ID, using the documented retrieval interface and result store. [feasibility]
- Include output differences and all available metrics without ranking or recommendation. [feasibility]
- Use a Python stack. [feasibility]
- Hosting and operational requirements remain undecided. [feasibility]

## Q1. First useful comparison response
The confirmed need includes output differences and all available metrics, but the exact output detail is still open. What must the first useful response show?

- A. Both stored outputs and all available metrics, plus whether the outputs match
- B. Both stored outputs, all available metrics, and element-level output differences
- C. All available metrics and an output match/mismatch indicator, without returning both full outputs
- D. Not yet defined
- X. Other (please specify)

[Answer]: A. Both stored outputs and all available metrics, plus whether the outputs match

## Q2. Runs with different inputs
Two stored runs can have different input digests. Should the endpoint compare them, or require the same input for a meaningful comparison?

- A. Reject the comparison unless both runs have the same input digest
- B. Allow it, but identify that the inputs differ and avoid implying an apples-to-apples comparison
- C. Allow it and compare the stored results without a special input-difference warning
- D. Not yet defined
- X. Other (please specify)

[Answer]: C. Allow it and compare the stored results without a special input-difference warning

## Q3. Runs with different step-counting versions
Stored runs record the ruleset used to count comparisons and moves. How should the endpoint handle runs with different step-counting versions?

- A. Reject the comparison unless both runs use the same version
- B. Return each run's metrics and version, clearly marking the counts as not directly comparable
- C. Compare the recorded counts without special handling
- D. Not yet defined
- X. Other (please specify)

[Answer]: A. Reject the comparison unless both runs use the same version

## Q4. Delivery priority
The retrieval implementation and comparison rules are both unresolved. Which should be addressed first in the delivery sequence?

- A. Confirm the run retrieval and storage integration first
- B. Deliver the basic comparison response first, then refine edge-case behavior
- C. Settle the rules for comparing unlike runs before implementation work
- D. No sequencing preference
- X. Other (please specify)

[Answer]: C. Settle the rules for comparing unlike runs before implementation work

## Consolidated Summary Confirmation

- Compare two stored runs by ID using the documented retrieval interface and result store.
- The first useful response includes both stored outputs, all available metrics, and whether the outputs match.
- Runs with different input digests may be compared without a special input-difference warning.
- Reject comparisons when the runs use different step-counting versions.
- Settle the rules for comparing unlike runs before implementation work.

Does this all look correct before I generate the artifact?

- Looks correct
- Request changes

[Answer]: Looks correct