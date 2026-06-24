# Gitflow And Release

Use this reference for commits, pushes, versioning, and releases.

## Branch Policy

- Start from `main`.
- Use `feature/<topic>` for new skills and substantial improvements.
- Use `fix/<topic>` for corrections.
- Use `release/<version>` for release preparation.
- Merge back to `main` only after validation passes.

## Commit Order

1. Commit changes inside each affected skill repo.
2. Push each affected skill repo.
3. Update the AgentSkills submodule pointer.
4. Update AgentSkills README/AGENTS/docs for visible behavior changes.
5. Commit and push AgentSkills.

## Versioning

- Use semantic versioning when the repo maintains versions.
- Patch: wording, docs, examples, validation fixes.
- Minor: new modes, references, outputs, or compatible capabilities.
- Major: renamed skill, breaking trigger contract, removed modes, or incompatible
  output contracts.

## Release Gate

Do not push a final release when validation is broken unless the user explicitly
asks for a WIP push.
