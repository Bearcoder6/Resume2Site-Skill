# Plan Site Prompt

Use this prompt after `work/profile.json` exists.

## Read

- `work/profile.json`.
- `mode-rules.md`.
- `profile-schema.md`.
- `information-architecture.md`.
- `academic-layout-rules.md` or `landing-layout-rules.md`.
- `content-rules.md`.
- `design-token-rules.md`.
- User style preferences and visual references when provided.

## Output

Create `work/site-plan.md` with:

```text
# Site Plan

Mode:
Style variant:
Audience:
Primary goal:
Content center:
Assumptions:

First viewport:
Section order:
Content rewrite plan:
Visual direction:
Design tokens:
Asset needs:
Privacy decisions:
Open questions:
```

## Rules

- Choose academic or landing mode from evidence.
- Choose a style variant from `style-pack.md`.
- Choose a content center from `information-architecture.md` and let it control section priority.
- Omit sections that have no real content.
- State any assumption that affects the final website.
- Do not invent missing facts to make the site fuller.
- Base global positioning on repeated evidence, not on a single incidental project or the fact that a website is being generated.
- Identify which contact details should be public.
- Decide whether visual assets are needed.
- Plan hero/profile/sidebar numbers only from explicit person-level facts. Do not use project-local or experience-local numbers as personal metrics.
- If useful numbers exist only inside projects or experience, keep them in those detailed sections and use a no-metric hero/profile design.
- Plan typography, max width, radius, shadows, and color tokens before writing HTML/CSS.
