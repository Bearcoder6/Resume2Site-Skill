# Workflow

Follow this sequence for every Resume2Site task.

1. Confirm the user goal and available materials.
2. Read resume content using the agent environment's available capabilities.
3. If PDF or DOCX extraction is poor, ask the user for a text version.
4. Read optional GitHub, paper, website, avatar, and user style preference inputs.
5. Create `work/profile.json` from source facts.
6. If a portrait is present or likely present in the resume, follow `avatar-rules.md` and save the public avatar into `output/site/assets/`.
7. Decide `academic` or `landing` mode.
8. If the user did not already choose a style variant and requirements, ask the Style Intake question from `SKILL.md`.
9. Create `work/site-plan.md` with the selected style variant, content center, information architecture, and design tokens.
10. Apply the built-in style variant from `style-pack.md` and `design-token-rules.md`.
11. Search for free/open/licensed visual assets when useful and record candidates.
12. Generate `output/site/` as a static GitHub Pages site.
13. Run a lightweight file-based final review, then make one polish pass before finishing.
14. Report the generated `output/site/index.html` path to the user.

Do not skip `work/profile.json`. It is the factual contract between the resume and the website.
Do not mix profile schema scopes. Project and experience metrics stay local unless the resume explicitly presents them as person-level facts.
Do not skip style intake for new users. It is the usability checkpoint between factual extraction and design generation.
Do not silently drop resume portraits. If extraction fails, record the attempted fallback in `work/final-review.md`.
Do not require browser automation, screenshots, Playwright, a local dev server, or any visual testing environment. Those checks are optional only when the user explicitly asks or the environment already supports them without setup.
Do not display the selected style variant name in the public page. It belongs in `work/site-plan.md`, not in user-facing page copy.
Write generated HTML, JSON, Markdown, and CSS files as UTF-8. Include `<meta charset="utf-8">` in every generated HTML file.

## Recommended Site Files

```text
output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```

## Working Files

```text
work/profile.json
work/site-plan.md
work/asset-recommendations.md
work/final-review.md
```

Working files are internal and should not be published unless the user asks.
