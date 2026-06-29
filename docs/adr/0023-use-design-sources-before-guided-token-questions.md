# Use Design Sources Before Guided Token Questions

UI Smith v1 will start token customization by reading the host repository's Design Source, preferring `DESIGN.md` when present and falling back to existing CSS variables, Tailwind theme values, or other token files. If the Design Source is missing or incomplete, UI Smith will use a Token Customization Workflow to ask structured questions about color, radius, density, typography, motion, and dark mode.

## Consequences

The Agent Skill should avoid inventing visual decisions when the host repository already documents them. The Generation Plan must explain which Design Source was used, which tokens were imported or mapped, and which decisions still need developer input.
