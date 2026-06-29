# Support Upgrade-Aware Generation Without Automatic Migration

Status: superseded by ADR-0027

UI Smith v1 will be upgrade-aware but not a full automatic migrator. It will use Generation Compatibility metadata to detect drift and present an Upgrade Plan, but it will not silently rewrite App-Owned Component Source or overwrite application edits.

## Considered Options

- Generate components only, with no structured upgrade workflow.
- Detect drift and present Upgrade Plans.
- Automatically migrate generated components across versions.

## Consequences

The Agent Skill must distinguish generated baseline code from app-owned modifications where possible and show proposed changes before applying them. Upgrade support should prioritize preserving developer edits over achieving automatic migration coverage.
