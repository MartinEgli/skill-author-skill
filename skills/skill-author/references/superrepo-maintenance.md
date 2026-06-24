# Superrepo Maintenance

Use this reference when a skill change affects AgentSkills.

## Update AgentSkills When

- A new skill repo is added.
- A skill name, trigger, mode, role, output contract, handoff, evidence rule, or
  diagram capability changes.
- Installation guidance changes.
- A submodule pointer changes.

## README Updates

Update the catalog with:

- repo name
- Codex skill name
- use-for statement
- do-not-use statement
- example prompts when the skill is user-facing
- main modes
- output focus
- choosing guide entry
- install command when appropriate
- submodule list entry

## AGENTS Updates

Update AGENTS when contributor instructions change, especially:

- submodule inventory
- branch policy
- evidence and traceability policy
- README maintenance rules
- validation and push expectations

## Submodule Rule

Commit the skill repo first, then commit the superrepo pointer. The superrepo
must not point to an unpushed or unvalidated skill commit.
