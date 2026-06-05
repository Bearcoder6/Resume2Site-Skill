# Extract Profile Prompt

Use this prompt to create `work/profile.json`.

## Read

- User-provided resume PDF, DOCX, TXT, or Markdown.
- Optional `avatar.png`, GitHub links, paper links, website links, and style preference files.
- Optional pasted summaries from the user.

If PDF or DOCX reading is unreliable, ask the user for `resume.txt`.

## Output

Create `work/profile.json` using this shape:

```json
{
  "person": {
    "name": "",
    "headline": "",
    "location": "",
    "bio": "",
    "avatar": ""
  },
  "contact": {
    "email": "",
    "phone": "",
    "website": "",
    "github": "",
    "linkedin": "",
    "google_scholar": ""
  },
  "education": [],
  "experience": [],
  "projects": [],
  "papers": [],
  "skills": [],
  "awards": [],
  "links": [],
  "mode": "",
  "sources": []
}
```

## Rules

- Do not hallucinate.
- Use empty strings or empty arrays for missing data.
- Preserve important factual details.
- Keep user-provided facts traceable when possible.
- Improve wording later, not during raw extraction.
- If GitHub or arXiv links are provided, summarize them only if you can access them. Otherwise ask the user to paste summaries.
- Do not directly generate the website from the raw resume.

## Source Notes

Add source hints in `sources`, such as:

```json
{
  "type": "resume",
  "path": "input/resume.pdf",
  "notes": "Education, projects, and contact extracted from resume."
}
```
