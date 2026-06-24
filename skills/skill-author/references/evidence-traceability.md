# Evidence And Traceability

Use this reference whenever a skill is created or changed.

## Evidence Types

- User fact: explicit request, wording, file, repo name, path, or constraint from
  the user.
- Repo fact: existing `SKILL.md`, `AGENTS.md`, README, package script, test, or
  tool output.
- Source fact: cited external standard, documentation, or reference.
- Inference: conclusion derived from evidence.
- Assumption: useful but not verified.
- Gap: missing input that could change the result.

## Required Practice

- Preserve exact identifiers: paths, repos, commands, role names, modes, and
  source labels.
- Keep important recommendations traceable to at least one evidence type.
- Mark assumptions before they affect design.
- Mark gaps when missing input changes trigger behavior, scope, safety, or
  validation.
- Do not turn assumptions into source claims.
- Do not cite frameworks or standards unless the skill actually uses them.

## Evidence Receipt

For substantial outputs, include:

| Claim or Decision | Source | Type |
| --- | --- | --- |
| Skill name and repo name | User request or repo path | User fact / repo fact |
| Trigger behavior | `SKILL.md` frontmatter | Repo fact |
| Validation status | command output | Repo fact |
| Missing input | stated absence | Gap |
