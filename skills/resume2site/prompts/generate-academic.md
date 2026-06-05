# Generate Academic Homepage Prompt

Use this prompt for academic mode.

## Read

- `work/profile.json`.
- `work/site-plan.md`.
- `academic-layout-rules.md`.
- `content-rules.md`.
- `asset-rules.md`.
- `profile-schema.md`.
- `information-architecture.md`.
- `design-token-rules.md`.
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
- Include `<meta charset="utf-8">` and write generated files as UTF-8.
- Do not show the selected style variant name in visible page text, page title, navigation, hero, headings, or footer. The variant name belongs in `work/site-plan.md` only.
- Use strong readable typography and restrained spacing.
- Use explicit design tokens for color, typography, spacing, radius, max width, and shadow intensity.
- Format publications clearly.
- Preserve and render arXiv, DOI, Google Scholar, GitHub, project page, dataset, and personal website links from `profile.json`.
- Place paper links directly in publication entries and profile links in the sidebar, header, or contact area.
- If `person.avatar` is set, render the portrait in a clean profile slot without cropping off the head. If no avatar is available, use a polished no-photo layout instead of a broken image.
- Use compact text links or single-color icons that match the page accent. Use brand icons only when they are available from official brand assets or a reputable open icon set with compatible terms.
- If a reliable icon is not available, use a text label such as `arXiv`, `DOI`, `Scholar`, or `GitHub`.
- Keep numeric evidence in its source section. Do not place project-local or experience-local numbers in profile cards, sidebar cards, personal info, hero stats, or global highlight strips.
- Only create profile/sidebar metric cards from explicit person-level academic facts such as GPA, major rank, publication count, citation count, patent count, award count, or years of experience. If these facts are missing or sparse, use a clean profile layout without metric cards.
- Use subtle visual assets or CSS patterns.
- Keep the profile card clean and factual.
- Do not expose generation-process notes in public copy. Never say the page was generated from a resume/DOCX/PDF, that data was omitted by privacy rules, or that metrics were kept in source sections.
- Keep profile and about copy person-centered. Do not make the generator, demo context, source resume, or one incidental project the main public narrative.
- Keep profile/about copy source-grounded. Avoid unsupported claims about the person's motivation, preference, or mindset; summarize research area, projects, methods, links, and verified outcomes instead.
- Avoid fake metrics, commercial exaggeration, and generic AI gradients.
- Run `bad-smell-checklist.md` before finalizing.

## Final Step

Run the lightweight file-based `prompts/final-review.md`, fix important issues, write `work/final-review.md`, then give the user the local `output/site/index.html` path. Do not require screenshots or browser automation.
