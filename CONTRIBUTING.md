# Contributing

Thanks for helping improve Resume2Site-Skill.

This project is a lightweight Agent Skill, not a CLI product. Contributions should strengthen the instructions, prompts, examples, design guidance, privacy rules, or agent compatibility.

## Good Contributions

- Clearer workflow rules.
- Better academic homepage guidance.
- Better personal landing page guidance.
- Stronger factual writing and anti-hallucination rules.
- Better fake examples.
- Better style distillation notes.
- More precise privacy and asset-credit guidance.

## Please Avoid

- Adding a required CLI or package runtime.
- Promising automatic PDF or DOCX parsing.
- Adding generated websites to the repository.
- Adding real resumes or private user data.
- Adding unlicensed images.

## Development Notes

Keep `skills/resume2site/SKILL.md` concise and route detailed guidance to nearby Markdown files. Prompts should be practical enough for an agent to use directly.

Before opening a pull request, check:

```text
skills/resume2site/SKILL.md exists
skill.json points to skills/resume2site/SKILL.md
README.md describes the project as a Skill
No raw resumes or generated output are committed
```
