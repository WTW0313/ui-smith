# Verification

Use this reference when deciding Verification Evidence, accessibility checks, contract validation, or checklist coverage.

## Contract Checks

Before accepting scaffolded source, verify that it satisfies the selected JSON Deterministic Generation Contract:

- Required files exist.
- Required exports exist.
- Required component artifacts live in the relevant Component Folder.
- Primitive-Backed Components use the selected Base UI primitive.
- Semantic Components use valid native semantics and do not overclaim Base UI behavior.
- Styling uses the Styling Contract and App-Owned Design Tokens where practical.
- Kit Manifest, Kit README, examples, and verification artifacts are updated.

## Layered Accessibility Verification

Generate the strongest approved layer the host repository can support:

- Testing Library and user-event behavior tests when compatible tooling exists.
- Axe checks when axe tooling already exists or the user approves adding it.
- Playwright checks when Playwright already exists or the user approves adding it.
- Manual checklist guidance always.

Tests, accessibility checks, and verification notes live directly in the relevant Component Folder. Represent every generated, omitted, pending, or unsupported verification artifact with Artifact Status metadata in the Component Inventory.

Accessibility guidance must cover labels, keyboard interaction, focus visibility, disabled state, loading state, error state, reduced motion where relevant, and valid semantics.

Base UI is an accessibility and behavior foundation for Primitive-Backed Components, not a certification. Wrappers still need checks.

## Test-Backed Generation

Write tests by default only when the host repository has compatible tooling. Do not install test tooling without explicit approval.

Tests should assert external behavior:

- App-Facing Component usage.
- Keyboard and pointer interactions.
- Focus management for overlays and disclosure components.
- Open, closed, active, inactive, disabled, loading, and error states where relevant.
- Form labels, descriptions, validation messaging, and error state wiring.

If no compatible test setup exists, write a verification checklist and recommend setup. The checklist is Verification Evidence, not a substitute for runnable tests when runnable tests are available.
