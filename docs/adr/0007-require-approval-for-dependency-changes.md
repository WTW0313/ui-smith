# Require Approval for Dependency Changes

UI Smith v1 will detect missing dependencies and include proposed Dependency Changes in the Generation Plan, but it will not install or upgrade packages without explicit developer approval. Dependency and lockfile changes are significant host repository modifications and should remain intentional.

## Consequences

The Agent Skill must identify the package manager, list exact package changes, and show the command it intends to run. If approval is not given, UI Smith may still generate source that assumes manually installed dependencies only when the developer explicitly accepts that path.
