# Use Scaffold-First Generation With No Upgrade Lifecycle

UI Smith will be scaffold-first only: it creates a strong initial Component Kit for a new or existing project, then all later component changes belong to the application team. UI Smith should not position itself as an ongoing component-kit manager, should not provide a re-run or upgrade workflow, and should not track app-owned edits as drift.

## Considered Options

- Keep upgrade-aware generation with fingerprints and Upgrade Plans.
- Treat UI Smith as a scaffold-first tool with no upgrade lifecycle.

## Consequences

The Kit Manifest remains useful as an AI-facing Component Inventory and scaffold provenance record, but not as lifecycle state for future migrations. UI Smith should avoid commands, metadata, or language that implies it controls generated files after the initial scaffold is accepted.
