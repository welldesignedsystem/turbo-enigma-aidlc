## Q1. Runs to compare
The current retrieval API draft fetches a stored run by `run_id`. How should the comparison endpoint identify its two runs?

- A. Accept two existing run IDs and compare their stored results
- B. Accept two run requests, execute them, and compare the new results
- C. Support both existing run IDs and new run requests
- D. Not yet defined
- X. Other (please specify)

[Answer]: A. Accept two existing run IDs and compare their stored results

## Q2. Comparison output
The run response contains `elapsed_ns`, `comparisons`, and `moves`; the API draft warns that elapsed time varies by environment and should not be used alone to rank algorithms. What should comparison results emphasize?

- A. Show time and step metrics side by side, with a clear timing caveat
- B. Emphasize deterministic comparisons and moves; show elapsed time as secondary context
- C. Show output differences and all available metrics without ranking or recommendation
- D. Not yet defined
- X. Other (please specify)

[Answer]:

## Q3. Existing interfaces and storage
The current drafts describe `POST /v1/runs` for creating runs and `GET /v1/runs/{run_id}` for retrieving stored runs. What dependencies should the comparison endpoint use?

- A. Reuse the existing run retrieval interface and result store
- B. Read stored runs through an internal service or repository layer
- C. Compare only results supplied directly in the comparison request
- D. Not yet defined
- X. Other (please specify)

[Answer]:

## Q4. Technical stack
The workspace scan did not identify a language, framework, or build system. What stack or existing project standard should implementation follow?

- A. Use the stack already established in the application repository
- B. A specific stack is required; I will name it
- C. The stack has not been decided
- X. Other (please specify)

[Answer]:

## Q5. Data and compliance constraints
The current run examples use integer arrays and algorithm measurements. Are there privacy, security, retention, or regulatory requirements for stored runs or comparison responses?

- A. No additional requirements are known
- B. The data is internal and must follow existing organizational controls
- C. Specific privacy, security, retention, or regulatory requirements apply
- D. Not yet defined
- X. Other (please specify)

[Answer]:

## Q6. Delivery constraints
Are there budget, timeline, release, or organizational constraints that affect this endpoint?

- A. No specific constraints are known
- B. There is a target date or milestone; I will specify it
- C. There is a budget or capacity limit; I will specify it
- D. There are organizational blockers or dependencies; I will specify them
- E. Not yet defined
- X. Other (please specify)

[Answer]:

## Q7. Hosting and operations
The project drafts do not establish which cloud accounts or hosting services are in use. Where must the endpoint run, and are there operational requirements to preserve?

- A. Follow the existing application hosting and deployment setup
- B. A specific AWS account, region, or service is required; I will specify it
- C. Hosting and operational requirements are not yet decided
- X. Other (please specify)

[Answer]:
