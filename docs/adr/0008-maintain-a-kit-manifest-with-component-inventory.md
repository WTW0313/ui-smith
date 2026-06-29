# Maintain a Kit Manifest With Component Inventory

UI Smith v1 will maintain a Kit Manifest for each generated Component Kit. The manifest records generation decisions and includes a Component Inventory so Coding Agents can understand which components are available in the project instead of guessing imports or recreating duplicate UI.

## Consequences

The Agent Skill must update the Kit Manifest whenever it adds, changes, or removes generated components. The manifest is both workflow state for UI Smith and usage guidance for future Coding Agent sessions.
