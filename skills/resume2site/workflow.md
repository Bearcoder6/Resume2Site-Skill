# Workflow

Follow this sequence for every Resume2Site task.

1. Confirm the user goal and available materials.
2. Read resume content using the agent environment's available capabilities.
3. If PDF or DOCX extraction is poor, ask the user for a text version.
4. Read optional GitHub, paper, website, avatar, and user style preference inputs.
5. Create `work/profile.json` from source facts.
6. Decide `academic` or `landing` mode.
7. If the user did not already choose a style variant and requirements, ask the Style Intake question from `SKILL.md`.
8. Create `work/site-plan.md` with the selected style variant.
9. Apply the built-in style variant from `style-pack.md`.
10. Search for free/open/licensed visual assets when useful and record candidates.
11. Generate `output/site/` as a static GitHub Pages site.
12. Run final review, then make one polish pass before finishing.

Do not skip `work/profile.json`. It is the factual contract between the resume and the website.
Do not skip style intake for new users. It is the usability checkpoint between factual extraction and design generation.

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
