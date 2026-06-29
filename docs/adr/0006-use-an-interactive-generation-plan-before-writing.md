# Use an Interactive Generation Plan Before Writing

UI Smith v1 will inspect the host repository and present a Generation Plan before writing App-Owned Component Source. This makes the workflow slower than an immediate generator, but it gives developers a chance to confirm paths, components, styling assumptions, dependency changes, and Verification Evidence before production UI code is added.

## Considered Options

- Present an interactive Generation Plan before writing.
- Generate immediately from inferred assumptions.
- Require command-style options before every run.

## Consequences

The Agent Skill must separate discovery from writing and treat user approval as part of the workflow. A faster default path can be added later once the assumptions are proven reliable.
