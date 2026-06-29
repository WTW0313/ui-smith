# Support Framework-Aware Generation for Next.js and Vite

UI Smith v1 will use Framework-Aware Generation for detected Next.js and Vite React applications, with a generic React fallback for other setups. Interactive Base UI Primitive components often need framework-specific handling such as Next.js client boundaries, CSS entry points, import aliases, and test conventions.

## Considered Options

- Detect Next.js and Vite and adapt generation in v1.
- Generate generic React-only files.
- Split into separate framework-specific skills.

## Consequences

The Agent Skill must inspect the host repository before writing and include framework assumptions in the Generation Plan. Framework-specific handling should stay inside the generation workflow instead of forking the product into separate skills in v1.
