# Asset Recommendation Prompt

Use this prompt when the site needs visual assets or when the user asks for a more polished visual style.

## Read

- `work/profile.json`.
- `work/site-plan.md`.
- `asset-rules.md`.
- User style preferences and references.

## Output

Create `work/asset-recommendations.md`:

```text
# Asset Recommendations

Mode:
Visual direction:

Recommended searches:
1.
2.
3.

Potential sources:

Candidate assets:

Licensing notes:

CSS-only fallback:
```

If final assets are used, create `output/site/ASSET_CREDITS.md` with source, title, author, license/terms, URL, and access date when known.

## Rules

- Recommend open, free-to-use, or clearly licensed sources only.
- Do not use unlicensed images.
- Verify the source page, not only a search result snippet.
- Do not use random stock people.
- Prefer Wikimedia Commons or Openverse when strict open licensing matters.
- For Unsplash, Pexels, Pixabay, 清若网, 图星人, or other platform-license sources, record the platform terms and asset page.
- Prefer CSS-only patterns when licensing is unclear.
- Do not copy user-provided inspiration exactly.
