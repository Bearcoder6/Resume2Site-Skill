# Implementation Process

## Previous Problem

The repository had grown into a CLI/static-site-generator product. That made the positioning unclear and too heavy for a Skill. It included parser logic, package metadata, doctor checks, avatar extraction, asset downloading, tests, and product-style commands.

## New Decision

The project is now a pure Skill.

- Agent-powered file reading.
- No custom parser promise.
- No CLI promise.
- No package install.
- No deployment engine.
- Structured workflow and quality rules instead of product automation.

## New Architecture

```text
Root README and metadata
skills/resume2site/SKILL.md
skills/resume2site/rules and prompts
skills/resume2site/template references
skills/resume2site/fake examples
docs/install.md
docs/usage.md
docs/style-distillation/
```

## Removed Or Moved

The old CLI implementation, packaging files, tests, schema, product templates, and old examples were removed from the active tree. A Git backup branch preserves the previous state:

```text
backup/pre-pure-skill-refactor
```

## Retained

- MIT license.
- Resume2Site name and GitHub Pages goal.
- Academic and landing mode concepts.
- Privacy-first intent.
- Design-quality ambition.

## Future Extensions

To add a mode:

1. Add a mode rule file or extend `mode-rules.md`.
2. Add a layout rule file.
3. Add a generation prompt.
4. Add a template reference folder.
5. Add a fake example.
6. Update README and quality checklist.

To add a style pack:

1. Add notes under `docs/style-distillation/`.
2. Add concrete do/don't rules.
3. Add asset recommendation patterns.
4. Avoid copying exact designs.
