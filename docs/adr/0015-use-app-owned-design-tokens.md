# Use App-Owned Design Tokens

UI Smith v1 will generate default App-Owned Design Tokens and map generated components to existing host repository tokens when detectable. This keeps visual decisions under the application team's control and prevents UI Smith from becoming a canonical theme provider.

## Considered Options

- Generate app-owned token defaults and map to existing tokens when possible.
- Maintain a UI Smith-owned token preset.
- Require existing tokens before generation.

## Consequences

Generated components should reference Design Tokens through the Styling Contract rather than hard-coded visual values wherever practical. UI Smith may provide good defaults, but the host application owns the resulting token names and values.
