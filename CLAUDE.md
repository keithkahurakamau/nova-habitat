# Nova-Habitat Technologies — Company landing site

## What this is
A single, self-contained static landing page for **Nova-Habitat Technologies** — a
Kenyan SaaS company providing cloud **POS and analytics** software for schools,
hospitals, hotels, restaurants and supermarkets (M-Pesa + KRA eTIMS, multi-branch).
**MediFleet** (clinical-grade hospital platform) is the first live product.

- **The site lives in `index.html`** — markup, CSS (in a `<style>` block), and a small
  inline JS (footer year + scroll-reveal IntersectionObserver). No build step, no
  dependencies, no framework.
- Brand assets: `logo.svg` (lockup), `logo-mark.svg` (icon), `favicon.svg`,
  `og-cover.svg` (1200×630 social image).
- SEO: `robots.txt`, `sitemap.xml`, plus geo meta + JSON-LD inside `index.html`.
- `vercel.json` — `cleanUrls` + a catch-all rewrite to `/index.html`.
- **Hosted on GitHub Pages** (`main` root, auto-deploys on push). Also Vercel-ready.

## Working in this repo
- Edit `index.html` directly. Keep it a single file — do not introduce a build
  pipeline, bundler, or external CSS/JS files unless explicitly asked.
- **Design system:** earthy theme — forest green (`--forest`/`--moss`) + clay brown
  (`--clay`) on warm paper (`--paper`), with a grain overlay. Fonts: **Fraunces**
  (display/headings) + **Hanken Grotesk** (body) — do NOT use Inter/Roboto.
  All tokens are CSS custom properties in `:root`; reuse them, don't hardcode colors.
- Reuse existing classes: `.wrap` container, `.btn`/`.btn-primary`/`.btn-ghost`/
  `.btn-clay`, `.eyebrow`, `.obs` (scroll-reveal), `.ind`/`.cap`/`.prod` cards.
- The brand mark is a leaf + four-point "nova" spark + clay stem. Keep header/footer
  inline marks in sync with `logo.svg` if you change it.
- Keep it accessible and responsive (breakpoints at `920px` and `600px`;
  `prefers-reduced-motion` is honored).
- SEO/canonical/OG use `https://nova-habitat.tech/` (the brand domain, not yet live).

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
