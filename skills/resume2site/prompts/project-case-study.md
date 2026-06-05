# Project Case Study Prompt

Use this prompt when converting project bullets into website sections.

## Read

- Project entries in `work/profile.json`.
- Any linked GitHub repositories or project pages that the agent can access.
- User-provided project summaries.

## Output

For each selected project, write:

```text
Project name
One-line summary
Problem
Role
Contribution
Method / Stack
Outcome
Links
```

## Rules

- Do not invent metrics, users, revenue, or production status.
- If the outcome is not stated, describe the implemented result rather than claiming impact.
- Prefer 2-4 selected projects over listing everything.
- Make technical projects understandable to non-specialist readers.
- Preserve important stack details when relevant.
