# Final Review Prompt

Use this prompt before finishing.

This review must be lightweight and file-based by default. Do not start a browser, run Playwright, capture screenshots, launch a local server, or require any visual testing dependency unless the user explicitly requested it.

## Read

- `quality-checklist.md`.
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
Mobile/design checks:
Fixes made:
Remaining notes:
```

## Rules

- Fix critical failures before reporting completion.
- Do not publish raw resumes, internal notes, or private mappings.
- Confirm generated files exist.
- Confirm the site does not contain fake facts.
- Confirm the design is not just a raw resume.
- Confirm the final answer includes the local path to `output/site/index.html`.
