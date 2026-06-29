# Keep Form Components Library-Neutral

UI Smith v1 will generate Form-Library-Neutral Components by default and add Form Adapter Examples when the host repository already uses a form library such as React Hook Form or TanStack Form. Base UI supports form primitives and common integrations, but UI Smith should not force a form stack into the host repository.

## Considered Options

- Keep generated form components form-library-neutral.
- Make React Hook Form the default form integration.
- Generate mandatory adapters for multiple form libraries.

## Consequences

Generated field, input, select, checkbox, radio, switch, and validation components must expose ordinary React and native form integration points. Form Adapter Examples are documentation and examples, not required runtime infrastructure.
