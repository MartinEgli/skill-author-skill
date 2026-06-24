# Forward Testing

Use this reference when a skill needs realistic validation beyond static checks.

## Prompt Shape

Ask a fresh agent to use the skill the way a user would:

```text
Use skill-author at <path> to create or refine <target skill request>.
```

Do not include the intended answer, hidden diagnosis, or desired patch unless the
test specifically requires it.

## What To Observe

- Did the skill trigger for the right reason?
- Did the agent load only relevant references?
- Did it preserve evidence and gaps?
- Did it avoid domain work outside the skill boundary?
- Did it update README/AGENTS/submodule instructions when needed?
- Did validation guidance produce repeatable commands?

## When To Skip

Skip forward testing when it would require live production changes, credentials,
or long-running work the user has not approved.
