# Use Layered Accessibility Verification

UI Smith v1 will use layered Accessibility Verification for generated components. Base UI Primitive behavior is the foundation, but UI Smith must still verify generated wrappers, labels, focus behavior, composition, and semantic output because App-Owned Component Source can accidentally break accessibility.

## Considered Options

- Use Testing Library and user-event behavior tests when the host repository supports them.
- Add axe checks when the host repository already has or approves the dependency.
- Add Playwright browser-level checks when the host repository already uses Playwright or explicitly wants that level of verification.
- Rely on a manual checklist only.

## Consequences

Accessibility Verification is evidence, not certification. Every generated component should include manual accessibility guidance, while automated checks adapt to the host repository's existing test stack and approved Dependency Changes.
