# Mode Rules

Choose the mode from evidence in the resume and supporting materials.

## Academic Homepage

Choose academic mode when the resume includes strong academic signals:

- Publications.
- arXiv, DOI, journal, conference, workshop, thesis, or preprint.
- Research interests.
- Lab, advisor, professor, PhD, master student, research assistant.
- Academic awards, fellowships, grants, teaching, or university research projects.

Default style: `academic-editorial`.

## Personal Landing Page

Choose landing mode when the resume emphasizes:

- Job seeking.
- Product, design, engineering, creator, business, freelance, or client work.
- Internships and project portfolios.
- Personal brand, services, case studies, or selected works.

Default style: `engineering-commercial` for technical candidates, otherwise `business-polished`.

## Uncertain Cases

Ask the user which mode they prefer when evidence is balanced. If no answer is available, infer from dominant evidence and write the assumption in `work/site-plan.md`.

## Style Variant Selection

Choose one variant from `style-pack.md` after mode selection. Offer the user a choice only when the request is exploratory or the evidence is balanced.

- `academic-editorial`: research, papers, labs, graduate applications, faculty-style homepages.
- `academic-lab`: AI, engineering, data, lab/project-heavy academic resumes.
- `engineering-commercial`: backend, frontend, AI engineer, data engineer, product engineering, job seeking.
- `business-polished`: consulting, operations, product management, finance, enterprise-facing resumes.
- `creative-portfolio`: design, media, writing, creator, visual or client work.
- `minimal-resume-site`: conservative one-page sites when the user wants simple, fast, or very formal output.
