# Limit the Kit Manifest to Inventory and Scaffold Provenance

In the scaffold-first model, `ui-smith.json` should be a Component Inventory and scaffold provenance record only. It should tell Coding Agents which components exist, how to import and use them, which Styling Contract was scaffolded, which Design Source informed the scaffold, and which verification artifacts were generated.

## Consequences

The Kit Manifest should not store Generated File Fingerprints, drift status, Upgrade Plans, or metadata that implies UI Smith owns future maintenance. Future Coding Agents may use the manifest to avoid duplicate UI, but they should treat the generated source as ordinary app-owned code.
