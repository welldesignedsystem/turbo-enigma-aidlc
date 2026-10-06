# Practices Discovery Questions

## Confirmed Context

- This is a greenfield Python/API project; no application, CI, test, or deployment configuration exists yet. [evidence.md]
- One developer has dedicated capacity and Python/API skills; occasional reviews are expected, but retrieval/storage integration, test-design, security, and operations ownership are not confirmed. [team-assessment.md]
- The choices below are team-practice decisions. Organization defaults and feature-scope requirements are suggestions or workflow requirements, not evidence of practices already in use. [org.md]
- The approved comparison scope remains unchanged: compare two stored runs, include both outputs and available metrics, indicate output equality, allow different input digests without a special warning, and reject different `step_counting_version` values. [scope-document.md]

## Q1. Branching and integration
What branching and merge approach should this team use for the project? The organization suggests short-lived branches from `main` and squash merges, but no project convention exists yet.

- A. Use short-lived branches from `main`, merge to `main`, and squash-merge
- B. Use short-lived branches from `main`, but preserve individual commits when merging
- C. Use another branching or merge approach; describe it
- D. Defer this choice until implementation setup
- X. Other (please specify)

[Answer]:

## Q2. Thin end-to-end slice
Build a thin end-to-end slice first? A walking skeleton is a minimal version that runs the whole way through, built first to prove the pieces connect before the real features go in. For this project, that could exercise the comparison request, stored-run retrieval, comparison, and API response.

- A. Yes, build and verify that thin slice first
- B. No, build in another order; describe the preferred order
- C. Not decided yet
- X. Other (please specify)

[Answer]:

## Q3. Testing methodology
Which approach should guide how tests and implementation are sequenced? The organization-level fallback is test-after; the feature scope separately requires an 80% line-coverage floor and CI execution before merge.

- A. Test-after: implement a testable layer, then write and run that layer's tests
- B. TDD: write a failing test before implementing each behavior
- C. BDD: define behavior scenarios before implementation, then implement against them
- D. ATDD: agree on acceptance tests before implementation, then build to pass them
- E. Custom or mixed approach; describe the method
- X. Other (please specify)

[Answer]:

## Q4. Test ordering
What explicit ordering should the team follow when adding tests? For example, should behavior-level scenarios precede lower-level tests, or should each layer be implemented and tested before moving to the next?

- A. Implement and test one layer at a time before moving to the next
- B. Define API-level acceptance tests first, then implement and add lower-level tests
- C. Write tests for the complete change after implementation, before merge
- D. Use another ordering; describe it
- E. Defer ordering until the architecture and storage boundary are known
- X. Other (please specify)

[Answer]:

## Q5. Test ownership and quality checks
Who should own test design and execution, and which checks should be required before merge? Testing ownership is not confirmed; this project has no test runner, coverage configuration, or CI yet. Select all that apply.

- A. The developer owns test design, execution, and coverage reporting
- B. An engineering reviewer shares test-design and review responsibility
- C. Assign a QA/test specialist if one is available; availability must be confirmed
- D. Keep ownership unassigned until the Inception plan names an owner
- E. Require the feature-scope 80% line-coverage floor and passing CI checks before merge
- F. Decide tools and exact merge checks after the application and CI are selected
- X. Other (please specify)

[Answer]:

## Q6. Deployment approach
What release approach should be the working team practice? The organization suggests deployment to staging on merge and a separate human approval for production, but no hosting or environments are selected.

- A. Adopt staging deployment on merge and require human approval for production
- B. Use a different release process; describe it
- C. Defer the practice until hosting and environments are selected
- D. Not decided yet
- X. Other (please specify)

[Answer]:

## Q7. Python code conventions and tools
What code-style conventions should the team adopt for the new Python project? No formatter, linter, type checker, or project configuration is present. Select all that apply.

- A. Follow idiomatic Python naming and defer to checked-in project configuration
- B. Adopt Black as formatter and configure a Python linter for CI
- C. Select formatter, linter, and type-checking tools during project setup
- D. Keep tool selection open until the developer proposes a setup
- X. Other (please specify)

[Answer]:

## Q8. Security checks and ownership
Which security practices should be required as the project and hosting are set up? No CI provider, deployment target, scanner, or security/operations owner is established. Select all that apply, and use Other to name any required owner or threshold.

- A. Add automated secret and dependency checks to CI
- B. Add source-code security scanning to CI and define who triages findings
- C. Add dynamic scanning once a reachable test environment exists
- D. Require protected-branch checks and least-privilege CI credentials
- E. Defer tool and threshold choices until hosting and CI are selected; public exposure still requires a security decision
- F. Not decided yet
- X. Other (please specify)

[Answer]:
