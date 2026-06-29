# Use Strict JSON Schema for the Kit Manifest

UI Smith v1 will define the Kit Manifest as strict JSON with a Manifest Schema. This gives UI Smith and other Coding Agents a stable, validateable contract for reading Component Inventory, Styling Contract, paths, dependencies, and test policy.

## Considered Options

- Strict JSON with a published schema.
- JSONC.
- Markdown.
- YAML.

## Consequences

The manifest cannot rely on comments or informal prose for meaning. The Agent Skill should validate the Kit Manifest before trusting it and should treat schema evolution as a compatibility concern.
