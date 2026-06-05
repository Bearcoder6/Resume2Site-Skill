# Final Review Prompt

Use this prompt before finishing.

This review must be lightweight and file-based by default. Do not start a browser, run Playwright, capture screenshots, launch a local server, or require any visual testing dependency unless the user explicitly requested it.

## Read

- `quality-checklist.md`.
- `bad-smell-checklist.md`.
- `work/profile.json`.
- `work/site-plan.md`.
- Generated `output/site/` files.

## Output

Create `work/final-review.md`:

```text
# Final Review

Shared checks:
Academic or landing checks:
Privacy checks:
Asset credit checks:
Avatar checks:
Mobile/design checks:
Fixes made:
Remaining notes:
```

## Rules

- Fix critical failures before reporting completion.
- Do not publish raw resumes, internal notes, or private mappings.
- Confirm generated files exist.
- Confirm the site does not contain fake facts.
- Confirm project-local or experience-local numbers, such as latency, API count, test count, throughput, cost, or benchmark results, remain inside their original project/experience sections and are not displayed as personal/profile metrics.
- Confirm the profile schema boundaries are respected: identity, contact, education, experience, projects, papers, awards, links, and metrics are not mixed.
- Confirm the page uses explicit design tokens and avoids the visual bad smells list.
- Confirm public copy does not reveal generation process, source file type, privacy-rule decisions, metric-placement rules, final-review notes, or internal Skill behavior.
- Confirm the design is not just a raw resume.
- Confirm any detected resume portrait is either used from `output/site/assets/` or has a recorded extraction failure note.
- Confirm generated HTML has `<meta charset="utf-8">` and visible page copy does not expose internal style variant names.
- Confirm the final answer includes the local path to `output/site/index.html`.
