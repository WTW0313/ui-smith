# Layered Accessibility And Test-Backed Generation

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Expand Verification Evidence so scaffolded components use layered Accessibility Verification. The workflow should create tests by default when the host repository has compatible test tooling, propose optional axe or Playwright checks when appropriate, always produce manual accessibility guidance, and verify that LLM-Authored Component Source satisfies its Deterministic Generation Contract.
Verification artifacts should be recorded in the Component Inventory with Artifact Status metadata and placed inside each component's Component Folder.

## Acceptance criteria

- [ ] Fixtures with Testing Library and user-event receive behavior tests for generated components.
- [ ] Fixtures with an approved or existing axe setup receive accessibility checks where appropriate.
- [ ] Fixtures with an approved or existing Playwright setup receive browser-level checks where appropriate.
- [ ] Fixtures without a compatible test setup receive a verification checklist and recommended setup instead of automatic dependency installation.
- [ ] Tests, accessibility checks, and verification notes are placed directly in the relevant Component Folder instead of central test or verification folders.
- [ ] Test, axe, Playwright, and checklist artifacts are represented with Artifact Status metadata, including `pending-approval`, `unsupported`, or `skipped` when a layer is not created.
- [ ] Dependency Changes for test tooling are proposed and require approval.
- [ ] Verification Evidence checks external behavior rather than internal implementation details.
- [ ] Verification Evidence checks that scaffolded source satisfies the selected Deterministic Generation Contract.
- [ ] Accessibility guidance covers labels, keyboard interaction, focus visibility, disabled/loading/error states, reduced motion where relevant, and valid semantics.
- [ ] Primitive-Backed Components and Semantic Components have appropriately scoped accessibility claims.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/04-foundation-component-set.md
- .scratch/ui-smith-agent-skill/issues/05-overlay-disclosure-and-feedback-components.md
- .scratch/ui-smith-agent-skill/issues/12-hybrid-generation-contracts.md
