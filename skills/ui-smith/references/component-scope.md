# Component Scope

Use this reference when a run needs component selection, taxonomy, API shape, or component-specific scaffold checks.

## First Component Set

Foundation components:

- Button
- Input
- Textarea
- Select
- Checkbox
- Radio Group
- Switch
- Label
- Field and Error Message

Overlay, disclosure, navigation, and feedback components:

- Dialog
- Popover
- Tooltip
- Dropdown Menu
- Tabs
- Accordion
- Toast
- Alert

## Taxonomy

Primitive-Backed Components use Base UI primitives for accessibility and interaction behavior. Before authoring one, fetch current Base UI documentation for the selected primitive and use the current API surface.

Semantic Components use native HTML and ARIA semantics with the shared Styling Contract. Do not imply they are Base UI-backed. Alert is semantic unless a Base UI primitive-backed equivalent is intentionally selected.

## API Rules

- Every component exposes an App-Facing Component for common product usage.
- Components expose Composable Parts when advanced composition is expected, especially overlays, menus, tabs, accordions, fields, and provider-backed feedback.
- Compound components keep the App-Facing Component and Composable Parts in the same component source file instead of splitting Base UI parts into separate files.
- Form-related components remain Form-Library-Neutral: standard React props, native form semantics, accessible labels, descriptions, validation messaging, disabled state, and error state.
- Components use detected host variant conventions. If none exist, propose a CVA-style Variant System and treat any added Variant Utility as a Dependency Change.
- Source files must not include generated-by headers or UI Smith ownership markers.

## Component Evidence

Each scaffolded component needs:

- A JSON Deterministic Generation Contract.
- A Markdown Contract Brief.
- App-Owned Component Source satisfying the contract.
- A usage example covering important variants, states, and composition paths.
- Verification Evidence suited to the host test setup.
- Kit Manifest and Kit README entries.

All per-component artifacts belong directly in that component's flat lowercase/kebab-case Component Folder.
