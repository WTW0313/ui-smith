# Design Source And Token Customization Workflow

Status: ready-for-agent

## Parent

.scratch/ui-smith-agent-skill/PRD.md

## What to build

Extend UI Smith so token customization starts from the host repository's Design Source. The workflow should read `DESIGN.md` when present, fall back to CSS variables, Tailwind theme values, or token files, and ask structured token questions only when the available design information is incomplete. After confirmed decisions, it should create or update `DESIGN.md` according to the Design Documentation Standard.
Token output should align with the Normalized Kit Layout: shared tokens live at the Component Kit Root, and component-local CSS files require an explicit Generation Plan reason.

## Acceptance criteria

- [ ] A fixture with `DESIGN.md` uses that file as the primary Design Source.
- [ ] A fixture without `DESIGN.md` can import visual decisions from existing CSS variables or Tailwind theme values.
- [ ] Missing design decisions are surfaced as structured token questions before writing.
- [ ] Confirmed decisions produce App-Owned Design Tokens.
- [ ] Generated components consume tokens through the Styling Contract instead of hard-coded visual values where practical.
- [ ] Token CSS is generated or updated at the Component Kit Root rather than inside individual Component Folders.
- [ ] Component-local CSS files are not introduced unless the Generation Plan records an explicit reason.
- [ ] `DESIGN.md` is created when missing and token/design decisions have been confirmed.
- [ ] Created or updated `DESIGN.md` includes design principles, Design Tokens, component styling rules, accessibility rules, responsive rules, and do/avoid guidance.
- [ ] The Generation Plan states which Design Source was used and which decisions still need input.

## Blocked by

- .scratch/ui-smith-agent-skill/issues/01-minimal-ui-smith-tracer-bullet.md
