# Upgrade-Aware Workflow

Status: wontfix

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

This issue is obsolete. UI Smith is now scaffold-first only and intentionally does not provide a re-run, upgrade, migration, drift-detection, or ongoing component-kit management lifecycle.

Superseded by:

- docs/adr/0027-use-scaffold-first-generation-with-no-upgrade-lifecycle.md
- docs/adr/0028-limit-the-kit-manifest-to-inventory-and-scaffold-provenance.md

## Acceptance criteria

- [ ] No implementation work should be picked up from this issue.
- [ ] Any existing `upgrade` command, Generated File Fingerprints, drift metadata, or Upgrade Plan behavior should be removed under the scaffold-first work.
- [ ] The Kit Manifest should remain a Component Inventory and scaffold provenance record only.

## Blocked by

Closed as obsolete by scaffold-first product decision.

## Comments

Closed because UI Smith is now a scaffold-first tool. App-owned component changes after initial scaffolding are ordinary application development, not a UI Smith upgrade lifecycle.
