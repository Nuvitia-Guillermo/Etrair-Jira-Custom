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

Use lowercase words separated by hyphens. Do not commit project work directly to `main`. Avoid force-pushing shared branches.

## Commits

Use Conventional Commit messages:

```text
<type>(optional-scope): <short imperative summary>
```

Common types: `feat`, `fix`, `docs`, `refactor`, `test`, `build`, and `chore`. Add a breaking-change note in the commit body when applicable.

## Pull requests and review

- Target `main` and link the issue being addressed.
- Summarize the user-visible and technical changes.
- Describe validation performed, or explain why validation was not applicable.
- Call out configuration, security, migration, compatibility, and versioning effects.
- Update `CHANGELOG.md` for changes that belong in a release.
- Keep design decisions and implementation aligned; update the decision record if the approved design changes.
- Resolve review comments before merging. Prefer a new corrective commit over rewriting published history.

## Baselines, versioning, and releases

Treat `main` as the current integration baseline. For reproducible work, identify a baseline by an immutable commit SHA or a release tag; do not use a moving branch name as a baseline.

Use Semantic Versioning tags in the form `vMAJOR.MINOR.PATCH`. While the project is pre-1.0, use `0.MINOR.PATCH`: increment MINOR for new capabilities or incompatible contract changes, and PATCH for compatible fixes. Reserve `1.0.0` for the first agreed stable release.

When a release or delivery baseline is needed:

1. Confirm the intended scope is merged to `main`, the working state is clean, and the agreed validation is recorded.
2. Update `CHANGELOG.md` and any configuration, migration, or operator guidance affected by the release.
3. Create a new version tag on the exact release commit. Never move or reuse a published tag; issue a new patch version for corrections.
4. Add a baseline record under `docs/releases/` with the tag, commit SHA, scope, compatibility notes, configuration/migration notes, and validation evidence.
5. Create a GitHub Release from that tag with a concise summary, known limitations, and required artifacts when applicable.

Do not create a tag or release for routine analysis, design, or unmerged work. This governance setup does not assign a release version.

## Security and project maintenance

- Never commit credentials, access tokens, private keys, customer data, or production exports.
- Keep local configuration out of version control; provide sanitized examples only when useful.
- Use the least access needed for integrations and document security-sensitive decisions.
- Keep dependency declarations and lockfiles in sync when the chosen stack requires them.
- Review dependency and runtime version changes as part of the pull request.
- Keep documentation, issue templates, and release records aligned with the current implementation.
