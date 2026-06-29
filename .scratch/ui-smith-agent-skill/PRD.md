# UI Smith Agent Skill PRD

Status: ready-for-agent

## Problem Statement

Developers who want to build web apps quickly still need a full set of accessible, production-ready UI components that fit their application's design language. Existing UI libraries either impose a visual system, require manual assembly of headless primitives, or leave teams without enough Verification Evidence to trust generated output in production.

UI Smith should solve this as a portable Agent Skill first. It should help a Coding Agent scaffold App-Owned Component Source for React applications, using Base UI Primitives as the accessibility and interaction foundation while preserving Host Repository Conventions and letting teams customize the result through App-Owned Design Tokens.

The product model is scaffold-first only. UI Smith creates a strong initial Component Kit for a new or existing project. After scaffolding, all later component changes belong to the application team and are ordinary app development work, not a UI Smith lifecycle.

## Solution

UI Smith will be an Agent Skill that inspects a host repository, presents a Generation Plan, and, after approval, scaffolds a React Component Kit. The kit will use Base UI Primitives for Primitive-Backed Components, native semantics for Semantic Components, Tailwind-first styling with CSS variable-backed Design Tokens, and Test-Backed Generation whenever the host repository has a compatible test setup.

UI Smith should use Hybrid Generation. Deterministic contracts define the allowed output shape, file targets, Base UI Primitive requirements, Styling Contract, Dependency Change rules, manifest expectations, and Verification Evidence. A Coding Agent may then author or adapt the component source, examples, tests, and token mappings inside those constraints. Static templates should not be used to scaffold component source.

The skill will create a strict JSON Kit Manifest named `ui-smith.json`, with a Component Inventory and scaffold provenance for future Coding Agents. It will also create a Kit README near the generated Component Kit and create or update `DESIGN.md` according to the Design Documentation Standard when token decisions are resolved.

UI Smith should preserve the host repository's convention for where the Component Kit Root lives, then enforce a Normalized Kit Layout inside that root. Each component gets its own flat lowercase/kebab-case Component Folder, all per-component artifacts live in that folder, compound component parts stay in one source file, and imports target concrete component files instead of barrel files or directory indexes.

V1 will use a simple skill folder format while keeping the workflow, contract, and manifest format portable enough to support different Coding Agents.

## User Stories

1. As an app developer, I want to scaffold a React Component Kit from Base UI Primitives, so that I can build application screens without assembling every primitive manually.
2. As an app developer, I want generated components to be App-Owned Component Source, so that my team can edit and customize them freely after scaffolding.
3. As an app developer, I want UI Smith to inspect my repository before writing, so that it follows my existing structure and conventions.
4. As an app developer, I want to review a Generation Plan before files are written, so that I understand the components, paths, dependencies, styling assumptions, and Verification Evidence.
5. As an app developer, I want dependency changes to require explicit approval, so that package and lockfile changes remain intentional.
6. As an app developer, I want Tailwind-first styling with CSS variable-backed Design Tokens, so that customization is fast and consistent.
7. As an app developer, I want generated Design Tokens to be app-owned, so that UI Smith does not impose a permanent visual identity.
8. As an app developer, I want UI Smith to read `DESIGN.md` when present, so that generated components align with the project's documented design direction.
9. As an app developer, I want UI Smith to infer tokens from CSS variables, Tailwind theme values, or token files when `DESIGN.md` is missing, so that existing visual decisions are preserved.
10. As an app developer, I want a guided Token Customization Workflow when design information is incomplete, so that important visual decisions are made explicitly.
11. As an app developer, I want UI Smith to create or update `DESIGN.md` after confirmed token decisions, so that future Coding Agents have a canonical Design Source.
12. As an app developer, I want generated components to include typed APIs, so that usage errors are caught early.
13. As an app developer, I want a Dual-Layer Component API, so that common use stays simple while advanced composition remains possible.
14. As an app developer, I want App-Facing Components for common workflows, so that product screens can be built quickly.
15. As an app developer, I want Composable Parts available for advanced cases, so that I can customize structure without forking behavior.
16. As an app developer, I want a consistent Variant System, so that component size, intent, tone, density, and state styling remain predictable.
17. As an app developer, I want UI Smith to preserve an existing variant convention when one is detected, so that generated code fits my project.
18. As an app developer, I want Semantic Components included where useful, so that the initial kit can cover practical app UI beyond Base UI exports.
19. As an accessibility reviewer, I want generated components to include Accessibility Verification, so that accessibility claims are backed by evidence.
20. As an accessibility reviewer, I want Base UI behavior treated as a foundation rather than a certification, so that generated wrappers are still tested.
21. As a test-minded developer, I want tests generated by default when my repository supports them, so that generated components are easier to trust.
22. As a test-minded developer, I want UI Smith to avoid installing a test stack without approval, so that my project controls its tooling.
23. As a frontend developer, I want examples for every generated component, so that I can see the intended usage quickly.
24. As a frontend developer, I want UI Smith to ask whether to use Storybook for Visual Presentation, so that I can choose the extra tooling cost.
25. As a Storybook user, I want stories generated when Storybook is already present or approved, so that component states are easy to inspect.
26. As a form builder, I want form components to stay form-library-neutral, so that they work with native React and multiple form libraries.
27. As a form builder, I want Form Adapter Examples when a form library is detected, so that integration with React Hook Form or TanStack Form is clear.
28. As a Next.js developer, I want UI Smith to handle client boundaries and framework-specific CSS entry points, so that interactive components work correctly.
29. As a Vite developer, I want UI Smith to adapt to Vite project conventions, so that generated files fit the application.
30. As a developer in another React setup, I want a generic React fallback, so that UI Smith can still help even if my framework is not first-class in v1.
31. As a Coding Agent, I want a Kit Manifest with a Component Inventory, so that I know which project components already exist and how to import them.
32. As a Coding Agent, I want a Manifest Pointer in agent-facing instructions, so that I discover the Kit Manifest before inventing new UI.
33. As a Coding Agent, I want the Component Inventory to be authoritative but verifiable, so that I prefer existing components while still checking the repository.
34. As a maintainer, I want the Kit Manifest to record scaffold provenance, so that future agents can understand which UI Smith generation rules, Base UI version, and contracts were used initially.
35. As an app developer, I want no generated-by headers in source files, so that scaffolded components feel like normal app-owned code.
36. As a design-system maintainer, I want the Kit README to explain usage, customization, verification, and scaffold provenance, so that humans and Coding Agents can work from the same guidance.
37. As a design-system maintainer, I want UI Smith to generate only the required Integration Layer, so that the skill does not restructure my app.
38. As a product team, I want a Neutral Visual Default, so that generated components look professional before brand customization.
39. As a product team, I want tokens to be the key customization mechanism, so that visual changes scale across the Component Kit.
40. As a Coding Agent, I want deterministic JSON contracts plus Markdown Contract Briefs, so that I can author components dynamically while still satisfying validateable constraints.
41. As a Coding Agent, I want each component's source, contract, brief, example, test, story, and verification note to live in one Component Folder, so that I can inspect the full setup without searching shared artifact folders.
42. As a developer, I want UI Smith imports to target concrete component files instead of barrel files, so that component usage stays explicit and easy for Coding Agents to verify.
43. As a Coding Agent, I want the Component Inventory to record concrete artifact paths and import paths, so that I do not infer paths from naming conventions.
44. As a Coding Agent, I want Component Setup Status and Artifact Status values in the manifest, so that I can understand setup progress before using or modifying a component.
45. As an app developer, I want UI Smith to detect Component Layout Conflicts before writing, so that existing components are not moved, overwritten, or silently adopted.

## Implementation Decisions

- UI Smith v1 is a portable Agent Skill distributed in a simple folder format.
- V1 is React-only because Base UI is a React primitive library.
- UI Smith is scaffold-first only. It does not provide a re-run, upgrade, migration, or ongoing component-kit management lifecycle.
- The skill scaffolds App-Owned Component Source rather than an npm UI library or dependency wrapper.
- Component source should be LLM-authored or LLM-adapted under Deterministic Generation Contracts, not copied from static templates.
- Deterministic Generation Contracts are represented as machine-checkable JSON contracts plus Markdown Contract Briefs.
- Static component templates are not part of the production scaffolding path.
- The default Styling Contract is Tailwind-first with CSS variable-backed Design Tokens.
- Design Tokens are app-owned and should be mapped to existing project tokens when possible.
- The Generation Plan is interactive by default and must be approved before writing App-Owned Component Source.
- Dependency Changes must be detected, listed with exact commands, and explicitly approved before installation.
- The skill preserves Host Repository Conventions for where the Component Kit Root lives, but the Normalized Kit Layout is non-optional inside that root.
- The Normalized Kit Layout uses flat lowercase/kebab-case Component Folders and lowercase/kebab-case file names for source, contracts, briefs, examples, tests, stories, and verification notes.
- Component Folder locality overrides central host test, story, example, or contract folder conventions for UI Smith component artifacts.
- Compound components keep their App-Facing Component and Composable Parts in the same component source file instead of splitting each Base UI part into a separate file.
- Component imports must use Explicit Component Imports: the host repository's alias when available, otherwise relative paths, always targeting the concrete component file and never a barrel file or directory index.
- UI Smith must not create component barrel files, root kit component barrels, or `index` modules for component re-exports.
- Shared Kit Utilities are allowed at the Component Kit Root only when at least two Component Folders need them, and they must not re-export components.
- Component-local CSS files are not part of the default Normalized Kit Layout; styling should flow through kit-root tokens and component source classes unless the Generation Plan records an explicit reason.
- Component Layout Conflicts are reported in the Generation Plan before writes. UI Smith must ask the user to choose `skip`, `replace`, or `scaffold-new` instead of moving, overwriting, or silently adopting existing components.
- `scaffold-new` creates a distinct component identity in the Component Inventory and records the original requested component for traceability.
- The First Component Set includes foundation components, overlays, navigation/disclosure components, and feedback components: Button, Input, Textarea, Select, Checkbox, Radio Group, Switch, Label, Field/Error Message, Dialog, Popover, Tooltip, Dropdown Menu, Tabs, Accordion, Toast, and Alert.
- Components are classified as Primitive-Backed Components or Semantic Components so accessibility and Base UI claims stay precise.
- Generated components should use a Dual-Layer Component API with App-Facing Components and Composable Parts.
- The default Variant System is CVA-style when no Host Repository Convention exists, but adding a Variant Utility is a Dependency Change.
- The skill generates only the required Integration Layer for selected components.
- Form components are Form-Library-Neutral by default, with Form Adapter Examples for detected form libraries.
- V1 supports Framework-Aware Generation for Next.js and Vite, with a generic React fallback.
- The Kit Manifest is strict JSON, named `ui-smith.json`, and backed by a Manifest Schema.
- The Kit Manifest records Component Inventory, scaffold provenance, Styling Contract summary, Design Source, selected contracts, generated verification artifacts, and AI-facing usage guidance.
- The Component Inventory records each component's Component Setup Status, folder, concrete artifact paths, explicit import path, artifact statuses, and traceability for renamed `scaffold-new` components.
- Artifact Status values are limited to `scaffolded`, `pending-agent-authoring`, `pending-approval`, `not-requested`, `unsupported`, and `skipped`.
- Component Setup Status values are limited to `planned`, `in-progress`, `blocked`, `ready`, and `skipped`.
- A component can be marked `ready` only when source, contract, brief, example, and verification artifacts are `scaffolded`; tests are `scaffolded` or explicitly non-blocking with a reason; and stories are `scaffolded`, `not-requested`, `unsupported`, or `skipped`.
- The Kit Manifest must not record Generated File Fingerprints, drift state, Upgrade Plans, or any lifecycle state implying UI Smith owns future maintenance.
- A Manifest Pointer is added to agent-facing project instructions so Coding Agents discover the Kit Manifest.
- The Kit Manifest is authoritative but verifiable for Coding Agent usage.
- The skill generates a Kit README near the Component Kit.
- UI Smith reads `DESIGN.md` first as the Design Source, then falls back to CSS variables, Tailwind theme values, or token files.
- UI Smith creates or updates `DESIGN.md` after confirmed token decisions and follows the Design Documentation Standard.
- `DESIGN.md` must cover design principles, Design Tokens, component styling rules, accessibility rules, responsive rules, and concrete do/avoid guidance.
- Examples are generated for every component. Storybook is optional and must be proposed or approved before adding new Storybook dependencies.
- Source files should not include generated-by headers or UI Smith ownership markers.

## Testing Decisions

- The main test seam is running UI Smith end-to-end against fixture host repositories.
- Fixture repositories should include Next.js with Tailwind, Vite with Tailwind, an app with existing `DESIGN.md`, an app with CSS tokens but no `DESIGN.md`, an app with an existing compatible test setup, and an app with no compatible test setup.
- Tests should verify externally observable behavior: generated manifest contents, contract artifacts, scaffolded source files, token outputs, Kit README, design documentation, examples, proposed dependency changes, generated tests or checklists, and absence of upgrade/fingerprint lifecycle metadata.
- Tests should verify Normalized Kit Layout behavior: Component Kit Root detection, flat lowercase/kebab-case Component Folders, component-local artifacts, no barrel files or directory-index imports, explicit import paths, shared kit-root artifacts, and manifest Component Setup Status plus Artifact Status values.
- Tests should cover Component Layout Conflicts by proving UI Smith reports conflicts and waits for `skip`, `replace`, or `scaffold-new` approval instead of moving, overwriting, or silently adopting existing files.
- Tests should not overfit private implementation details when an end-to-end fixture assertion can prove the same behavior.
- Accessibility Verification is layered: Testing Library and user-event behavior tests when supported, axe checks when available or approved, Playwright checks when already present or explicitly requested, and manual accessibility guidance always.
- Test-Backed Generation should create tests by default when the host repository has a compatible setup.
- If no compatible test setup exists, UI Smith should generate a verification checklist and recommend a setup instead of installing one without approval.
- Hybrid Generation should be tested by giving the Coding Agent a Deterministic Generation Contract and Contract Brief, then verifying that the scaffolded source, examples, tests, manifest, and README satisfy the contract.
- Scaffold-first behavior should be tested by confirming there is no `upgrade` command, no Generated File Fingerprints, no drift language, and no source-level generated-by markers.
- Dependency Change behavior should be tested by using fixtures with missing packages and verifying that UI Smith proposes commands rather than running them without approval.
- Component API tests should prioritize App-Facing Component usage, with focused coverage for Composable Parts where advanced composition could affect accessibility.

## Out of Scope

- Publishing a standalone npm UI library in v1.
- Supporting Vue, Svelte, Solid, or non-React frameworks in v1.
- Re-running UI Smith to upgrade or migrate an existing Component Kit.
- Tracking Generated File Fingerprints or drift after scaffolding.
- Supporting alternate internal layouts for UI Smith-scaffolded components.
- Creating barrel files, directory-index component exports, or root kit component re-export modules.
- Installing Storybook, test frameworks, axe, Playwright, or variant utilities without explicit approval.
- Formal accessibility certification.
- Maintaining a UI Smith-owned canonical theme or preset marketplace.
- Generating every Base UI component in v1.
- Complex components such as data tables, date pickers, command palettes, and full combobox workflows unless added in a later scoped release.
- Separate skills per React framework in v1.

## Further Notes

The product promise is trustable scaffolding, not ongoing component lifecycle management. UI Smith should make its assumptions visible, preserve host project choices, and leave behind enough structured state for future Coding Agents to use the Component Kit correctly.

Base UI should be described as the accessibility and behavior foundation for Primitive-Backed Components. Semantic Components should be described separately so UI Smith does not overclaim Base UI coverage.
