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
