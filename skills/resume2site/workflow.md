# Workflow

Follow this sequence for every Resume2Site task.

1. Confirm the user goal and available materials.
2. Read resume content using the agent environment's available capabilities.
3. If PDF or DOCX extraction is poor, ask the user for a text version.
4. Read optional GitHub, paper, website, avatar, and style reference inputs.
5. Create `work/profile.json` from source facts.
6. Decide `academic` or `landing` mode.
7. Create `work/site-plan.md`.
8. Recommend visual assets when useful.
9. Generate `output/site/` as a static GitHub Pages site.
10. Run final review, then make one polish pass before finishing.

Do not skip `work/profile.json`. It is the factual contract between the resume and the website.

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
