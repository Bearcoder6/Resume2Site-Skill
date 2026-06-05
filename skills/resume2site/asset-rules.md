# Asset Rules

The Skill may guide the agent to search for free, open-licensed, or clearly free-to-use visual assets when the website would benefit from a background image, texture, hero image, research visual, workspace image, or subtle editorial asset.

Do not treat "free download" as "safe to publish." Verify the license or usage terms for each asset before using it.

Create:

```text
work/asset-recommendations.md
output/site/ASSET_CREDITS.md
```

For user/resume portraits, also follow `avatar-rules.md`. A resume portrait is user-provided content, not a stock asset search task.

## Search Strategy

Choose assets by the person's field, role, audience, and visual tone. Do not force a school, company, city, or exact location background unless it is visually strong and directly useful.

Good asset themes:

- Backend / infrastructure: abstract network texture, server aisle, terminal-like light, code workspace, datacenter detail, cool technical geometry.
- AI / ML: abstract tensor grid, research desk, lab screen glow, neutral computational pattern, paper-and-code visual.
- Product / design: editorial workspace, clean desk, studio texture, product board, muted creative environment.
- Academic: library light, paper texture, campus architecture, research desk, soft grid, abstract geometry, low-contrast lab or archive imagery.

The asset must work as a web background. It should have calm areas for text, natural cropping at desktop and mobile sizes, and enough visual restraint that it does not compete with the content.

## Search Workflow

1. Decide whether the site needs a visual asset or can use CSS-only patterns.
2. Generate 3-6 search phrases based on the user's field, role, and mode.
3. Search sources with explicit license or usage pages.
4. Check image dimensions before using a candidate as a background.
5. Check visual fit: background suitability, calm text zones, cropping, contrast, and relevance.
6. Prefer assets without identifiable people, brands, trademarks, or private locations.
7. Record candidates in `work/asset-recommendations.md`.
8. Use or download an asset only when its license/terms are clear and its resolution is suitable.
9. Write `output/site/ASSET_CREDITS.md` with source, title, author, license/terms, URL, and access date.

## Resolution Requirements

- Full-width hero or large background: prefer at least `3200px` wide; minimum `2560px` wide.
- Half-width hero image or large card visual: minimum `1800px` wide.
- Small decorative image or thumbnail: minimum `900px` wide.
- Portrait/avatar: minimum `600px` on the shorter side when possible.
- If the only available resume portrait is smaller than `600px`, it may still be used in a small profile slot. Do not upscale it into a large hero image.
- If a candidate fails the required size, do not stretch it as a background. Use it only as a small credited image, find a higher-resolution alternative, or use a CSS-only background.
- Avoid blurry, over-compressed, low-light, heavily cropped, or visibly upscaled images even if their pixel dimensions pass.

## Visual Fit Requirements

Reject an image if:

- It is technically high resolution but visually wrong for the role.
- It has strong signage, letters, logos, or accidental objects that draw attention.
- It only works because of a forced dark overlay.
- It crops badly on mobile.
- It looks like generic stock filler rather than a designed background.
- It makes the page feel tied to the wrong school, company, city, or building.

If no strong asset is available, use CSS-only atmosphere: layered gradients, soft grids, translucent panels, paper grain, code-like lines, or abstract geometry.

## International Sources

- Wikimedia Commons: best for openly licensed or public-domain educational, campus, library, research, historical, architecture, and technical images. Verify the file page license and attribution requirements.
- Openverse: search engine for Creative Commons and public-domain media. Verify the original source page before use.
- Unsplash: free-to-use photos under the Unsplash License. Good for editorial backgrounds, workspace, nature, and city scenes. Avoid identifiable people and brands unless clearly appropriate.
- Pexels: free stock photos and videos under the Pexels License. Good for clean workspace, portrait-adjacent, and lifestyle backgrounds. Avoid generic stock people.
- Pixabay: royalty-free images, illustrations, video, audio, and other media under the Pixabay Content License. Check restrictions before use.

## Chinese / China-Friendly Sources

Use these only when the page clearly states usage rights for the specific asset:

- Wikimedia Commons with Chinese keywords.
- Openverse with Chinese keywords.
- Unsplash, Pexels, and Pixabay with Chinese keywords.
- Qingruo / sootu.art: candidate source for Chinese free-commercial visual materials; verify the asset page and terms before use.
- Tuxingren / tuxingren.com: candidate source for AI-generated or commercial-use visual materials; verify the asset page and terms before use.

Avoid domestic asset sites if the page only says "free download" but does not clearly state commercial/public website usage rights.

## Academic Mode Assets

Prefer subtle, non-distracting assets:

- Paper texture.
- Library light.
- Research desk.
- Campus architecture only when visually strong.
- Abstract geometry.
- Soft grid.
- Subtle neural network pattern.
- Monochrome lab background.

Academic pages may combine transparent overlays, gradients, CSS paper texture, and low-contrast visual bands. They do not need a literal campus photo.

## Landing Mode Assets

Prefer expressive but tasteful assets:

- Clean portrait background.
- Studio texture.
- Editorial background.
- Product workspace.
- Technical grid or infrastructure-inspired abstract background.
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
- If no asset is visually suitable, use original CSS-only background patterns.
- Do not copy visual references exactly.
- Prefer attribution even when a platform says attribution is not required.

## Search Phrase Examples

Academic:

```text
library interior natural light
research desk paper texture
abstract scientific grid
machine learning research background
实验室 背景 光影
学术 纸张 纹理 背景
```

Landing:

```text
backend engineering abstract background
server room detail background
modern workspace desk
product engineering background
code grid dark background
办公桌 科技 背景
后端 工程 抽象 背景
```
