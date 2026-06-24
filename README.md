# Skill Author Skill

Agent skill for building and maintaining production-ready skills in the
MartinEgli/AgentSkills ecosystem across Codex and other agent hosts.

## Skill

- Skill: `skill-author`
- Primary file: `skills/skill-author/SKILL.md`
- Use for: new skill repos, skill refinements, evidence rules, validation,
  Gitflow, releases, AgentSkills README/AGENTS updates, submodule maintenance,
  and target-agent compatibility.

## Validate

```powershell
npm run validate
npm run test
npm run package
```

## Install

Codex:

```powershell
npx -y skills add MartinEgli/skill-author-skill --skill * -a codex --yes
```

Other agents:

Use `skill-author /skill-author agents` to define the target agent, metadata,
install/import path, and validation evidence before claiming support.
