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

Resolution check:

Visual fit check:

CSS-only fallback:
```

If final assets are used, create `output/site/ASSET_CREDITS.md` with source, title, author, license/terms, URL, and access date when known.

## Rules

- Recommend open, free-to-use, or clearly licensed sources only.
- Do not use unlicensed images.
- Verify the source page, not only a search result snippet.
- Record image dimensions and reject images that are too small for the intended placement.
- For full-width backgrounds, prefer 3200px+ wide images and require at least 2560px wide.
- Reject high-resolution images if they are visually wrong for the person's field, crop badly, contain distracting signage, or do not work as a webpage background.
- Prefer CSS-only backgrounds when no asset is both licensed and visually suitable.
- Do not use random stock people.
- Prefer Wikimedia Commons or Openverse when strict open licensing matters.
- For Unsplash, Pexels, Pixabay, Qingruo / sootu.art, Tuxingren / tuxingren.com, or other platform-license sources, record the platform terms and asset page.
- Prefer CSS-only patterns when licensing is unclear.
- Do not copy user-provided inspiration exactly.
