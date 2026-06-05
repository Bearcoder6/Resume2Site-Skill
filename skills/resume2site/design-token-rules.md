# Design Token Rules

Use lightweight design tokens so pages feel intentionally designed rather than template-generated.

## Shared Token Requirements

Define tokens in CSS variables or equivalent:

```css
:root {
  --bg: ;
  --surface: ;
  --ink: ;
  --muted: ;
  --line: ;
  --accent: ;
  --accent-2: ;
  --radius: ;
  --shadow: ;
  --page-max: ;
}
```

## Typography

- Use a clear font stack that fits the resume language.
- For Chinese resumes, prefer Chinese-first labels and body copy.
- Do not rely on browser default serif/sans without an intentional stack.
- Keep type scale balanced: hero name, headline, section title, card title, body, metadata.
- Do not make section headings compete with the person's name.

## Layout Tokens

- Desktop-first target: `1366px` to `1440px`.
- Recommended page max width: `1120px` to `1380px`, depending on style.
- Use stable grid columns for sidebars, hero media, project grids, and timelines.
- Avoid nested cards and excessive rounded cards.
- Prefer borders, rules, spacing, and type hierarchy over heavy shadows.

## Variant Token Guidance

- `academic-editorial`: near-white paper, fine borders, subtle texture, low radius `0-6px`, restrained ink/green/navy accents.
- `academic-lab`: light research atmosphere, translucent but readable panels, soft grid, radius `6-10px`.
- `engineering-commercial`: dark or neutral technical system, crisp panels, one strong accent, radius `4-8px`.
- `business-polished`: premium light surface, precise spacing, sober accent, radius `4-8px`, minimal shadows.
- `creative-portfolio`: expressive composition, stronger image treatment, editorial asymmetry, radius chosen deliberately.
- `minimal-resume-site`: high readability, little decoration, low or zero radius, no oversized hero.

## Anti-AI Visual Rules

- Avoid generic purple-blue gradients, glass cards everywhere, random icon grids, huge round cards, and SaaS-style fake proof strips.
- Do not use metric cards unless the metrics are person-level and useful.
- Do not let decorative visuals overpower resume facts.
- Use no-metric and no-card layouts when they are cleaner.

