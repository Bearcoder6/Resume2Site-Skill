# Generate Personal Landing Page Prompt

Use this prompt for landing mode.

## Read

- `work/profile.json`.
- `work/site-plan.md`.
- `landing-layout-rules.md`.
- `content-rules.md`.
- `asset-rules.md`.
- `profile-schema.md`.
- `information-architecture.md`.
- `design-token-rules.md`.
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
- Include `<meta charset="utf-8">` and write generated files as UTF-8.
- Do not show the selected style variant name in visible page text, page title, navigation, hero, headings, or footer. The variant name belongs in `work/site-plan.md` only.
- Use a strong but tasteful personal-brand visual direction.
- Use explicit design tokens for color, typography, spacing, radius, max width, and shadow intensity.
- Turn projects into selected works or case studies.
- Preserve and render project, GitHub, demo, portfolio, and profile links from `profile.json`.
- If `person.avatar` is set, render the portrait in a clean profile or hero slot without cropping off the head. If no avatar is available, use a polished no-photo layout instead of a broken image.
- Use compact link buttons or inline link rows. Use brand icons only when they are available from official brand assets or a reputable open icon set with compatible terms.
- Render brand icons as single-color `currentColor` or the page accent color so they fit the selected style. Do not use mismatched full-color logos in a restrained page.
- If a reliable icon is not available, use a text label instead of adding an unverified image.
- Keep numeric evidence in its source section. Do not place project-local or experience-local numbers in hero stats, profile cards, sidebar cards, personal info, or global highlight strips.
- Only create hero/profile metric cards from explicit person-level facts such as GPA, major rank, publication count, citation count, award count, or years of experience. If there are not enough clear person-level facts, use a text-led layout without metric cards.
- Use concrete strengths instead of generic traits.
- Do not expose generation-process notes in public copy. Never say the page was generated from a resume/DOCX/PDF, that data was omitted by privacy rules, or that metrics were kept in source sections.
- Keep hero and positioning copy person-centered. Do not make the generator, demo context, source resume, or one incidental project the main public narrative.
- Keep positioning source-grounded. Avoid unsupported claims about the person's motivation, preference, or mindset; summarize role, domain, responsibilities, stack, and outcomes instead.
- Avoid fake testimonials, fake numbers, and generic SaaS visuals.
- Optimize for PC / desktop by default.
- Run `bad-smell-checklist.md` before finalizing.

## Final Step

Run the lightweight file-based `prompts/final-review.md`, fix important issues, write `work/final-review.md`, then give the user the local `output/site/index.html` path. Do not require screenshots or browser automation.
