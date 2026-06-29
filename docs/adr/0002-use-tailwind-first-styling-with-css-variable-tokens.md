# Use Tailwind-First Styling With CSS Variable Tokens

UI Smith v1 will generate components with Tailwind-first styling and CSS variable-backed Design Tokens. Base UI is intentionally styling-agnostic, so choosing a default Styling Contract gives generated Component Kits a consistent customization model while still allowing teams to revise the App-Owned Component Source.

## Considered Options

- Tailwind-first classes with CSS variable-backed Design Tokens.
- CSS Modules-first generated components.
- Plain CSS-first generated components.
- A full styling adapter system in v1.

## Consequences

V1 can produce consistent, inspectable React Component Kits quickly, but teams not using Tailwind will need a later adapter or manual conversion path. The generated components should keep behavior in Base UI Primitives and keep visual decisions isolated behind Design Tokens wherever practical.
