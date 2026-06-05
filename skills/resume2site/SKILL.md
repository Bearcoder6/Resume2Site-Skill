---
name: resume2site
description: Lightweight Agent Skill for turning resumes, GitHub projects, papers, and optional style references into polished GitHub Pages personal websites. Use when Codex, Claude Code, Cursor, or another coding agent needs to extract a structured profile, choose academic homepage or personal landing-page mode, plan site narrative, generate static HTML/CSS output, recommend licensed assets, protect privacy, and run a final quality review.
---

# Resume2Site

Use this Skill to guide a coding agent from resume materials to a polished GitHub Pages-ready personal website.

This Skill is not a CLI, parser, crawler, SaaS app, Python package, npm package, or full automation system. Use the agent environment's available file-reading, writing, browser, and development tools.

## Required Workflow

1. Read the user's resume and optional materials from the provided paths.
2. If PDF or DOCX extraction is unreliable, ask for `resume.txt`.
3. Do not directly generate a website from the raw resume.
4. Create `work/profile.json` first using `prompts/extract-profile.md`.
5. Choose academic or landing mode using `mode-rules.md`.
6. Create `work/site-plan.md` using `prompts/plan-site.md`.
7. Apply privacy rules before deciding what becomes public.
8. Generate `output/site/index.html`, `output/site/styles.css`, `output/site/README.md`, `output/site/.nojekyll`, and assets as needed.
9. If assets are recommended or used, create `work/asset-recommendations.md` and `output/site/ASSET_CREDITS.md`.
10. Run the final quality checklist and improve the page once before finishing.

## Inputs

Suggested, not required:

```text
input/
  resume.pdf or resume.docx or resume.txt
  avatar.png
  github_links.txt
  paper_links.txt
  website_links.txt
  style_preference.txt
  references/
```

Create folders as needed. Do not require the user to prepare this structure if they already gave concrete file paths.

## Outputs

```text
work/
  profile.json
  site-plan.md
  asset-recommendations.md
  final-review.md

output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```

Never copy raw resumes, private notes, hidden mappings, or internal extraction logs into `output/site/`.

## Mode Selection

- Academic Homepage: read `academic-layout-rules.md` and `prompts/generate-academic.md`.
- Personal Landing Page: read `landing-layout-rules.md` and `prompts/generate-landing.md`.
- If uncertain, read `mode-rules.md`. Ask the user when evidence is balanced.

## Core References

- `workflow.md`: complete sequence.
- `privacy-rules.md`: public/private data handling.
- `content-rules.md`: factual language and rewriting.
- `asset-rules.md`: licensed asset recommendations and credits.
- `style-pack.md`: style choices and polish guidance.
- `quality-checklist.md`: final review criteria.

## Non-Negotiables

- Extract facts before rewriting them.
- Do not invent missing experience, publications, metrics, awards, affiliations, advisors, testimonials, or credentials.
- Use empty strings or arrays for missing profile fields.
- Keep user-provided facts traceable to sources when possible.
- Ask before publicly including phone numbers or sensitive personal details.
- Do not hide raw resume text in HTML comments.
- Make the page look like a personal website, not a raw resume.
