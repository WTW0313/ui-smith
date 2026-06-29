# Framework-Aware Next.js And Vite Support

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Add Framework-Aware Generation for Next.js and Vite host repositories, with a generic React fallback. The workflow should adapt generated files, imports, client boundaries, CSS entry points, examples, and tests to the detected framework without forking UI Smith into separate framework-specific skills.
Framework-aware behavior should preserve the detected Component Kit Root location while keeping the Normalized Kit Layout inside that root.

## Acceptance criteria

- [ ] A Next.js fixture is detected correctly.
- [ ] Interactive generated components in Next.js include appropriate client-boundary handling.
- [ ] Next.js CSS entry points and import aliases are handled according to Host Repository Conventions, while component imports still target concrete component files.
- [ ] A Vite fixture is detected correctly.
- [ ] Vite CSS entry points and import aliases are handled according to Host Repository Conventions, while examples and tests stay component-local in the Normalized Kit Layout.
- [ ] A generic React fallback is available when neither Next.js nor Vite is detected.
- [ ] The workflow preserves the host repository's Component Kit Root location but does not opt out of the Normalized Kit Layout inside that root.
- [ ] Framework assumptions are shown in the Generation Plan.
- [ ] Framework-specific behavior is covered by end-to-end fixture tests.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/01-minimal-ui-smith-tracer-bullet.md
- .scratch/ui-smith-agent-skill/issues/03-strict-kit-manifest-and-agent-inventory.md
