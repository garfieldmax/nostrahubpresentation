# Nostra Spine Reveal

A static, CSS-only presentation for Nostra's three guiding aspects. Hover, focus, or tap to reveal each sliver of the story.

## Structure

- `index.html` — the landing page with the hero, central zig-zag spine, and interactive content pieces.
- `styles.css` — all layout, motion, and accessibility styling.
- `assets/` — imagery and brand marks referenced in the layout. Keep existing filenames to avoid broken links.
- `vercel.json` — deployment preferences for Vercel (clean URLs, no trailing slash).

## Updating Copy or Layout

All copy lives directly in `index.html`. Update the headings and supporting text inline, then adjust styles if needed in `styles.css`. Maintain the `piece__eyebrow`, heading, paragraph, and figure structure so the hover/tap reveal animation remains intact.

## Image Management

Images are expected at:

- `/assets/nostra-logo.webp`
- `/assets/slide1-plant.png`
- `/assets/slide2-room.jpg`
- `/assets/slide3.jpg`

If an asset is not yet available, keep the filename reference in place; the layout will gracefully fall back. Specifically for the third slide, a gradient tile that reads “Coming soon” is shown by default.

To swap from the placeholder to the actual image:

1. Add `/assets/slide3.jpg` to the repository.
2. Open `index.html` and add `class="has-slide3"` to the `<html>` element.
3. The CSS will automatically hide the placeholder and display the real artwork.

## Accessibility & Motion

- Every piece is focusable and supports keyboard expansion via `:focus-within`.
- A skip link and visible focus ring are provided.
- Motion respects the user’s `prefers-reduced-motion` settings.

## Deploying on Vercel

1. Push your changes to GitHub (or another Git provider).
2. In the Vercel dashboard, import the repository.
3. For **Framework Preset**, choose **Other**.
4. Leave the **Build Command** empty and set **Output Directory** to `./`.
5. Deploy — Vercel will serve the static files as-is.

