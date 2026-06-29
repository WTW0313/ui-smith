# Strict Kit Manifest And Agent Inventory

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Implement the schema-backed Kit Manifest as root `ui-smith.json`. The manifest should include a Component Inventory, scaffold provenance, Styling Contract summary, Design Source, selected Deterministic Generation Contracts, generated Verification Evidence, and AI-facing usage guidance. The workflow should also add a Manifest Pointer to agent-facing project instructions.

The manifest is not lifecycle state. It must not track drift or imply UI Smith owns future maintenance.
The Component Inventory should make the Normalized Kit Layout explicit so Coding Agents do not infer component paths or setup readiness from naming rules.

## Acceptance criteria

- [ ] `ui-smith.json` is strict JSON and validates against a Manifest Schema.
- [ ] The manifest records scaffolded components, categories, usage notes, Component Setup Status, Explicit Component Import guidance, and concrete artifact paths in a Component Inventory.
- [ ] The manifest records Artifact Status metadata for source, contract, brief, example, test, story, and verification artifacts, including explicit non-blocking statuses for absent optional artifacts.
- [ ] The Manifest Schema restricts Artifact Status to `scaffolded`, `pending-agent-authoring`, `pending-approval`, `not-requested`, `unsupported`, and `skipped`.
- [ ] The Manifest Schema restricts Component Setup Status to `planned`, `in-progress`, `blocked`, `ready`, and `skipped`.
- [ ] A component is marked `ready` only when required artifacts meet the readiness rule and optional artifacts have explicit non-blocking statuses.
- [ ] The Component Inventory is treated as authoritative but verifiable by the skill.
- [ ] The manifest records Styling Contract summary, Design Source, selected contract IDs/versions/hashes, and verification artifact summary.
- [ ] The manifest records scaffold provenance, including UI Smith generation version and Base UI version used for the initial scaffold.
- [ ] The manifest does not record Generated File Fingerprints, drift state, Upgrade Plans, or lifecycle metadata.
- [ ] A Manifest Pointer is added to agent-facing instructions when initializing a kit.
- [ ] Existing agent-facing instructions are updated in place without clobbering unrelated content.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/01-minimal-ui-smith-tracer-bullet.md
