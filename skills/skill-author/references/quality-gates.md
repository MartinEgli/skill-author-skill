# Quality Gates

Use this reference for `/skill-author validate`.

## Static Checks

- Frontmatter exists and has only expected fields.
- Skill folder name matches frontmatter name.
- Trigger description is concrete.
- Required sections exist.
- Links resolve.
- No placeholder markers remain.
- No stale example names remain.

## Behavioral Checks

- A normal user prompt would trigger the skill.
- A neighboring domain prompt would not trigger the skill.
- Modes cover expected work without duplicating each other.
- Handoffs are explicit.
- Evidence rules match the skill's outputs.
- Output contracts are usable without extra explanation.

## Repo Checks

- `npm run validate` passes when available.
- `npm run test` passes when available.
- `npm run package` passes when available.
- `git diff` contains only intended changes.
- Generated package artifacts are included only when the repo expects them.
