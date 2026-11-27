# Release and baseline records

A release record identifies the exact source baseline and the evidence needed to reproduce or review a delivery. Create one only when a release or named delivery baseline is needed.

Name each record `vMAJOR.MINOR.PATCH.md` and use this structure:

```markdown
# Baseline vMAJOR.MINOR.PATCH

- Tag:
- Commit:
- Date:
- Status: Planned | Released | Superseded

## Scope
What capabilities and fixes are included?

## Compatibility
Document API, Jira/Codebeamer, configuration, and data compatibility.

## Configuration and migration
List required settings, migration steps, and operational changes, or state none.

## Validation evidence
List the agreed checks and their outcome, with links where available.

## Known limitations
List relevant limitations or state none.
```

Tags must point to the exact release commit and must not be moved or reused. For a corrected delivery, create a new version and record how it supersedes the earlier baseline.
