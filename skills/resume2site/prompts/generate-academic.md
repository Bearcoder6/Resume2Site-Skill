# Generate Academic Homepage Prompt

Use this prompt for academic mode.

## Read

- `work/profile.json`.
- `work/site-plan.md`.
- `academic-layout-rules.md`.
- `content-rules.md`.
- `asset-rules.md`.
- `templates/academic-profile/`.

## Create

```text
output/site/index.html
output/site/styles.css
output/site/assets/
output/site/README.md
output/site/.nojekyll
output/site/ASSET_CREDITS.md
```

## Structure

Use:

```text
Profile card / sidebar
About Me
News
Research Interests
Education
Selected Publications
Selected Projects
Honors & Awards
Experience
Contact
```

Omit empty sections.

## Design Requirements

- Make it look like a real academic homepage, not a resume dump.
- Use strong readable typography and restrained spacing.
- Format publications clearly.
- Use subtle visual assets or CSS patterns.
- Keep the profile card clean and factual.
- Avoid fake metrics, commercial exaggeration, and generic AI gradients.

## Final Step

Run `prompts/final-review.md`, fix important issues, then write `work/final-review.md`.
