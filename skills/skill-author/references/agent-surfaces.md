# Agent Surfaces

Use this reference when a skill should support Codex, Claude, Cursor,
Windsurf, Cline, or another agent host.

## Default Rule

Codex is the default target only when the user does not name another agent.
When the user names an agent, preserve the exact agent name and make support
explicit in the skill repo and Superrepo documentation.

## Compatibility Model

For each target agent, record:

- target agent name
- supported skill file or instruction format
- metadata files used by that agent
- install command or copy path
- known limitations
- validation command or manual check
- evidence source for the support claim

## Repository Expectations

AgentSkills repos may contain one canonical skill contract plus target-agent
metadata. Keep the core skill instructions portable:

- avoid Codex-only wording unless Codex behavior is required
- keep target-specific install instructions in README or references
- keep target-specific metadata in clearly named files
- do not duplicate domain method across agent-specific files
- preserve evidence and traceability rules across all supported agents

## Current Metadata Pattern

Codex currently uses:

- `SKILL.md`
- `agents/openai.yaml`
- install commands such as `npx -y skills add <repo> --skill * -a codex --yes`

Other agents may require different file names, project instructions, or import
steps. If the exact target-agent format is not present in the repo, mark support
as planned or compatibility-oriented instead of claiming full installation
support.

## Install Guidance Pattern

README install sections should separate commands by target agent:

```text
Codex:
<command>

Claude:
<command or manual import path>

Cursor/Windsurf/Cline:
<command, import path, or compatibility note>
```

If a target has no verified command, write the current verified status and the
gap instead of inventing one.

## Quality Gate

Before claiming multi-agent support:

- the target agent is named
- install or import path is documented
- metadata files are present or the gap is explicit
- target-specific assumptions are visible
- validation or manual verification is recorded
- Superrepo README reflects the supported agent scope
