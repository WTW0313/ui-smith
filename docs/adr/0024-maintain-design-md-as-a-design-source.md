# Maintain DESIGN.md as a Design Source

UI Smith v1 will create or update `DESIGN.md` during the Token Customization Workflow after the developer confirms design and token decisions. This gives future Coding Agents a canonical Design Source instead of forcing them to infer visual intent from generated CSS alone.

## Consequences

UI Smith must not invent design language silently. When `DESIGN.md` is missing, the Agent Skill should derive it from approved token decisions and detected project styles, then write it according to the Design Documentation Standard.
