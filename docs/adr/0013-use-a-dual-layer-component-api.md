# Use a Dual-Layer Component API

UI Smith v1 will generate a Dual-Layer Component API: App-Facing Components for common usage and Composable Parts for advanced composition. This keeps generated components productive for routine app screens without hiding the Base UI composition model from teams that need more control.

## Considered Options

- Thin wrappers that closely expose Base UI props and parts.
- Curated App-Facing Components that hide most Base UI structure.
- A dual layer with App-Facing Components and Composable Parts.

## Consequences

Generated components must document both the simple usage path and the advanced composition path. Tests and examples should cover the App-Facing Component first, then include enough Composable Part coverage to show that advanced composition stays accessible.
