# Store the Kit Manifest at the Project Root

UI Smith v1 will store the Kit Manifest as `ui-smith.json` at the host repository root and add a Manifest Pointer to the host repository's agent-facing instructions. A root JSON file is easy for tools and Coding Agents to find, while the Manifest Pointer prevents agents from missing the Component Inventory during future work.

## Considered Options

- Store `ui-smith.json` at the host repository root with an agent-facing pointer.
- Store the manifest near generated components.
- Store the manifest under a hidden `.ui-smith/` directory.
- Record the manifest only in `AGENTS.md`.

## Consequences

Host repositories get one visible UI Smith file at the root. The Agent Skill must keep the root manifest and the agent-facing pointer consistent when initializing or updating a Component Kit.
