# Use Hybrid Generation With Deterministic Contracts

UI Smith should move from static-template component generation to Hybrid Generation. Deterministic contracts should define the Generation Plan, file ownership, manifest updates, Dependency Changes, Base UI Primitive constraints, and Verification Evidence, while a Coding Agent authors or adapts the App-Owned Component Source inside those constraints.

## Considered Options

- Generate components from static templates.
- Let a Coding Agent freely generate components from broad guidance.
- Use Hybrid Generation with deterministic contracts and verification.

## Consequences

UI Smith can produce components that better match the host repository, `DESIGN.md`, and local conventions, but the workflow must treat LLM output as untrusted until it satisfies the Deterministic Generation Contract and produces Verification Evidence. Static templates are not part of the production scaffolding path.

The deterministic side owns the contract shape: Generation Plan, dependency rules, manifest schema, Component Inventory, file targets, Base UI Primitive requirements, required component states, and verification requirements. The Coding Agent may author component source, examples, tests, and token mappings only inside that contract.
