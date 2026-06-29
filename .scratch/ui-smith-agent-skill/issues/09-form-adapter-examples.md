# Form Adapter Examples

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Keep generated form components Form-Library-Neutral while adding Form Adapter Examples for detected form libraries. The workflow should support examples for common host repository form stacks such as React Hook Form and TanStack Form without making either a required runtime dependency.
Component-specific Form Adapter Examples should live in the relevant Component Folder; shared form guidance belongs in the Kit README or another justified Component Kit Root artifact.

## Acceptance criteria

- [ ] Form components continue to work with standard React props and native form semantics.
- [ ] React Hook Form is detected when present in a fixture.
- [ ] TanStack Form is detected when present in a fixture.
- [ ] Detected form libraries receive Form Adapter Examples.
- [ ] Component-specific Form Adapter Examples are placed directly in the relevant component's Component Folder.
- [ ] Form Adapter Examples are documented as optional usage guidance, not required runtime infrastructure.
- [ ] No form library is installed without explicit approval.
- [ ] Form examples preserve labels, validation messaging, error states, and accessibility expectations.
- [ ] The Kit README and Kit Manifest are updated with form integration guidance, concrete adapter example paths, and Artifact Status metadata.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/04-foundation-component-set.md
