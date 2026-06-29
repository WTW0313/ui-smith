# UI Smith

UI Smith is an agent skill for scaffolding app-owned, accessible React component kits from Base UI primitives.

It is scaffold-first: the skill helps create an initial component kit inside a host app, then the app owns the generated source. It does not provide an upgrade, migration, drift detection, or long-term lifecycle workflow.

## Install

Copy `skills/ui-smith` into the skill directory used by your agent runtime.

Then ask your coding agent to use `$ui-smith` in a React repository.

## Contents

- `skills/ui-smith/SKILL.md` - main skill instructions
- `skills/ui-smith/references/` - supporting reference docs loaded as needed
- `CONTEXT.md` and `docs/adr/` - project vocabulary and design decisions
- `.scratch/` - local markdown PRD and issue tracker

## License

MIT
