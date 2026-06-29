# Generate App-Owned Component Source

UI Smith will first generate app-owned React component source files instead of a shared npm UI package. This lets developers customize the generated Component Kit deeply while Base UI Primitive behavior remains the accessibility and interaction foundation.

## Considered Options

- Generate app-owned source files into the application repository.
- Publish a dependency wrapper package that applications import from.

## Consequences

Applications own their generated component API and styling decisions. UI Smith must focus on repeatable generation, adaptation, and maintenance workflows rather than promising a stable external component package API in v1.
