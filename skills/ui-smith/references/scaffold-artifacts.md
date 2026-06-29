# Scaffold Artifacts

Use this reference when creating or validating a Generation Plan, Kit Manifest, Kit README, Design Source, Integration Layer, examples, Storybook stories, or form adapter examples.

## Normalized Kit Layout

Preserve the host repository's Component Kit Root location, then apply the Normalized Kit Layout inside that root.

Rules:

- Each component gets one flat lowercase/kebab-case Component Folder.
- Component source, contract, brief, example, test, story, and verification artifacts are component-local artifacts that live directly in that Component Folder as lowercase/kebab-case files.
- Compound components keep the App-Facing Component and Composable Parts in the same component source file.
- Use Explicit Component Imports: the host repository's alias when available, otherwise relative paths, always targeting the concrete component file.
- Do not create component barrel files, root kit component barrels, `index` re-export modules, or directory-index imports.
- Component Folder locality overrides central host test, story, example, contract, and verification folders for UI Smith component artifacts.
- Kit-wide artifacts such as `tokens.css`, the Kit README, Shared Kit Utilities, providers, and other Integration Layer files live at the Component Kit Root.
- Shared Kit Utilities are allowed only when at least two Component Folders need them, and they must not re-export components.
- Component-local CSS files are not part of the default layout; styling should flow through kit-root tokens and component source classes unless the Generation Plan records an explicit reason.

## Generation Plan

The Generation Plan must show:

- Selected components and whether each is Primitive-Backed or Semantic.
- Normalized Kit Layout target files and why each file is required.
- Selected Deterministic Generation Contracts and Contract Briefs, including versions or hashes when available.
- Base UI Primitive requirements for Primitive-Backed Components.
- Styling Contract assumptions, Design Source, App-Owned Design Tokens, and unresolved token questions.
- Framework assumptions for Next.js, Vite, or generic React.
- Component Layout Conflicts and the approved resolution: `skip`, `replace`, or `scaffold-new`.
- Dependency Changes with exact commands.
- Examples, optional Storybook output, form adapter examples, and Verification Evidence.

When an existing file or component conflicts with a normalized target path, do not move, overwrite, or silently adopt it. Ask for `skip`, `replace`, or `scaffold-new`. A `scaffold-new` result is a distinct component identity and records the originally requested component for traceability.

## Design Source

Read `DESIGN.md` first. If it is missing, infer visual decisions from CSS variables, Tailwind theme values, token files, and existing components before asking token questions.

Create or update `DESIGN.md` after confirmed decisions. It must include design principles, Design Tokens, component styling rules, accessibility rules, responsive rules, and concrete do/avoid guidance.

## Kit Manifest

Write root `ui-smith.json` as strict JSON. It records:

- Component Inventory: component names, categories, usage notes, Component Setup Status, Explicit Component Import guidance, concrete artifact paths, Artifact Status metadata, and `scaffold-new` traceability when relevant.
- Scaffold provenance: UI Smith generation rules, Base UI version, Design Source, and selected contracts used for the initial scaffold.
- Styling Contract summary.
- Selected contract provenance.
- Verification Evidence summary.
- AI-facing usage guidance.

Artifact Status values are limited to:

- `scaffolded`
- `pending-agent-authoring`
- `pending-approval`
- `not-requested`
- `unsupported`
- `skipped`

Component Setup Status values are limited to:

- `planned`
- `in-progress`
- `blocked`
- `ready`
- `skipped`

A component can be marked `ready` only when source, contract, brief, example, and verification artifacts are `scaffolded`; tests are `scaffolded` or explicitly non-blocking with a reason; and stories are `scaffolded`, `not-requested`, `unsupported`, or `skipped`. If source is `pending-agent-authoring`, the component is `in-progress`, not `ready`.

It must not record file fingerprints, drift state, Upgrade Plans, lifecycle state, or any claim that UI Smith owns future maintenance.

Add a Manifest Pointer to agent-facing instructions, updating existing files in place without clobbering unrelated content.

## Integration Layer

Generate only support code required by the selected components and framework context:

- Shared Kit Utilities only when at least two Component Folders need them.
- Token CSS only as required by the Styling Contract, at the Component Kit Root.
- Providers, viewports, portals, positioners, and framework hooks only when selected components need them.
- Contract artifacts only for selected components, inside the relevant Component Folder.
- No component barrel files, directory-index imports, root kit component re-export modules, or component re-export utilities.

Do not reorganize the host application.

## Visual And Form Output

Every scaffolded component receives an example directly in its Component Folder. If Storybook already exists, propose stories in the Generation Plan and place stories directly in the relevant Component Folder. If Storybook is missing, ask whether the user wants Storybook for Visual Presentation and treat installation as a Dependency Change.

When React Hook Form or TanStack Form is detected, add optional Form Adapter Examples for relevant form components directly in the relevant Component Folder. Shared form guidance belongs in the Kit README or another justified Component Kit Root artifact. Do not install a form library without approval.
