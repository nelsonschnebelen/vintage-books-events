# Vintage Books — "What's On" events page

Static single-page site (`index.html`) deployed on Netlify at
https://vintagebooks-events.netlify.app/ — no build step (`publish = "."`).

## Workflow rules
- **Always push every change straight to `main`.** `main` is the live site
  (Netlify auto-deploys from it). Do not wait to be asked to push.
- Development branch for this work is `claude/hopeful-hawking-d050o1`; commit
  there, then push to both the branch and `main`.

## Flyers
- Event flyer images live in `assets/flyers/` and are wired into the page by
  filename in `index.html`. See `assets/flyers/README.txt` for the current
  filename → section mapping.
- Flyer assets are served with `Cache-Control: public, max-age=0,
  must-revalidate` (see `netlify.toml`), so overwriting a flyer in place shows
  up immediately — no need to rename for cache-busting.
- A small script in `index.html` shows a striped "flyer coming soon"
  placeholder for any flyer image that 404s, so missing art degrades gracefully.
