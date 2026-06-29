# Track Generated File Fingerprints in the Kit Manifest

Status: superseded by ADR-0027

UI Smith v1 will track Generated File Fingerprints in the Kit Manifest instead of adding noisy generated-by headers to every source file. Fingerprints help the Agent Skill detect app-owned edits before updates or Upgrade Plans while preserving the feeling that generated files belong to the host repository.

## Consequences

The Agent Skill must update fingerprints after approved writes and compare them before changing existing generated files. A fingerprint mismatch should trigger a more cautious Upgrade Plan rather than automatic overwrite.
