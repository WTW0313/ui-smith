# Do Not Mark Generated Source Files

UI Smith should not add generated-by headers or ownership markers to scaffolded source files. Scaffolded components are App-Owned Component Source immediately after generation, and source-level markers would incorrectly imply ongoing UI Smith ownership.

## Consequences

Scaffold provenance belongs in `ui-smith.json` and the Kit README. Component source files should look and feel like normal project code that the application team can edit freely.
