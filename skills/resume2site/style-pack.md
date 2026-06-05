# Style Pack

Use this built-in style pack as the default visual judgment for Resume2Site. The user does not need to distill style manually. User screenshots or inspiration can be optional supplements, but the Skill should already know what academic and landing pages need to look like.

## Shared Principles

- Make the first screen immediately identify the person and their positioning.
- Use strong typography and spacing instead of decorative clutter.
- Use visual assets only when they support the person's story.
- Choose background visuals by profession, field, and audience; do not force a school/place image unless it improves the page.
- Avoid generic AI gradients, excessive glassmorphism, random icons, and stock-photo cliches.
- Keep sections dense enough to be useful but relaxed enough to feel designed.
- Optimize for desktop / PC viewing first, especially `1366px` to `1440px` wide screens.
- Add only a simple mobile fallback unless the user explicitly asks for mobile-first or fully responsive design.
- Build one coherent visual system: type, color, spacing, borders, images, and section rhythm must feel related.
- Add enough crafted details that the page feels designed: section labels, date rhythm, subtle rules, image treatment, hover states, and purposeful empty space.
- Keep type scale balanced. Hero headings should feel confident, not oversized; section headings should not visually compete with the person's name.
- Match the page language to the user's resume and request. Do not default to English-heavy labels when the user provided a Chinese resume.
- Pick one style variant below and apply it consistently. Do not mix visual languages across sections.
- On desktop, prevent overflow from long Chinese lines, URLs, and technology stacks. Let technical stacks wrap cleanly in cards.
- Treat public links as content, not decoration. GitHub, arXiv, DOI, Scholar, demo, project, dataset, and portfolio links should be visible where relevant.
- Use small single-color brand icons only when the source is official or a reputable open icon set and the license/terms allow use. Match icons to the page accent or text color.
- Do not introduce a heavy icon library only for a few links; inline SVG or text labels are enough for static pages.

## Style Variants

Use these as distilled, lightweight recipes. They are not fixed templates; adapt them to the resume content.

Every variant must cover the same five design decisions: `Visual language`, `Layout`, `Details`, `Links`, and `Avoid`.

### `academic-editorial`

For papers, labs, advisors, research interests, grants, and graduate or faculty-style pages.

- Visual language: near-white paper surface, fine borders, serif or scholarly display headings, restrained green/ink/navy accent.
- Layout: left profile/sidebar plus main research column, or top profile band plus publication sections.
- Details: publication cards, date rhythm, research tags, subtle paper grain or library/research imagery.
- Links: place Scholar, ORCID, GitHub, arXiv, DOI, paper, and lab links near the profile or publication entries.
- Avoid: startup CTA language, fake metrics, dark technical hero unless the user asks.

### `academic-lab`

For academic resumes with engineering, AI, data, robotics, systems, or applied research signals.

- Visual language: translucent panels, soft grids, low-contrast gradients, light lab/research atmosphere.
- Layout: profile panel plus research/project modules; allow wider horizontal composition than a resume.
- Details: method tags, datasets/tools, research-to-engineering bridge, optional abstract CSS diagrams.
- Links: place arXiv, DOI, GitHub, project page, dataset, demo, and lab links in compact research/project rows.
- Avoid: looking like a product SaaS page or a literal school brochure.

### `engineering-commercial`

For backend, frontend, AI engineer, data engineer, cloud, security, and job-seeking technical resumes.

- Visual language: dark or neutral technical background, one restrained accent, crisp cards, code/grid/infrastructure cues.
- Layout: split hero with portrait or project signal, proof strip, selected project case cards, skills grouped by system role.
- Details: stack chips, architecture highlights, performance facts only when present in the resume.
- Links: show GitHub, demo, project page, technical blog, and portfolio links as compact action rows with single-color icons or text labels.
- Avoid: generic startup landing copy, invented numbers, school/company background images that do not support the role.

### `business-polished`

For product, consulting, operations, finance, management, sales, and enterprise-facing resumes.

- Visual language: light premium surface, strong whitespace, sober accent color, precise typography.
- Layout: confident hero, capability bands, experience timeline, selected outcomes or work highlights.
- Details: role scope, industries, tools, collaboration strengths, clear contact path.
- Links: show website, LinkedIn, portfolio, case-study, press, report, or public work links as restrained text actions.
- Avoid: overly playful graphics, neon technical motifs, academic publication framing.

### `creative-portfolio`

For design, media, writing, marketing, creator, and client-facing portfolios.

- Visual language: editorial asymmetry, strong image treatment, expressive but controlled type, richer section rhythm.
- Layout: immersive first viewport, selected work gallery, case-study cards, process or services section.
- Details: thumbnails, project images, client/work categories, tasteful motion when the stack supports it.
- Links: show portfolio, live work, social/profile, video, press, writing, or client-safe project links close to the work item.
- Avoid: empty decoration, fake client logos, motion that hides content.

### `minimal-resume-site`

For conservative, fast, formal, or sparse resumes.

- Visual language: clean one-page site, quiet type hierarchy, limited color, strong readability.
- Layout: name/role hero, compact sections, timeline, skills, contact.
- Details: printable feel, high contrast, no oversized hero, no decorative background unless it adds clarity.
- Links: keep GitHub, Scholar, website, email, DOI, arXiv, demo, and portfolio links in a simple text row or compact contact section.
- Avoid: trying to make sparse content look big through empty cards or huge typography.

## Academic Direction

Use restrained editorial design:

- White or near-white background.
- Strong serif or scholarly heading typography when appropriate.
- Fine borders, small caps, section rhythm, and readable publication formatting.
- Subtle profile card or sidebar.
- Optional visual band with library, paper, lab, campus, or abstract research imagery.
- Prefer quiet confidence: credibility, clarity, and information design over personal-brand hype.
- Use publication lists, research interests, and education blocks as core visual material.
- Add subtle academic atmosphere through paper grain, soft grid, campus/library imagery, or careful typographic hierarchy.
- Academic atmosphere can come from translucent panels, gradients, paper texture, and low-contrast CSS patterns. A literal campus photo is optional, not required.
- For Chinese academic pages, prefer Chinese section labels with English only where it is factual or conventional, such as paper titles, venues, arXiv, GitHub, or technical terms.

## Landing Direction

Use a personal-brand design:

- Strong hero with clear positioning.
- Purposeful color palette derived from domain and audience.
- Concrete strengths and selected work cards.
- CTA that fits the user's goal: contact, GitHub, portfolio, resume, Scholar, or email.
- Expressive but not generic visual language.
- Use stronger composition than academic mode: hero split, editorial band, proof strip, project case-study grid, or layered background.
- Use role-appropriate backgrounds. Backend and engineering profiles can use technical grids, infrastructure-inspired abstraction, terminal/code rhythm, or product workspace imagery instead of literal school/company photos.
- Use project content as the main proof, not fake metrics.
- Make the page feel commercially polished without becoming a generic SaaS landing page.

## Optional User References

The built-in style pack comes first. When the user provides screenshots or inspiration, use them only to supplement:

- Layout rhythm.
- Typography mood.
- Color temperature.
- Visual density.
- Card, section, and navigation behavior.

Do not copy exact layouts, artwork, proprietary UI, or identifiable brand expression.
