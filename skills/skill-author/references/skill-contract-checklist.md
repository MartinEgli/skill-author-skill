# Skill Contract Checklist

Use this checklist before committing a skill change.

## Required Contract

- `SKILL.md` exists and frontmatter `name` matches the skill folder.
- `description` explains what the skill does and when to use it.
- Purpose is narrow enough to distinguish the skill from neighbors.
- Mandatory rules are actionable.
- Do-not-use cases prevent wrong triggering.
- Inputs expected are explicit.
- Modes are named and map to real workflows.
- Evidence handling matches actual outputs.
- Handoffs name adjacent skills and why they take over.
- Boundaries say what not to invent or decide.
- Output style is practical and not decorative.

## Resources

- Every linked reference exists.
- Every reference is directly discoverable from `SKILL.md`.
- Assets are templates or files the agent can reuse in outputs.
- Scripts are tested when added or changed.
- No placeholder examples remain.

## Metadata And Packaging

- `agents/openai.yaml` reflects the current skill.
- Package default points to the actual skill name.
- Validation, tests, and packaging pass.
- Dist artifacts are regenerated only when intended.
