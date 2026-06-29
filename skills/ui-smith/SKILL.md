---
name: ui-smith
description: Scaffold app-owned, accessible React Component Kits from Base UI primitives. Use when a developer wants an initial production-ready React UI kit, token-customizable components, Base UI-backed component source, or an AI-readable component inventory.
---

# UI Smith

UI Smith is scaffold-first. It creates an initial React Component Kit, then the host application owns the source. Do not provide a rerun, upgrade, migration, drift-detection, or ongoing component-lifecycle workflow.

## Workflow

1. Inspect the host repository before planning.
   - Confirm it is a React repository and classify it as Next.js, Vite, or generic React.
   - Read `DESIGN.md` first. If it is missing, inspect CSS variables, Tailwind configuration, token files, existing component conventions, import aliases, test setup, Storybook setup, form libraries, package dependencies, and agent-facing instructions.
   - Detect the Component Kit Root and any Component Layout Conflicts before proposing files.
   - Completion criterion: you can name the detected framework, Design Source, Component Kit Root, import alias, styling convention, test convention, missing Dependency Changes, Component Layout Conflicts, and any token decisions that still require user input.

2. Create a Generation Plan before writing files.
   - The plan must list selected components, Normalized Kit Layout target files, Deterministic Generation Contracts, Contract Briefs, Base UI Primitive requirements, Styling Contract assumptions, Design Source, App-Owned Design Tokens, Integration Layer files, examples, Visual Presentation options, Verification Evidence, Component Layout Conflicts, and Dependency Changes with exact commands.
   - Ask the user whether they want Storybook for Visual Presentation when Storybook is not already present and stories would be useful.
   - For each Component Layout Conflict, ask the user to choose `skip`, `replace`, or `scaffold-new` before writing.
   - Ask for explicit approval before writing files or changing dependencies. Dependency approval is separate from file-write approval.
   - Completion criterion: the user has approved the plan, and every proposed dependency install, removal, upgrade, Storybook setup, test-tool setup, axe setup, Playwright setup, or Variant Utility has explicit approval before it is run.

3. Scaffold App-Owned Component Source under contracts.
   - Use Hybrid Generation: JSON Deterministic Generation Contracts define the checkable constraints, and Markdown Contract Briefs explain intent and tradeoffs. The Coding Agent may author or adapt the component source inside those constraints.
   - Do not scaffold component source from static templates. Contracts steer agent-authored source.
   - Preserve the host repository's Component Kit Root location, then enforce the Normalized Kit Layout inside that root: flat lowercase/kebab-case Component Folders, component-local artifacts, Explicit Component Imports, and no barrel files or directory-index imports.
   - Scaffold Primitive-Backed Components with current Base UI primitives, and mark Semantic Components separately when native HTML and ARIA semantics are used.
   - Use a Dual-Layer Component API: App-Facing Components for common use and Composable Parts where advanced composition is expected.
   - Preserve Host Repository Conventions when detectable except where the Normalized Kit Layout intentionally overrides central artifact folders. Use a CVA-style Variant System only when no host convention exists, and treat adding a Variant Utility as a Dependency Change.
   - Use Tailwind-first styling with CSS variable-backed App-Owned Design Tokens. Avoid hard-coded visual values where practical.
   - Do not add generated-by headers, UI Smith ownership markers, file fingerprints, drift metadata, Upgrade Plans, or lifecycle state.
   - Completion criterion: every approved component folder, example, contract artifact, manifest entry, README entry, token file, Design Source update, Integration Layer file, and optional visual/form artifact has been written or intentionally skipped with Artifact Status metadata.

4. Leave behind agent-readable kit state.
   - Write root `ui-smith.json` as strict JSON with Component Inventory, scaffold provenance, Styling Contract summary, Design Source, selected contract provenance, Verification Evidence summary, Component Setup Status, Artifact Status metadata, concrete artifact paths, Explicit Component Imports, and AI-facing usage guidance.
   - Add or update a Manifest Pointer in agent-facing instructions without clobbering unrelated content.
   - Write a Kit README near the Component Kit that explains available components, usage rules, customization through tokens, verification commands, Integration Layer boundaries, and scaffold provenance.
   - Create or update `DESIGN.md` after confirmed token decisions using the Design Documentation Standard.
   - Completion criterion: `ui-smith.json`, the Kit README, `DESIGN.md`, and agent-facing instructions agree on component paths, usage guidance, token customization, and scaffold provenance.

5. Produce Verification Evidence.
   - Generate tests when the host repository already has compatible test tooling. If it does not, write a verification checklist and recommend setup instead of installing tooling without approval.
   - Use layered Accessibility Verification: behavior tests where supported, axe checks when present or approved, Playwright checks when present or approved, and manual accessibility guidance always.
   - Verify external behavior and contract satisfaction rather than private implementation details.
   - Completion criterion: approved checks have run, failures are reported with next steps, and unsupported layers have checklist coverage instead of silent omission.

## References

- Load [`references/component-scope.md`](references/component-scope.md) when selecting, authoring, or validating components.
- Load [`references/scaffold-artifacts.md`](references/scaffold-artifacts.md) when planning manifest, README, Design Source, Integration Layer, examples, Storybook, or form-adapter output.
- Load [`references/verification.md`](references/verification.md) when deciding tests, accessibility checks, contract checks, or checklist coverage.
