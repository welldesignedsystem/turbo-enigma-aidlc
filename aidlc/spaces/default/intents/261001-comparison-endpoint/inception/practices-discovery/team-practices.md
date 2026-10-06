# Team Practices (Lead Draft)

These are suggested defaults for human review, not confirmed team practices. The project is greenfield and the practices interview has not yet occurred.

## Way of Working

- Suggested default (not confirmed): We use trunk-based development with `main` as the base and merge target, keep feature branches short-lived (typically 1-2 days), and squash-merge.
- Source: `aidlc/spaces/default/memory/org.md`. No existing team branching or merge practice is established by the available project evidence.

## Walking Skeleton

- Suggested default (not confirmed): We build a thin end-to-end slice first. The active `feature` scope sets `skeleton: on`; after the pre-implementation decisions are settled, the first slice should exercise the comparison request, stored-run retrieval, comparison, and API response through the intended integration boundary.
- This is a proposed scope-aligned default, not a team commitment. Storage/retrieval ownership and the behavior for differing algorithm sets remain open and must be resolved before implementation.

## Testing Posture

- **Methodology**: test-after
- **Ordering**: Implement each applicable testable layer, then write and run that layer's tests.
- Suggested defaults (not confirmed): This follows the organization-level default in `org.md`. The active `feature` scope adds an 80% line-coverage floor and CI execution before merge.
- Applicable workflow guardrail, not a confirmed team practice: requirements must be testable, and user-story acceptance criteria use Given/When/Then.
- Test-design ownership and available QA/reviewer coverage are unconfirmed. The greenfield application has no established test tooling or CI configuration from which to infer existing practice.

## Deployment

- Suggested default (not confirmed): We deploy on merge to staging and require separate human approval before production deployment.
- Source: `aidlc/spaces/default/memory/org.md`. Hosting, exposure, deployment topology, and operations ownership are undecided; this is not evidence of an existing pipeline or environment.

## Code Style

- Suggested default (not confirmed): We defer to project-level formatter and linter configuration; for the selected Python language, use idiomatic Python conventions such as `snake_case` where no project configuration states otherwise.
- No application formatter, linter, or style configuration has been established for this greenfield project.