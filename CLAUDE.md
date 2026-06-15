# Nova-Habitat Technologies — Company landing site

## What this is
A single, self-contained static landing page for **Nova-Habitat Technologies**, the
company behind **MediFleet** (a clinical-grade hospital management platform).

- **Everything lives in `index.html`** — markup, CSS (in a `<style>` block), and the
  one line of JS (footer year). No build step, no dependencies, no framework.
- `vercel.json` — `cleanUrls` + a catch-all rewrite to `/index.html`.
- Deploys to Vercel (or any static host: GitHub Pages, Netlify).

## Working in this repo
- Edit `index.html` directly. Keep it a single file — do not introduce a build
  pipeline, bundler, or external CSS/JS files unless explicitly asked.
- Design tokens are CSS custom properties in `:root` (`--bg`, `--ink`, `--brand`,
  etc.). Reuse them rather than hardcoding colors.
- Match the existing style: `Inter` font, dark theme, `.wrap` max-width container,
  `.btn`/`.btn-primary`/`.btn-ghost` button classes, `.product` cards.
- Keep it accessible and responsive (there's a mobile breakpoint at `640px`).

## Preview locally
```bash
python3 -m http.server 8080   # then open http://localhost:8080
```

## Deploy
```bash
vercel --prod                  # vercel.json serves index.html for all routes
```

## Conventions
- Commit messages: Conventional Commits (`feat:`, `fix:`, `chore:`), as in history.
- Default branch is `main`; remote is `origin`. Only push when asked.
