# Represent Generation Contracts as JSON Plus Markdown

UI Smith should represent each Deterministic Generation Contract as a machine-checkable JSON contract plus a Markdown Contract Brief. The JSON contract is the source of truth for validation, file targets, requirements, component taxonomy, dependencies, and Verification Evidence. The Contract Brief explains intent, examples, and tradeoffs for Coding Agents and humans.

## Consequences

Coding Agents should generate LLM-Authored Component Source from the Contract Brief, but validation and manifest updates should rely on the JSON contract. Markdown instructions must not add hidden requirements that are absent from the JSON contract.
