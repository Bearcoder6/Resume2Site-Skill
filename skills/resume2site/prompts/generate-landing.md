# Generate Personal Landing Page Prompt

Use this prompt for landing mode.

## Read

- `work/profile.json`.
- `work/site-plan.md`.
- `landing-layout-rules.md`.
- `content-rules.md`.
- `asset-rules.md`.
- `templates/personal-landing/`.

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
Hero
Personal Positioning
Core Strengths
Selected Projects / Works
Experience Highlights
Skills
Contact CTA
Resume Download
```

Omit empty sections.

## Design Requirements

- Make the first viewport polished and specific to the person.
- Use a strong but tasteful personal-brand visual direction.
- Turn projects into selected works or case studies.
- Preserve and render project, GitHub, demo, portfolio, and profile links from `profile.json`.
- Use compact link buttons or inline link rows. Use brand icons only when they are available from official brand assets or a reputable open icon set with compatible terms.
- Render brand icons as single-color `currentColor` or the page accent color so they fit the selected style. Do not use mismatched full-color logos in a restrained page.
- If a reliable icon is not available, use a text label instead of adding an unverified image.
- Use concrete strengths instead of generic traits.
- Avoid fake testimonials, fake numbers, and generic SaaS visuals.
- Optimize for PC / desktop by default.

## Final Step

Run the lightweight file-based `prompts/final-review.md`, fix important issues, write `work/final-review.md`, then give the user the local `output/site/index.html` path. Do not require screenshots or browser automation.
