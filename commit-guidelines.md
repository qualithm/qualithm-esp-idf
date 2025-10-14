# Commit Guidlines

- Format: type(scope)!: subject
  - type: feat, fix, docs, style, refactor, perf, test, build, ci, chore, revert
  - scope: optional, describes area (e.g., parser, ui)
  - !: optional; indicates a breaking change
  - subject: imperative, lower case, no trailing period
- Body (optional): after a blank line, explain what and why, not how
- Footer (optional): metadata and references
  - BREAKING CHANGE: description
  - Closes/Fixes/Refs: issue references (e.g., Closes #123)
- Reverts: use type revert with the reverted header in quotes in the body; include the SHA
- Release guidance:
  - feat -> minor version
  - fix/perf -> patch version
  - any BREAKING CHANGE or ! -> major version

Examples:

- feat(parser): add async function support
- fix(ui)!: prevent crash on null avatar BREAKING CHANGE: Avatar component API renamed prop "img" to
  "src".
- docs(readme): clarify installation steps
- build(ci): add Node 20 to matrix
- revert: feat(api): add beta endpoints Reverts commit 1a2b3c4.
