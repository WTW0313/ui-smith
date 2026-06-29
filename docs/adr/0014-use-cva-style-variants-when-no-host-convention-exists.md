# Use CVA-Style Variants When No Host Convention Exists

UI Smith v1 will use a CVA-style Variant System when the host repository has no existing variant convention. This gives generated components consistent typed variants while preserving Host Repository Conventions when a project already uses another Variant Utility or pattern.

## Consequences

The Agent Skill must detect existing variant patterns before proposing a default. Adding `class-variance-authority` or a similar Variant Utility is a Dependency Change and requires explicit approval before installation.
