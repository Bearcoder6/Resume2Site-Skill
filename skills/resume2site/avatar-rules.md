# Avatar Rules

Treat the user's real resume portrait as a high-priority asset when it exists. Do not silently drop it.

## Extraction Priority

Use this order:

1. Explicit user-provided avatar file, such as `avatar.png`, `avatar.jpg`, or an image path in the prompt.
2. DOCX embedded images. Inspect `word/media/*` or use the agent environment's document tooling to extract images.
3. PDF embedded images or page render. If direct image extraction fails, render the first resume page and crop the likely portrait region.
4. Screenshot/crop fallback from the resume page only when the environment can do it without heavy setup.
5. No-avatar layout only after the attempts above fail.

## DOCX Heuristics

- Many Chinese resume templates place the portrait in the top-right or top-left table cell.
- If multiple images exist, prefer the one with a portrait-like aspect ratio, usually between `0.7` and `1.4`, and reasonable size.
- Ignore tiny icons, logos, QR codes, decorative lines, and background fragments.
- Save the chosen image to `output/site/assets/avatar.<ext>` and set `person.avatar` to that relative path.

## PDF / Rendered Page Heuristics

If no embedded image can be recovered:

- Render the first page at a high enough resolution when available.
- Search likely resume portrait zones first: top-right, top-left, and upper profile area.
- Crop a clean rectangular portrait area rather than stretching or distorting the full page.
- Prefer a complete face/portrait over a tight crop. Do not cut off the head if a larger crop is possible.
- If the crop quality is poor, use a no-avatar design and record the reason.

## Output Notes

- Put the final public avatar in `output/site/assets/`.
- Use relative paths in HTML, such as `assets/avatar.jpg`.
- Record the chosen method in `work/final-review.md`.
- If no avatar is used, write a short note in `work/final-review.md` explaining which attempts failed.
- Do not invent, generate, or use a stock portrait as a substitute unless the user explicitly asks.
