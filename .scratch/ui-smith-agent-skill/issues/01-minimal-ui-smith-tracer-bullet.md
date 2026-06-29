# Minimal UI Smith Tracer Bullet

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Build the first runnable UI Smith Agent Skill path against a small fixture host repository. The slice should inspect the fixture, present a Generation Plan, and, after approval, scaffold one Primitive-Backed Component for Button with a minimal Kit Manifest, Kit README, App-Owned Design Tokens, and Verification Evidence.

This tracer bullet should preserve any already-working scaffold behavior and evolve it toward scaffold-first Hybrid Generation. Do not recreate completed behavior from scratch when it can be adapted.
The Button scaffold should prove the Normalized Kit Layout with a flat lowercase/kebab-case Component Folder, component-local artifacts, Explicit Component Import guidance, and no barrel files.

## Acceptance criteria

- [ ] A fixture React repository can be used to exercise the workflow end to end.
- [ ] The skill inspects Host Repository Conventions before proposing changes.
- [ ] The skill presents a Generation Plan before writing files.
- [ ] The Generation Plan lists target files, missing Dependency Changes, styling assumptions, Verification Evidence, and any Component Layout Conflicts.
- [ ] Dependency Changes are proposed but not installed without explicit approval.
- [ ] The Button scaffold is produced from a Deterministic Generation Contract and Contract Brief, not from an unconstrained prompt.
- [ ] The generated Button is App-Owned Component Source built on a Base UI Primitive.
- [ ] The generated Button uses Tailwind-first styling with CSS variable-backed App-Owned Design Tokens.
- [ ] The Button source, contract, brief, example, verification note, and generated test or checklist are placed directly in a flat lowercase/kebab-case Button Component Folder.
- [ ] The Button import guidance targets the concrete component source file and does not use a barrel file or directory index.
- [ ] A minimal `ui-smith.json` Kit Manifest is generated with Component Inventory, scaffold provenance, Component Setup Status, Artifact Status metadata, concrete artifact paths, and explicit import path.
- [ ] A local Kit README is generated near the Component Kit.
- [ ] Verification Evidence is generated as a test when the fixture supports it, or as a checklist when it does not.
- [ ] No upgrade command, Generated File Fingerprints, drift metadata, generated-by source headers, barrel files, or root kit component re-export modules are introduced.

## Blocked by

None - can start immediately
