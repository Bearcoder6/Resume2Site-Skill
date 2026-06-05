# Refactor Summary

## What Changed

Resume2Site-Skill was rebuilt as a lightweight installable Agent Skill. The repository now centers on instructions, prompts, rules, examples, and quality checks for agents that generate GitHub Pages personal websites from resumes and supporting materials.

## What Was Removed

- Python package metadata and CLI-oriented entry points.
- Standalone parser, doctor, avatar, asset, and site generator implementation.
- CLI smoke tests.
- Old product-style templates and generated-output assumptions.
- Local generated folders and caches.

The previous state is preserved in the Git backup branch:

```text
backup/pre-pure-skill-refactor
```

## What Was Added

- Root `SKILL.md` and `skill.json`.
- Main installable Skill at `skills/resume2site/SKILL.md`.
- Workflow, mode, privacy, content, asset, style, layout, and quality rules.
- Practical prompt pack under `skills/resume2site/prompts/`.
- Academic and landing template reference notes.
- Fake academic and landing examples.
- Install, usage, implementation-process, and style-distillation documentation.

## Why It Is Now A Pure Skill

The project no longer asks users to install or run a custom CLI. It guides Codex, Claude Code, Cursor, or another coding agent to use its own file-reading, writing, web, and development abilities while following a structured workflow.

## How To Use It

Point the agent to:

```text
skills/resume2site/SKILL.md
```

Ask it to create:

```text
work/profile.json
work/site-plan.md
output/site/
```

The generated site should include `index.html`, `styles.css`, `assets/`, `.nojekyll`, `README.md`, and `ASSET_CREDITS.md` when assets are used.

## Remaining TODOs

- Add more community-reviewed example outputs.
- Add optional agent-specific installation notes as platforms stabilize.
- Expand style reference examples without copying proprietary designs.
- Add more specialized modes, such as lab homepage or designer portfolio.

## Suggested Next Steps

1. Review the new README and Skill wording.
2. Commit the refactor.
3. Push a branch and open a PR against `main`.
