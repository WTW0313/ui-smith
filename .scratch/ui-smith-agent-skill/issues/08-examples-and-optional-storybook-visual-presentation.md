# Examples And Optional Storybook Visual Presentation

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Generate examples for every generated component and offer Storybook as an optional Visual Presentation surface. If Storybook already exists, propose stories in the Generation Plan. If Storybook is missing, ask whether the developer wants it and treat installation as a Dependency Change requiring approval.
Examples and stories should follow Component Folder locality even when the host repository has central example or story folders.

## Acceptance criteria

- [ ] Every generated component receives a usage example.
- [ ] Each generated component's example is placed directly in that component's Component Folder.
- [ ] Examples cover important variants, states, and composition paths.
- [ ] The Kit README links or summarizes generated examples.
- [ ] Storybook is detected when present in a fixture host repository.
- [ ] Storybook stories are proposed when Storybook is already present and are placed directly in the relevant Component Folder.
- [ ] When Storybook is missing, the workflow asks whether the developer wants Storybook for Visual Presentation.
- [ ] Installing Storybook is treated as a Dependency Change requiring approval.
- [ ] Story artifacts are represented in the Component Inventory with Artifact Status metadata such as `scaffolded`, `pending-approval`, `not-requested`, `unsupported`, or `skipped`.
- [ ] Storybook output is not treated as a replacement for Verification Evidence.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/04-foundation-component-set.md
- .scratch/ui-smith-agent-skill/issues/05-overlay-disclosure-and-feedback-components.md
