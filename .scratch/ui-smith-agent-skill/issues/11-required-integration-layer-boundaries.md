# Required Integration Layer Boundaries

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Constrain UI Smith's scaffolded Integration Layer so it adds only the support code required by selected components and framework context. The workflow should identify shared utilities, exports, providers, token CSS, manifest/contract artifacts, and framework hooks in the Generation Plan and preserve Host Repository Conventions instead of restructuring the application.
The Integration Layer should support the Normalized Kit Layout without becoming a barrel-file or artifact-dump escape hatch.

## Acceptance criteria

- [ ] The Generation Plan lists every proposed Integration Layer file and why it is required.
- [ ] Shared Kit Utilities are generated only when at least two selected Component Folders need them.
- [ ] Token CSS is generated or updated only as required by the Styling Contract.
- [ ] No component barrel files, directory-index imports, root kit component re-export modules, or component re-export utilities are generated.
- [ ] Providers, viewports, portals, or framework hooks are generated only when selected components require them.
- [ ] Contract artifacts are scaffolded only when required by selected components.
- [ ] Contract artifacts are placed directly in the relevant Component Folder rather than a shared contracts folder.
- [ ] Component-local CSS files are not generated unless the Generation Plan records an explicit reason.
- [ ] Existing app structure is not reorganized as part of Integration Layer generation.
- [ ] Integration Layer behavior is covered in Next.js and Vite fixtures.
- [ ] The Kit README explains the generated Integration Layer and how to extend it safely.
- [ ] The Integration Layer does not include upgrade, drift tracking, or lifecycle-management files.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/04-foundation-component-set.md
- .scratch/ui-smith-agent-skill/issues/05-overlay-disclosure-and-feedback-components.md
- .scratch/ui-smith-agent-skill/issues/06-framework-aware-nextjs-and-vite-support.md
