# Privacy Rules

This Skill does not promise automatic local masking. The agent must make careful publication choices.

## Required Rules

- Warn users before processing sensitive resumes.
- Do not copy raw resumes into `output/site/`.
- Do not publish private phone numbers unless the user clearly wants that.
- Prefer email, GitHub, LinkedIn, Google Scholar, or personal website links for public contact.
- If the user wants privacy, use placeholders in draft output.
- Never include hidden raw resume text in HTML comments.
- Never include internal notes, extraction logs, or mapping files in public output.
- Never explain privacy decisions in public page copy, such as "phone omitted by privacy rule". Record those notes only in `work/final-review.md`.
- Do not publish home addresses, private IDs, birth dates, or unrelated personal details.

## Recommended Privacy Workflow

If the user is privacy-sensitive, ask them to provide a sanitized `resume.txt` or explicitly approve the public contact details to include.

## Public Contact Defaults

Safe defaults are:

- Name.
- Professional headline.
- Public email if already on the resume and appropriate.
- GitHub, LinkedIn, Scholar, ORCID, or personal website links.

Risky defaults are:

- Phone number.
- Full street address.
- Private school ID or employee ID.
- Personal identifiers unrelated to the public website.
