# Nostra Static Reveal

A single-page, solarpunk-inspired landing experience for Nostra that highlights three coordinated pillars with responsive, CSS-only interactivity.

## Project structure

```
/
├─ assets/
│  ├─ nostra-logo.webp
│  ├─ slide1-plant.png
│  ├─ slide2-room.jpg
│  └─ slide3.jpg          # optional, see below
├─ index.html
├─ styles.css
└─ vercel.json
```

## Adding your assets

1. Place the provided images in the `/assets` directory using these exact filenames:
   - `nostra-logo.webp`
   - `slide1-plant.png`
   - `slide2-room.jpg`
2. When you have artwork for the third slide, drop it in as `/assets/slide3.jpg`.

The third panel ships with a gradient “Coming soon” placeholder. Once you add the real `slide3.jpg`, edit the opening tag of `index.html` from:

```html
<html lang="en">
```

to:

```html
<html lang="en" class="has-slide3">
```

That single class tells the CSS to hide the placeholder and reveal your new image automatically—no other changes needed.

## Customizing copy

Each pillar is defined inside `index.html` within an `<article class="piece">`. Update the headings and paragraphs directly in those blocks. The solarpunk palette and typography can be tuned inside the CSS variables at the top of `styles.css`.

## Deployment

This site is fully static, so deploying to Vercel is straightforward:

1. **GitHub flow**: push this folder to a repository and import it at [vercel.com/new](https://vercel.com/new). Vercel auto-detects static sites and deploys immediately.
2. **CLI flow**: install the Vercel CLI (`npm i -g vercel`), authenticate, and run:

   ```bash
   vercel deploy
   ```

   Vercel will build and host the static files without additional configuration. The included `vercel.json` simply enables clean URLs.

Enjoy exploring Nostra’s pillars with smooth, motion-conscious interactions across desktop and mobile.
