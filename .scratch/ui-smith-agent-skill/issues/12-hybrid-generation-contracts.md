# Hybrid Generation Contracts

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Add the scaffold-first Hybrid Generation layer that lets Coding Agents author or adapt component source dynamically while still obeying deterministic, validateable constraints. The slice should introduce JSON Deterministic Generation Contracts and Markdown Contract Briefs for component scaffolding, connect them to the Generation Plan, and record selected contract provenance in the Kit Manifest.

This issue should adapt existing working scaffold behavior where possible. Do not introduce a helper CLI; UI Smith should remain an agent workflow backed by contracts, manifest, token, and verification artifacts.
Contracts should encode the Normalized Kit Layout so agent-authored source and artifacts land in predictable component folders without static templates.

## Acceptance criteria

- [ ] UI Smith has a JSON Deterministic Generation Contract format for component scaffolding.
- [ ] UI Smith has a Markdown Contract Brief format paired with each JSON contract.
- [ ] The Generation Plan lists the selected contracts, versions, hashes, file targets, Normalized Kit Layout targets, Base UI Primitive requirements, Styling Contract requirements, and Verification Evidence requirements.
- [ ] Contracts require lowercase/kebab-case Component Folders and files, component-local artifacts, Explicit Component Imports, and no barrel files.
- [ ] Contracts require compound components to keep App-Facing Components and Composable Parts in the same component source file.
- [ ] Contracts define Component Layout Conflict handling and require user approval for `skip`, `replace`, or `scaffold-new`.
- [ ] A Coding Agent can use the Contract Brief to author LLM-Authored Component Source while validation relies on the JSON contract.
- [ ] Static templates are not used to scaffold component source; examples or fixtures may document expected output but must not drive the production scaffolding path.
- [ ] The Kit Manifest records selected contract provenance, concrete artifact paths, Component Setup Status, and Artifact Status metadata without recording file fingerprints or upgrade metadata.
- [ ] End-to-end fixture tests prove that a scaffolded Button satisfies its contract, manifest entry, README entry, and verification artifacts.
- [ ] The skill instructions explain that scaffolded source is app-owned immediately after scaffolding.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/01-minimal-ui-smith-tracer-bullet.md
- .scratch/ui-smith-agent-skill/issues/03-strict-kit-manifest-and-agent-inventory.md
