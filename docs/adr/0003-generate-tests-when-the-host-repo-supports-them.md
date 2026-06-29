# Generate Tests When the Host Repo Supports Them

UI Smith v1 will generate tests by default when the host repository already has a compatible test setup. This makes Verification Evidence part of the Component Kit workflow without forcing a test framework installation into repositories that have not chosen one.

## Considered Options

- Generate tests by default when a compatible host test setup exists.
- Generate test guidance only.
- Ask every time whether tests should be generated.
- Install a full test stack automatically.

## Consequences

The Agent Skill must inspect the host repository before generation and adapt test output to the detected setup. When no compatible setup exists, it should produce a verification checklist and recommend a setup instead of adding new dependencies without explicit approval.
