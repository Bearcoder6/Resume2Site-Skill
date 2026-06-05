# Asset Rules

The Skill may guide the agent to search for free, open-licensed, or clearly free-to-use visual assets when the website would benefit from a background image, texture, hero image, campus image, research visual, workspace image, or subtle editorial asset.

Do not treat "free download" as "safe to publish." Verify the license or usage terms for each asset before using it.

Create:

```text
work/asset-recommendations.md
output/site/ASSET_CREDITS.md
```

## Search Workflow

1. Decide whether the site needs a visual asset or can use CSS-only patterns.
2. Generate 3-6 search phrases based on the user's mode, field, and tone.
3. Search sources with explicit license or usage pages.
4. Check image dimensions before using a candidate as a background.
5. Prefer assets without identifiable people, brands, trademarks, or private locations.
6. Record candidates in `work/asset-recommendations.md`.
7. Use or download an asset only when its license/terms are clear and its resolution is suitable.
8. Write `output/site/ASSET_CREDITS.md` with source, title, author, license/terms, URL, and access date.

## Resolution Requirements

- Full-width hero or large background: prefer at least `3200px` wide; minimum `2560px` wide.
- Half-width hero image or large card visual: minimum `1800px` wide.
- Small decorative image or thumbnail: minimum `900px` wide.
- Portrait/avatar: minimum `600px` on the shorter side when possible.
- If a candidate fails the required size, do not stretch it as a background. Use it only as a small credited image, find a higher-resolution alternative, or use a CSS-only background.
- Avoid blurry, over-compressed, low-light, heavily cropped, or visibly upscaled images even if their pixel dimensions pass.

## International Sources

- Wikimedia Commons: best for openly licensed or public-domain educational, campus, library, research, historical, and architecture images. Verify the file page license and attribution requirements.
- Openverse: search engine for Creative Commons and public-domain media. Verify the original source page before use.
- Unsplash: free-to-use photos under the Unsplash License. Good for editorial backgrounds, workspace, nature, and city scenes. Avoid identifiable people and brands unless clearly appropriate.
- Pexels: free stock photos and videos under the Pexels License. Good for clean workspace, portrait-adjacent, and lifestyle backgrounds. Avoid generic stock people.
- Pixabay: royalty-free images, illustrations, video, audio, and other media under the Pixabay Content License. Check restrictions before use.

## Chinese / China-Friendly Sources

Use these only when the page clearly states usage rights for the specific asset:

- Wikimedia Commons with Chinese keywords: useful for Chinese campuses, libraries, city architecture, public-domain historical images, and cultural context.
- Openverse with Chinese keywords: useful for Creative Commons or public-domain media across multiple sources.
- Unsplash, Pexels, and Pixabay with Chinese keywords: useful when the user needs China-related scenes or Chinese search terms.
- 清若网 / sootu.art: candidate source for Chinese free-commercial visual materials; verify the asset page and terms before use.
- 图星人 / tuxingren.com: candidate source for AI-generated or commercial-use visual materials; verify the asset page and terms before use.

Avoid domestic素材站 if the page only says "free download" but does not clearly state commercial/public website usage rights.

## Academic Mode Assets

Prefer subtle, non-distracting assets:

- Paper texture.
- Library light.
- Research desk.
- Campus architecture.
- Abstract geometry.
- Soft grid.
- Subtle neural network pattern.
- Monochrome lab background.

## Landing Mode Assets

Prefer expressive but tasteful assets:

- Clean portrait background.
- Studio texture.
- Editorial background.
- Product workspace.
- Creative desk.
- Soft gradient mesh.
- Muted video background only when it helps and performance is acceptable.

## Rules

- Do not use unlicensed images.
- Do not use assets when the license page cannot be read.
- Do not use random stock people.
- Do not use images with visible brands, logos, celebrities, private individuals, or model-release ambiguity unless the user explicitly approves and the terms allow it.
- Do not use distracting background videos by default.
- Always include license and credit notes.
- If no asset is needed, use original CSS-only background patterns.
- Do not copy visual references exactly.
- Prefer attribution even when a platform says attribution is not required.

## Search Phrase Examples

Academic:

```text
library interior natural light
university campus architecture
research desk paper texture
abstract scientific grid
实验室 背景 光影
大学 校园 建筑
```

Landing:

```text
modern workspace desk
product engineering background
editorial portrait backdrop
creative studio texture
办公桌 科技 背景
产品 设计 工作台
```
