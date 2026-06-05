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

## Rewrite Style

Convert resume bullets into website-friendly writing:

- Match the primary language of the user's resume and request by default.
- If the resume is Chinese and the user did not request English, use Chinese-first section labels and body copy. Keep English only for paper titles, venue names, technical terms, official program names, and links.
- Avoid making the page feel like an English template filled with translated Chinese facts.
- Make academic content credible, concise, and source-grounded.
- Make landing-page content clear, specific, and personal-brand oriented.
- Remove weak generic phrases such as "passionate developer", "hard-working student", "detail-oriented individual", and "enthusiastic learner".
- Prefer concrete descriptions: problem solved, user role, method used, result achieved, research contribution, project outcome.

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
