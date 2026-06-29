# Record Generation Compatibility in the Kit Manifest

UI Smith v1 will record Generation Compatibility in the Kit Manifest, including the Base UI version targeted by generated components and the Template Version used to create or update them. Generated App-Owned Component Source can depend on specific Base UI APIs, so future agents need an explicit compatibility record instead of assuming the latest dependency is safe.

## Considered Options

- Record Base UI version and UI Smith Template Version in the Kit Manifest.
- Always target the latest Base UI version.
- Use a loose compatibility range without tracking generation details.

## Consequences

The Agent Skill must update compatibility metadata whenever it generates or upgrades components. Future upgrade workflows can compare manifest metadata with installed dependencies and template support before rewriting source.
