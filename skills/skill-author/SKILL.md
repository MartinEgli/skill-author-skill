---
name: skill-author
description: >
  Build, refine, validate, release, and document production-ready Codex skills
  in the MartinEgli/AgentSkills ecosystem. Use when creating a new skill repo
  from single-skill-template, updating an existing skill contract, adding modes,
  roles, references, evidence and traceability rules, diagram capability,
  agents/openai.yaml metadata, validation, packaging, Gitflow branches,
  submodules, README catalog entries, or installation guidance.
---

# Skill Author

## Purpose

Create and maintain focused Codex skills that are installable, traceable,
validated, and correctly represented in the AgentSkills superrepo.

## When to Use

Use this skill when the user asks to:

- create a new Codex skill or skill repository
- refine an existing `SKILL.md`, mode, role, trigger, or boundary
- add evidence, traceability, handoff, diagram, or output-contract rules
- update `agents/openai.yaml`
- validate, package, version, commit, push, or release a skill
- add a skill to AgentSkills as a submodule
- update AgentSkills README, AGENTS, install examples, or skill catalog entries
- define a repeatable recipe for building future skills

## Mandatory Rules

- Work on `feature/<topic>`, `fix/<topic>`, or `release/<version>` branches.
- Read the target repo `AGENTS.md` before editing when present.
- Use `single-skill-template` as the default base for new single-skill repos.
- Keep `SKILL.md` concise and move detailed method into direct reference files.
- Preserve exact user facts, paths, repo names, role names, commands, and source
  labels.
- Separate evidence, inference, assumption, and gap.
- Add or update `references/evidence-traceability.md` whenever the skill uses or
  produces claims, findings, decisions, diagrams, risks, roles, modes, or
  handoffs.
- Update `agents/openai.yaml` when the skill name, trigger description, default
  prompt, role, or scope changes.
- Update the AgentSkills README and AGENTS instructions when a skill, role, mode,
  output contract, handoff, evidence rule, diagram scope, or install command
  changes.
- Run available validation, tests, and packaging before committing.
- Commit granularly in the affected skill repo first, then update and commit the
  superrepo submodule pointer and documentation.
- Push skill repos and the superrepo after green validation unless the user asks
  for a local-only change.

## Do Not Use When

- The user needs normal architecture, software, Azure, .NET, DDD, or security
  work. Hand off to the domain skill.
- The user needs final architecture governance acceptance. Hand off to
  `mournival-architecture`.
- The user asks only for a simple answer and no skill artifact changes are
  needed.
- Required source material is missing and the result would invent domain
  knowledge. Mark the gap.

## Inputs Expected

Useful inputs include:

- target skill name and repo name
- intended user prompts and non-trigger examples
- scope boundaries and do-not-use cases
- roles or modes to support
- source material, standards, templates, or local examples
- expected outputs and quality gates
- installation target, superrepo path, and release/version expectations

Proceed with reasonable assumptions when the repo structure and user intent are
clear. Mark assumptions in the output and Evidence Receipt.

## Modes

### /skill-author plan

Define skill scope, trigger description, boundaries, expected inputs, output
contracts, references, assets, tests, and superrepo changes. Read
`references/skill-author-method.md` and
`references/skill-contract-checklist.md`.

### /skill-author create

Create a new skill repo from `single-skill-template`, replace placeholder
content, add references/assets that are actually needed, validate, package, push,
and add it to AgentSkills as a submodule. Read
`references/superrepo-maintenance.md` and `references/gitflow-release.md`.

### /skill-author refine

Update an existing skill contract, modes, roles, handoffs, evidence handling,
diagram scope, references, examples, and metadata. Keep the change scoped and
traceable.

### /skill-author evidence

Add or repair evidence and traceability behavior. Read
`references/evidence-traceability.md`.

### /skill-author handoffs

Clarify overlaps between skills and define when to continue, hand off, or use
multiple skills in sequence.

### /skill-author catalog

Update the AgentSkills README, AGENTS instructions, install examples, submodule
list, comparison tables, and use-case documentation after skill changes.

### /skill-author validate

Run skill validation, tests, packaging, README checks, and diff inspection. Read
`references/quality-gates.md`.

### /skill-author release

Prepare versioned release changes, changelog entries when the repo uses them,
tags, pushes, and superrepo pointer updates. Read
`references/gitflow-release.md`.

### /skill-author forward-test

Design realistic validation prompts for the skill without leaking intended
answers. Read `references/forward-testing.md`.

## Evidence Handling

Use `references/evidence-traceability.md` for every substantial skill change.

Always classify important inputs as:

- Evidence: user-provided material, existing repo files, tool output, or cited
  external source.
- Inference: a conclusion drawn from evidence.
- Assumption: useful but not verified.
- Gap: missing input that may change the result.

Include an Evidence Receipt in substantial final outputs and release summaries.

## Output Contracts

Use `assets/skill-author-output-template.md` for structured skill authoring
summaries when the user asks for a plan, audit, or release report.

Generated or updated skills should include:

- precise YAML `name` and `description`
- concise purpose and mandatory rules
- explicit do-not-use boundaries
- modes and expected inputs when useful
- evidence handling and handoffs
- output contracts and quality gates
- direct reference links only where needed
- `agents/openai.yaml` aligned with `SKILL.md`
- validation/test/package commands that pass

## Quality Gates

Before final answer or commit:

- no placeholder markers remain
- skill name matches folder name and package default
- trigger description covers use and non-use boundaries
- references linked from `SKILL.md` exist
- evidence rules match actual skill outputs
- openai metadata matches the current skill contract
- diagrams are scoped to the skill role when diagram capability exists
- README/catalog/submodule docs are updated when needed
- validation, tests, and packaging pass or failures are reported
- commits are granular and on the expected branch

## Handoffs

- Use `single-skill-template` as the base artifact for a new skill repository.
- Use the target domain skill for domain content that belongs inside a skill.
- Use `mournival-architecture` when architecture artifacts need independent
  evidence acceptance or governance review.
- Use GitHub tooling when PRs, remote repos, releases, or review threads are
  explicitly part of the task.

## Boundaries

Do not add broad domain knowledge just to make a skill look complete. A skill is
good when it has clear triggering, bounded scope, useful references, testable
behavior, and traceable outputs.

## Output Style

- Lead with changed artifacts, validation status, and any blockers.
- Use short tables for audits, handoffs, and catalog comparisons.
- Include exact commands only when they are useful for repeatability.
- Keep final user updates concise and include the Evidence Receipt for
  substantial changes.
