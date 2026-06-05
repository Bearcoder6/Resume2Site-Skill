# Usage

Use Resume2Site-Skill by giving your agent a resume and asking it to follow the Skill.

## Academic Example

```text
Use the Resume2Site Skill to convert my resume into an academic personal homepage.
My files are in ./input.
Use academic mode.
Create the site in ./output/site.
Do not invent publications or affiliations.
Before finishing, run the final quality checklist.
```

## Landing Example

```text
Use the Resume2Site Skill to convert my resume into a polished personal landing page.
Use landing mode.
Make it suitable for GitHub Pages.
Use a modern but not generic style.
Create profile.json and site-plan.md before generating HTML.
```

## Style Direction Example

```text
Use the Resume2Site Skill.
Use its built-in academic and landing style rules.
Make the page polished without copying generic templates.
If you use visual assets, search free/open/licensed sources and create ASSET_CREDITS.md.
```

Optional screenshot reference:

```text
Also look at screenshots in ./docs/style-references only as supplemental mood references.
Do not copy exact layouts, artwork, or assets.
Keep the built-in Resume2Site style rules as the baseline.
```

## Suggested Input Folder

```text
input/
  resume.pdf or resume.docx or resume.txt
  avatar.png
  github_links.txt
  paper_links.txt
  website_links.txt
  style_preference.txt
  references/
```

If PDF or DOCX reading fails, provide `resume.txt`.

## Required Intermediate Step

The agent must create:

```text
work/profile.json
work/site-plan.md
```

before generating HTML/CSS.

## Expected Output

```text
output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```
