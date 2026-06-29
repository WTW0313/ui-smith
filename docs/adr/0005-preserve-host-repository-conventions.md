# Preserve Host Repository Conventions

UI Smith v1 will inspect and preserve detectable Host Repository Conventions instead of always creating a parallel component structure. This prevents generated App-Owned Component Source from competing with an existing design system or forcing a second project style into production applications.

## Consequences

The Agent Skill must run a discovery step before generation and ask for direction when conventions cannot be inferred safely. UI Smith defaults are fallback behavior, not a reason to override a clear host repository pattern.
