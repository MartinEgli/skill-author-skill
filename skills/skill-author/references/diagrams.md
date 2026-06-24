# Diagram Capability Authoring

Use this reference when `skill-author` creates or refines another skill's
diagram capability.

## Rule

`skill-author` does not create domain diagrams as its own output. It defines or
reviews the diagram contract of the target skill.

## Required Diagram Contract

When a target skill supports diagrams, define:

- diagram purpose
- supported notation such as Mermaid, PlantUML, C4, or UML-style views
- role or skill scope
- inputs needed
- evidence and traceability expectations
- handoffs when the diagram belongs to another skill
- limitations and do-not-use cases

## Quality Gate

Before claiming diagram support:

- `SKILL.md` names the diagram mode
- `SKILL.md` links to the target skill's `references/diagrams.md`
- diagram scope stays inside the target skill role
- diagram elements trace back to evidence or marked assumptions
- security, enterprise, software, solution, DDD, Azure, or governance diagrams
  are handed to the owning skill when outside the target scope
