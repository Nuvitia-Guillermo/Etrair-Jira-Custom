# Contributing

## Working agreement

Keep this repository focused on the Etrair Jira–Codebeamer customization. The integration flow, API contract, widget behavior, and implementation choices must be discussed and recorded before code is started. Do not treat an open question as an agreed requirement.

## Issues and design

- Use a GitHub issue to describe each goal, defect, or design question.
- For behavior or architecture decisions, capture the context and decision in a short record under `docs/decisions/`.
- Link implementation issues to the relevant accepted design decision when one exists.
- Keep each issue and pull request small enough to review as one coherent change.

## Branches

Create short-lived branches from the latest `main`:

- `feature/<issue-number>-<short-name>` for new behavior
- `fix/<issue-number>-<short-name>` for corrections
- `docs/<issue-number>-<short-name>` for documentation
- `chore/<issue-number>-<short-name>` for maintenance

Use lowercase words separated by hyphens. Do not commit project work directly to `main`.

## Commits

Use Conventional Commit messages:

```text
<type>(optional-scope): <short imperative summary>
```

Common types: `feat`, `fix`, `docs`, `refactor`, `test`, `build`, and `chore`. Add a breaking-change note in the commit body when applicable.

## Pull requests

- Target `main` and link the issue being addressed.
- Summarize the user-visible and technical changes.
- Describe validation performed, or explain why validation was not applicable.
- Call out configuration, security, migration, and versioning effects.
- Update `CHANGELOG.md` for changes that belong in a release.
- Keep design decisions and implementation aligned; update the decision record if the approved design changes.

## Versioning and releases

Use Semantic Versioning tags in the form `vMAJOR.MINOR.PATCH`. While the project is pre-1.0, use `0.MINOR.PATCH`; reserve `1.0.0` for the first agreed stable release. Create tags only for reviewed release points on `main`. Record released changes in `CHANGELOG.md`.

No release version is assigned by this governance setup.
