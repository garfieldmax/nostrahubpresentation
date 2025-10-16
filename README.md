# Nostra Diagonal Reveal

A static, CSS-only hero that keeps the Nostra logo front and center while three diagonal slices expand to reveal more context on hover or focus.

## Structure

- `index.html` — full-screen stage with the logo backdrop and three diagonal slices.
- `styles.css` — layout, motion, accessibility, and responsive behavior.
- `assets/` — imagery used for the slices and the logo. Keep filenames the same to avoid broken references.
- `vercel.json` — deployment settings for Vercel (clean URLs, no trailing slash).

## Editing Content

Each slice has a short eyebrow label and body copy directly inside `index.html`. Update the text inline. Imagery is handled via the `<figure>` markup in each slice.

## Slide Three Placeholder

If `/assets/slide3.jpg` is not yet available, the third slice shows a gradient tile that reads “Coming soon.”

To switch over once the artwork exists:

1. Add `/assets/slide3.jpg` to the repository.
2. Add `class="has-slide3"` to the `<html>` element in `index.html`.
3. The CSS automatically hides the placeholder and displays the real image.

## Accessibility & Interaction

- Slices are focusable (`tabindex="0"`) and expose their expanded state on focus, mirroring the hover experience.
- A skip link is available for keyboard users.
- Motion respects `prefers-reduced-motion`.
- On small screens, slices stack vertically and remain expanded for easier reading.

## Deploying on Vercel

1. Push the repo to your Git provider.
2. In Vercel, import the repository.
3. Choose **Other** for the Framework Preset.
4. Leave the build command empty and keep the output directory as `./`.
5. Deploy — Vercel will host the static files as-is.
