# Generate Only the Required Integration Layer

UI Smith v1 will generate the minimal Integration Layer needed for the selected components to work in the host repository. This may include shared class utilities, token CSS, export files, or required provider/viewport components, but it should not restructure the application or scaffold unrelated app infrastructure.

## Consequences

The Generation Plan must identify which integration files are required by the selected components and why. Integration Layer changes should follow Host Repository Conventions and remain scoped to the Component Kit.
