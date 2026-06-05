# Content Rules

Extract facts first. Improve language only after `work/profile.json` exists.

## Do Not Invent

- Jobs.
- Awards.
- Publications.
- Metrics.
- Affiliations.
- Advisors.
- Testimonials.
- Credentials.
- Company impact claims.

Use empty strings or arrays for missing data.

## Numeric Evidence Placement

Numbers must stay attached to their original source context.

- Project-local or experience-local numbers belong only inside that project or experience entry. Examples: latency, response time, API count, test case count, retry count, throughput, cost reduction, bug count, user count, revenue, conversion, or benchmark results.
- Do not move project or experience numbers into the hero, profile card, sidebar, personal info area, or global highlight cards.
- Only use a number as a personal/global profile metric when the resume explicitly presents it as a person-level fact near identity, education, honors, publications, or contact information. Examples: GPA, major rank, graduation year, publication count, citation count, patent count, award count, or years of experience.
- If a number's scope is ambiguous, keep it in the detailed resume section where it appears, or omit it from decorative metric cards.
- Global metric cards are optional. A clean no-metric layout is better than a misleading metric layout.

## Rewrite Style

Convert resume bullets into website-friendly writing:

- Match the primary language of the user's resume and request by default.
- If the resume is Chinese and the user did not request English, use Chinese-first section labels and body copy. Keep English only for paper titles, venue names, technical terms, official program names, and links.
- Avoid making the page feel like an English template filled with translated Chinese facts.
- Make academic content credible, concise, and source-grounded.
- Make landing-page content clear, specific, and personal-brand oriented.
- Remove weak generic phrases such as "passionate developer", "hard-working student", "detail-oriented individual", and "enthusiastic learner".
- Prefer concrete descriptions: problem solved, user role, method used, result achieved, research contribution, project outcome.
- Public page copy must read like a normal personal website. Do not mention that the page was generated from a resume, DOCX, PDF, Markdown, this Skill, an agent workflow, extraction rules, privacy rules, metric-placement rules, or final-review checks.
- Global positioning should synthesize the person's role, field, audience, and repeated evidence. Do not make one tool/project, source file, or showcase goal sound like the person's entire identity unless the resume explicitly frames it that way.
- Avoid internal QA/demo wording in public copy, such as "test material", "automatic test", "for testing", "sample output", or "generated example", unless it is clearly part of a public project title or the user asks to show it.
- Avoid unsupported personality or preference claims such as "focuses on", "cares about", "is passionate about", or "tries to" unless the resume or user explicitly says so. Prefer factual synthesis: project types, responsibilities, methods, stack, and outcomes.

## Project Entries

Turn project entries into mini case studies:

```text
Problem
Role
Contribution
Method / Stack
Outcome
Links
```

If a field is missing, omit it rather than inventing it.

## Link Preservation

- Do not drop public work links found in the resume or supporting files.
- Preserve GitHub, arXiv, DOI, Google Scholar, personal website, project demo, portfolio, dataset, video, and paper/project page links.
- Render links near the content they belong to: paper links near papers, repository/demo links near projects, profile links near the hero or contact area.
- Keep link labels concise and factual, such as `GitHub`, `arXiv`, `DOI`, `Scholar`, `Demo`, `Website`, `Dataset`, or the project/paper title.
- If a link is private, broken, or clearly unrelated, do not publish it. Record the decision in `work/final-review.md`.

## Publication Entries

Use:

```text
Title
Authors
Venue / Year
Contribution summary
Links
```

If the user's contribution is unclear, say what the paper is about without claiming a contribution.
