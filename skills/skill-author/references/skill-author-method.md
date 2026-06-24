# Skill Author Method

Use this method when planning, creating, or refining a skill.

## Workflow

1. Locate the target repo and read `AGENTS.md`, `README.md`, `SKILL.md`, package
   scripts, and directly linked references.
2. Identify the user-visible purpose: what should trigger the skill, and what
   should not.
3. Define the smallest useful skill contract: purpose, mandatory rules, modes,
   inputs, evidence, handoffs, output contracts, quality gates, and boundaries.
4. Move detailed repeatable method into direct reference files.
5. Add assets only when they are copied or reused in outputs.
6. Update `agents/openai.yaml` so the UI metadata matches the skill contract.
7. Run validation, tests, package build, and a focused diff review.
8. Commit the skill repo first, then update AgentSkills documentation and
   submodule pointer.

## Design Rules

- Put trigger behavior in the YAML `description`.
- Keep `SKILL.md` below roughly 500 lines.
- Prefer direct references over nested reference chains.
- Avoid large framework summaries unless the skill needs them to act.
- Prefer clear do-not-use boundaries over vague "expert" positioning.
- Treat diagrams as output capability scoped to the role, not as a separate
  reason to bypass the skill boundary.
