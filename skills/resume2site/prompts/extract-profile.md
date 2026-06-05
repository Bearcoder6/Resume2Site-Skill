# Extract Profile Prompt

Use this prompt to create `work/profile.json`.

## Read

- User-provided resume PDF, DOCX, TXT, or Markdown.
- Optional `avatar.png`, GitHub links, paper links, website links, and style preference files.
- `avatar-rules.md`.
- `profile-schema.md`.
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
  "links": [
    {
      "label": "",
      "url": "",
      "kind": "",
      "source": ""
    }
  ],
  "mode": "",
  "sources": []
}
```

## Rules

- Do not hallucinate.
- Use empty strings or empty arrays for missing data.
- Preserve important factual details.
- Preserve numeric facts with their source scope. Numbers from project or experience bullets, such as latency, API count, test count, throughput, cost, benchmark, or optimization results, must remain inside that specific `projects[]` or `experience[]` entry.
- Do not copy project-local or experience-local numbers into `person`, `contact`, headline, bio, or generic/global highlights.
- Treat a number as person-level only when the resume explicitly presents it as identity, education, honor, publication, or career-level information, such as GPA, major rank, graduation year, publication count, citation count, patent count, award count, or years of experience.
- When creating `metrics`, include `label`, `value`, `scope`, `source_section`, `belongs_to`, and `render_as_global`.
- Set `render_as_global` to `true` only for person-level or clearly global education-level facts. Leave project, experience, paper, and award metrics local.
- Preserve an existing portrait when reliable. If the user provides an avatar file or the resume includes a portrait image, save it into `output/site/assets/` when possible and set `person.avatar` to the relative path.
- For DOCX resumes, inspect embedded images such as `word/media/*` before deciding that no portrait exists.
- For PDF resumes, try embedded image extraction or first-page portrait crop fallback when available.
- If extraction fails, leave `person.avatar` empty and record the failed attempts in `sources` or `work/final-review.md`; do not invent or use a stock portrait.
- Preserve all meaningful hyperlinks from the resume and optional materials, including GitHub, arXiv, DOI, Google Scholar, personal websites, project demos, portfolios, datasets, videos, and paper/project pages.
- Put general profile links in `contact` when they clearly identify the person, and also keep them in `links` when they should be rendered as visible site links.
- Attach project-specific or paper-specific links to the corresponding `projects[]` or `papers[]` entry when possible. Also keep a normalized copy in `links` if it is useful for global navigation or contact areas.
- Use `kind` values such as `github`, `arxiv`, `doi`, `scholar`, `website`, `demo`, `portfolio`, `dataset`, `video`, or `other`.
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
