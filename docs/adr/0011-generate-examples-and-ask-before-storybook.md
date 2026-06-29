# Generate Examples and Ask Before Storybook

UI Smith v1 will generate usage examples for components and ask whether the developer wants Storybook for Visual Presentation. If Storybook is already present, UI Smith may propose stories in the Generation Plan; if it is missing, adding Storybook is a Dependency Change that requires explicit approval.

## Consequences

Every generated component should have usage guidance even without Storybook. Storybook is treated as an optional presentation surface, not as required infrastructure or a substitute for Verification Evidence.
