# Project-Level Rules

> Project-specific specialisation and corrections. Loaded after `org.md` and
> `team.md` as strict-additive guidance; contradictions with broader policy
> are rejected. Populated by practices-discovery and the self-learning loop.
>
> Use sparingly: most teams don't need a project layer. Reach for it
> only when this specific project needs stable, durable guidance beyond the
> team practice (for example, package-specific release checks or an additional
> regression suite for a legacy component).

## Way of Working

<!-- Project-specific specialisation. Example: -->
<!-- This monorepo requires package-scoped branch names and a package owner -->
<!-- review in addition to the team's normal merge policy. -->

## Walking Skeleton

<!-- Project-specific specialisation. Example: -->
<!-- The walking skeleton must exercise the legacy service adapter as well -->
<!-- as the new service boundary. -->

## Testing Posture

<!-- Project-specific specialisation. -->

## Guard Policy

<!-- Project-specific. Mode: strict, relaxed, or off. Strict here holds for every intent and cannot be changed from chat. A section under the retired Change Control heading, written by an earlier release, is still read. -->

## Deployment

<!-- Project-specific specialisation. -->

## Code Style

<!-- Project-specific specialisation. -->

## Tech Stack

<!-- Technology choices locked for this project. -->

## Decided

<!-- Decisions made in earlier stages that should not be re-asked. -->
<!-- Format: DECIDED: [decision] (Stage [slug], [date]) -->

## Scope Overrides

<!-- Custom scope rules for this project. -->

## Forbidden

<!-- Populated by practices-discovery affirmation gate. -->
<!-- Format: NEVER [behavior] (affirmed [date]) -->
<!-- Example: NEVER throw exceptions across service layer boundaries (affirmed 2026-05-17) -->

## Mandated

<!-- Populated by practices-discovery affirmation gate. -->
<!-- Format: ALWAYS [behavior] (affirmed [date]) -->
<!-- Example: ALWAYS use Result<T,E> for fallible operations in service layer (affirmed 2026-05-17) -->

## Corrections

<!-- Project-specific corrections from human feedback. -->
<!-- Format: NEVER/ALWAYS [behavior] (learned [date]) -->
- comparison includes both per-run metrics and output differences; the follow-up resolved an apparent mismatch between earlier answers. (learned 2026-10-02) <!-- cid:261001-comparison-endpoint:intent-capture:76776629f9798ca3972115c921e812f51389c1cd0fd0f256b46e928396305c91 -->
- The selected Python stack is feasible for the read-only comparison path, but the draft run-service latency target assumes compiled execution; keep that performance claim open until measured against the real implementation. (learned 2026-10-02) <!-- cid:261001-comparison-endpoint:feasibility:666a0ff17c0d8e55385cfc88c9612a2f55ddd46fd135c29a7fed6ff4222a0574 -->
- Treat input and step-counting-version compatibility as separate scope decisions; they affect different claims about whether stored metrics and outputs can be compared fairly. (learned 2026-10-02) <!-- cid:261001-comparison-endpoint:scope-definition:67eed5e18032ce425e656352812b3b37b43620229691e72c5a4cfba01d298b71 -->
- Team formation confirms one developer with dedicated capacity and occasional reviews, not a mob; storage/retrieval, testing, and operational skill coverage remain unconfirmed and should be assigned before implementation. (learned 2026-10-02) <!-- cid:261001-comparison-endpoint:team-formation:a5f94c5c5669796dda0a569849cceb170f7ecfc39854d0e383cd1fc040028671 -->
- Carry the unresolved algorithm-set policy and storage/testing ownership into the handoff as pre-implementation items (learned 2026-10-02) <!-- cid:261001-comparison-endpoint:approval-handoff:62d47471690e0f7786f514a70379cfef6d1879f2d6553e1a46098260d6dd14b4 -->
