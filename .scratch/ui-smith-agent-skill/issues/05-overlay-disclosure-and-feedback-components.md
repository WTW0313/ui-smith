# Overlay Disclosure And Feedback Components

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Scaffold the overlay, disclosure, navigation, and feedback components in the First Component Set: Dialog, Popover, Tooltip, Dropdown Menu, Tabs, Accordion, Toast, and Alert. The workflow should use Deterministic Generation Contracts and Contract Briefs, keep the Primitive-Backed Component versus Semantic Component taxonomy visible, and generate examples plus Verification Evidence for interactive behavior, focus handling, and accessibility expectations.
Each component should follow the Normalized Kit Layout, with compound App-Facing Components and Composable Parts exported from one lowercase/kebab-case source file inside a flat Component Folder.

## Acceptance criteria

- [ ] Dialog, Popover, Tooltip, Dropdown Menu, Tabs, Accordion, Toast, and Alert can be generated into a fixture host repository.
- [ ] Each overlay, disclosure, navigation, and feedback component has a JSON Deterministic Generation Contract and Markdown Contract Brief.
- [ ] Each component's source, contract, brief, example, test or checklist, story when present, and verification note are placed directly in that component's flat lowercase/kebab-case Component Folder.
- [ ] LLM-Authored Component Source satisfies the relevant contract before the scaffold is accepted.
- [ ] Primitive-Backed Components use the relevant Base UI Primitives.
- [ ] Alert is handled as a Semantic Component unless a Base UI primitive-backed equivalent is intentionally selected.
- [ ] Components expose App-Facing Components for common usage.
- [ ] Components expose Composable Parts from the same component source file where advanced composition is expected.
- [ ] Required providers, viewports, portals, or positioning helpers are included in the Integration Layer only when needed.
- [ ] Component import guidance uses Explicit Component Imports and does not introduce barrel files, directory-index imports, or root kit component re-export modules.
- [ ] Examples cover common states and interaction flows.
- [ ] Verification Evidence covers keyboard behavior, focus management, and expected open/closed or active/inactive states.
- [ ] The Kit Manifest and Kit README are updated with the generated components, concrete artifact paths, Component Setup Status, and Artifact Status metadata.
- [ ] Generated source files do not include generated-by headers or UI Smith ownership markers.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/04-foundation-component-set.md
- .scratch/ui-smith-agent-skill/issues/12-hybrid-generation-contracts.md
