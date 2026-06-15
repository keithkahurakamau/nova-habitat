# Nova-Habitat Technologies

Company landing site for **Nova-Habitat Technologies** — software for the systems people depend on.

## Products

| Product | Status | Link |
|---------|--------|------|
| **MediFleet** — clinical-grade hospital management platform | Live | https://www.medifleet.app |

## Tech

A single self-contained static page (`index.html`) — no build step, no dependencies.
Deploys instantly to Vercel, GitHub Pages, Netlify, or any static host.

## Local preview

```bash
# any static server works, e.g.
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deploy (Vercel)

```bash
vercel --prod
```

The included `vercel.json` serves `index.html` for all routes.
