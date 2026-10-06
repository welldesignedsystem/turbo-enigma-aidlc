# Practices Discovery Evidence (Lead Draft)

## Project Context

- Greenfield project in `feature` scope; the application repository has no established implementation, test tooling, CI configuration, or deployment configuration to inspect.
- Market Research and Rough Mockups were skipped. There is no market-validation evidence or user-interface design evidence to use as a basis for practices.
- The API and run-retrieval design documents are described by the approved handoff as drafts, not implemented or independently validated behavior.

## Inspected Sources

- Lead (`aidlc-pipeline-deploy-agent`): read the Practices Discovery stage instructions, active `org.md`, `project.md`, and `phases/inception.md` rule files, the active feature scope configuration, and this record's state.
- Lead: read `ideation/approval-handoff/initiative-brief.md`, `ideation/approval-handoff/decision-log.md`, and `ideation/approval-handoff/approval-handoff-questions.md` for approved scope and handoff conditions.
- Lead: read `ideation/team-formation/team-assessment.md`, `ideation/team-formation/skill-matrix.md`, and `ideation/team-formation/team-formation-questions.md` for confirmed capacity and skill evidence.
- No support-agent reviews or human practices interview have occurred in this lead-draft step.

## Confirmed Team Facts

- One developer has dedicated capacity and confirmed Python/API development skill; capacity is not quantified.
- Occasional reviews are expected, but reviewer identity and cadence are unspecified.
- No mob or external partner/contractor is planned.
- Storage/retrieval integration, test-design/QA, security, and operations coverage are not confirmed.

## Suggested Defaults, Not Confirmed Practices

- Way of Working: `org.md` suggests trunk-based development, `main` as base and target, short-lived branches, and squash merges. No team-specific branching practice is established.
- Walking Skeleton: `org.md` makes this scope-dependent; the active `feature` scope sets `skeleton: on`. A thin end-to-end slice is therefore suggested, subject to the unresolved pre-implementation decisions.
- Testing Posture: `org.md` suggests test-after with layer-by-layer test ordering. The `feature` scope adds an 80% line-coverage floor and CI execution before merge. Neither is yet confirmed as an available team capability or adopted practice.
- Applicable inception workflow guardrails require testable requirements and Given/When/Then user-story acceptance criteria. These are framework requirements, not evidence of an affirmed team testing methodology.
- Deployment: `org.md` suggests deploy-on-merge to staging and a human-approved production gate. Hosting and exposure are undecided, so no actual deployment practice is known.
- Code Style: `org.md` suggests deferring to project-level configuration and idiomatic language conventions. No project formatter or linter configuration exists yet.

## Approved Project Decisions and Constraints

- The API compares two previously stored runs by run ID, returns both outputs and available per-run metrics, and indicates whether outputs match; it does not rank or recommend.
- Different input digests are allowed without a special warning; differing `step_counting_version` values are rejected.
- The algorithm-set behavior must be decided before implementation. Storage/retrieval integration ownership and test-design ownership must also be confirmed before implementation.
- Python is selected, but the framework and hosting are undecided. Performance against inherited targets is unmeasured; do not present target performance as validated.

## Unresolved Uncertainty

- The practices interview must confirm or revise all five proposed practice areas: Way of Working, Walking Skeleton, Testing Posture, Deployment, and Code Style.
- The policy for comparing runs with different algorithm sets remains open.
- Storage/retrieval integration and test-design ownership remain open; security and operations ownership depend on the hosting and exposure decision.
- No named reviewer, review cadence, delivery date, budget, or quantified developer capacity is established.

## Draft Status

This is the lead's initial draft only. Independent support reviews, the human interview, final integration, and affirmation have not occurred.