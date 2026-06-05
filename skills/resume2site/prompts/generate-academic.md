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
- Preserve and render arXiv, DOI, Google Scholar, GitHub, project page, dataset, and personal website links from `profile.json`.
- Place paper links directly in publication entries and profile links in the sidebar, header, or contact area.
- If `person.avatar` is set, render the portrait in a clean profile slot without cropping off the head. If no avatar is available, use a polished no-photo layout instead of a broken image.
- Use compact text links or single-color icons that match the page accent. Use brand icons only when they are available from official brand assets or a reputable open icon set with compatible terms.
- If a reliable icon is not available, use a text label such as `arXiv`, `DOI`, `Scholar`, or `GitHub`.
- Use subtle visual assets or CSS patterns.
- Keep the profile card clean and factual.
- Avoid fake metrics, commercial exaggeration, and generic AI gradients.

## Final Step

Run the lightweight file-based `prompts/final-review.md`, fix important issues, write `work/final-review.md`, then give the user the local `output/site/index.html` path. Do not require screenshots or browser automation.
