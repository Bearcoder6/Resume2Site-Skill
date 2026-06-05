# Profile Schema Contract

`work/profile.json` is the factual contract between the resume and the generated website. Keep fields scoped and traceable.

## Core Shape

Use this logical structure even when an agent adds extra fields:

```json
{
  "person": {},
  "contact": {},
  "education": [],
  "experience": [],
  "projects": [],
  "papers": [],
  "skills": [],
  "awards": [],
  "links": [],
  "metrics": [],
  "mode": "",
  "sources": []
}
```

## Field Boundaries

- `person`: identity only, such as name, role/headline, location, short bio, and avatar path.
- `contact`: direct contact and public profile links only.
- `education`: school, degree, major, period, GPA, rank, coursework, academic roles, and education-specific notes.
- `experience`: internships, jobs, assistantships, volunteer roles, and role-specific bullets.
- `projects`: project names, roles, stacks, summaries, outcomes, and project-specific links.
- `papers`: publications, preprints, manuscripts, datasets, research pages, and paper-specific links.
- `skills`: grouped skills or skill tags from the resume.
- `awards`: competitions, scholarships, honors, grants, and recognitions.
- `links`: normalized public links with `label`, `url`, `kind`, `scope`, and `source`.
- `metrics`: optional normalized numeric facts with strict source scope.

## Metric Objects

When a numeric fact may be reused visually, record it with scope:

```json
{
  "label": "Major rank",
  "value": "9/128",
  "scope": "education",
  "source_section": "education",
  "belongs_to": "Huazhong University",
  "render_as_global": true
}
```

Allowed `scope` values:

- `person`: career-level or identity-level fact explicitly stated as personal.
- `education`: GPA, rank, degree year, academic honors tied to education.
- `experience`: role-local metrics from a job or internship.
- `project`: project-local metrics from one project.
- `paper`: publication-local metrics.
- `award`: award-local rank or prize information.

## Reuse Rules

- Only `person` and clearly relevant `education` metrics may appear in profile cards, sidebars, hero stats, or global highlight strips.
- `experience`, `project`, `paper`, and `award` metrics must stay inside their owning entry unless the resume explicitly summarizes them as a person-level achievement.
- If `render_as_global` is missing or false, do not use the metric outside its original section.
- If the source scope is unclear, do not create a metric card. Keep the number in body copy where it came from.

