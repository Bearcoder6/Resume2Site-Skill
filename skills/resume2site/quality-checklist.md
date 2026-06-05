# Quality Checklist

Use this checklist before finishing. Create `work/final-review.md` with pass/fail notes and fix important failures.

This is a lightweight file-based checklist. Do not require browser automation, screenshots, Playwright, local dev servers, or visual regression tools. If those tools are unavailable, still finish normally after checking generated files and content.

## Shared Checks

- No hallucinated experience.
- No fake awards.
- No fake papers.
- No fake metrics.
- No project-local or experience-local numbers appear in hero stats, profile cards, sidebars, personal info, or global highlight cards.
- No empty visible sections.
- No raw resume hidden in HTML.
- No public page copy mentions generation process, source file type, extraction workflow, privacy-rule decisions, or final-review/internal Skill notes.
- Hero, about, and positioning sections describe the person, not the generator, demo process, source resume, or one incidental project.
- Public page copy avoids internal QA/demo wording unless it belongs to an explicit public project title.
- Public page copy avoids unsupported personality, motivation, or preference claims.
- No private files in `output/site/`.
- No public phone number unless approved.
- Resume portrait/avatar is preserved when present and extraction is reliable, or the failed extraction attempts are noted in `work/final-review.md`.
- Public HTML includes `<meta charset="utf-8">` and generated text files are written as UTF-8.
- Public page copy does not expose internal style variant names such as `academic-editorial`, `academic-lab`, `engineering-commercial`, `business-polished`, `creative-portfolio`, or `minimal-resume-site`.
- All links are structurally valid.
- Public GitHub, arXiv, DOI, Scholar, website, demo, portfolio, dataset, video, and project/paper links from the resume are preserved unless intentionally omitted with a note.
- Link icons, when used, are sourced from official or reputable open icon assets, use accessible labels, and match the page color system.
- Desktop layout is polished at `1366px` to `1440px` wide.
- Desktop layout is designed for `1366px` to `1440px` wide screens based on CSS/static review; screenshot verification is optional, not required.
- `index.html`, `styles.css`, `.nojekyll`, and `README.md` exist.
- `ASSET_CREDITS.md` exists if assets are used.
- Design does not look like a raw resume.
- Bad smells from `bad-smell-checklist.md` have been reviewed and fixed when present.
- Language is polished but factual.
- Page language matches the user's resume/request; English is not overused unless requested.
- Typography scale is balanced across hero, section headings, cards, and desktop content areas.
- Page has a first-viewport identity signal: name, role, and mode-appropriate positioning.
- Large background images meet the resolution threshold or are replaced by CSS-only visuals.
- A concrete style variant is named in `work/site-plan.md` and the page follows it consistently.
- Desktop layouts avoid horizontal overflow from nav, long Chinese text, URLs, or technology stacks.

## Academic Checks

- Looks like a real academic homepage.
- Publications are readable.
- Research interests are clear.
- Profile card or sidebar is clean.
- No commercial exaggeration.
- Education and honors are formatted cleanly.
- Academic hierarchy is easy to scan.

## Landing Checks

- Hero section has strong positioning.
- CTA buttons are clear.
- Selected works or projects are highlighted.
- Strengths are concrete.
- Visual style is polished.
- No generic SaaS template feel.
- Project cards read like small case studies, not pasted resume bullets.
