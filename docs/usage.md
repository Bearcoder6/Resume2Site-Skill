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

## Style Reference Example

```text
Use the Resume2Site Skill.
Also analyze screenshots in ./docs/style-references as style inspiration.
Do not copy exact layouts or assets.
Distill the style into an original personal website.
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
