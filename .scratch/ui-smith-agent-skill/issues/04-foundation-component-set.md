# Foundation Component Set

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Scaffold the First Component Set foundation components: Button, Input, Textarea, Select, Checkbox, Radio Group, Switch, Label, and Field/Error Message. The components should be LLM-authored or adapted under Deterministic Generation Contracts and Contract Briefs, then verified against Dual-Layer Component APIs, tokenized styling, a consistent Variant System, clear Primitive-Backed Component versus Semantic Component taxonomy, examples, and Verification Evidence.
Each foundation component should follow the Normalized Kit Layout: a flat lowercase/kebab-case Component Folder, lowercase/kebab-case files, component-local artifacts, Explicit Component Imports, and no barrel files.

## Acceptance criteria

- [ ] The selected foundation components can be generated into a fixture host repository.
- [ ] Each foundation component has a JSON Deterministic Generation Contract and Markdown Contract Brief.
- [ ] Each foundation component's source, contract, brief, example, test or checklist, story when present, and verification note are placed directly in that component's flat lowercase/kebab-case Component Folder.
- [ ] LLM-Authored Component Source satisfies the relevant contract before the scaffold is accepted.
- [ ] Primitive-Backed Components use Base UI Primitives for behavior and accessibility foundation.
- [ ] Semantic Components use native HTML and ARIA semantics without overclaiming Base UI behavior.
- [ ] Each component has an App-Facing Component API for common usage.
- [ ] Components that need advanced composition expose Composable Parts from the same component source file as the App-Facing Component.
- [ ] Component import guidance uses Explicit Component Imports and does not introduce barrel files, directory-index imports, or root kit component re-export modules.
- [ ] Components use the detected Host Repository Convention for variants when one exists.
- [ ] When no host variant convention exists, a CVA-style Variant System is proposed.
- [ ] Adding a Variant Utility is treated as a Dependency Change that requires approval.
- [ ] Form-related components stay Form-Library-Neutral.
- [ ] Examples and Verification Evidence are generated for each component.
- [ ] The Kit Manifest and Kit README are updated with the generated foundation components, concrete artifact paths, Component Setup Status, and Artifact Status metadata.
- [ ] Generated source files do not include generated-by headers or UI Smith ownership markers.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/01-minimal-ui-smith-tracer-bullet.md
- .scratch/ui-smith-agent-skill/issues/02-design-source-and-token-customization-workflow.md
- .scratch/ui-smith-agent-skill/issues/03-strict-kit-manifest-and-agent-inventory.md
- .scratch/ui-smith-agent-skill/issues/12-hybrid-generation-contracts.md
