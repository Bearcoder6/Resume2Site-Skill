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
- Use concrete strengths instead of generic traits.
- Avoid fake testimonials, fake numbers, and generic SaaS visuals.
- Keep mobile layout readable.

## Final Step

Run `prompts/final-review.md`, fix important issues, then write `work/final-review.md`.
