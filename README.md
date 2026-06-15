# Nova-Habitat Technologies

Company landing site for **Nova-Habitat Technologies** — cloud **POS and analytics
software** for the businesses Kenya depends on: schools, hospitals, hotels,
restaurants and supermarkets. M-Pesa payments and KRA eTIMS invoicing built in.

🌐 Live: https://keithkahurakamau.github.io/nova-habitat/ · Brand domain: nova-habitat.tech

## Products

| Product | Status | Link |
|---------|--------|------|
| **MediFleet** — clinical-grade hospital management platform | Live | https://www.medifleet.app |
| School / Hospitality / Retail suites | In development | — |

## Tech & files

A single self-contained static page — no build step, no dependencies.

| File | Purpose |
|------|---------|
| `index.html` | The entire site (markup, CSS, JS inline) |
| `logo.svg` | Horizontal logo lockup (mark + wordmark) |
| `logo-mark.svg` | Icon only (app icon / social avatar) |
| `favicon.svg` | Browser favicon |
| `og-cover.svg` | 1200×630 social share image |
| `robots.txt`, `sitemap.xml` | SEO crawl directives |
| `vercel.json` | Vercel static config (clean URLs) |

> **Design:** earthy theme — forest green + clay brown, Fraunces + Hanken Grotesk.
> Theme tokens live as CSS custom properties in `:root` inside `index.html`.

## SEO

Optimised for the Kenyan market: localized title/description/keywords, geo meta tags
(`geo.region=KE`), Open Graph + Twitter cards, JSON-LD structured data
(Organization, SoftwareApplication, FAQPage), `sitemap.xml` and `robots.txt`.

> **Note:** Social platforms prefer a PNG OG image. `og-cover.svg` is provided as the
> source — export it to `og-cover.png` (1200×630) and update the `og:image` /
> `twitter:image` paths if you need maximum share-preview compatibility.

## Local preview

```bash
python3 -m http.server 8080   # then open http://localhost:8080
```

## Deploy

The site is live on **GitHub Pages** (auto-deploys on every push to `main`).
It also deploys to Vercel via the included `vercel.json` (`vercel --prod`).
