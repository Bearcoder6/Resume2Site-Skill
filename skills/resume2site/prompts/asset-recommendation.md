# Asset Recommendation Prompt

Use this prompt when the site needs visual assets.

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

Licensing notes:

CSS-only fallback:
```

If final assets are used, create `output/site/ASSET_CREDITS.md` with source, author, license, and URL when known.

## Rules

- Recommend open or free sources only.
- Do not use unlicensed images.
- Do not use random stock people.
- Prefer CSS-only patterns when licensing is unclear.
- Do not copy user-provided inspiration exactly.
