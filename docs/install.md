# Install

Resume2Site-Skill is lightweight. There is no CLI, package runtime, or build command to install.

Depending on your agent environment, install the Skill by copying the `skills/resume2site` folder into your skill directory, or by giving the agent access to this repository and asking it to use `skills/resume2site/SKILL.md`.

## Codex-Style Local Install

macOS/Linux:

```bash
mkdir -p ~/.codex/skills
cp -R skills/resume2site ~/.codex/skills/resume2site
```

Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force ".\skills\resume2site" "$env:USERPROFILE\.codex\skills\resume2site"
```

Then start a new agent thread and ask it to use Resume2Site.

## Repository Reference Install

If your agent can read repository files directly, keep this repository available and prompt:

```text
Use the Resume2Site Skill at skills/resume2site/SKILL.md.
```

## Prompt-Only Fallback

If your environment does not support installable skills, paste the contents of `skills/resume2site/SKILL.md` into the session and point the agent to the supporting Markdown files as needed.

## Notes

- Do not run `pip install`.
- Do not expect a `resume2site build` command.
- Let the coding agent use its own PDF, DOCX, browser, filesystem, and development capabilities.
