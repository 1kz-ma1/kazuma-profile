# kazuma-profile

Personal website for sharing my products, development philosophy, and journey as a product developer.

## Purpose

This repository replaces the previous Django-based job-hunting portfolio with a lightweight static developer hub.

The site is designed to show not only finished work, but also:

- why a product was created
- how it was designed and implemented
- what changed after real use and evaluation
- how past projects influenced current work
- how my product-development philosophy evolves over time

## Stack

- Astro 7
- TypeScript
- Static site generation
- GitHub Actions
- Render Static Site

No application database, authentication, server-side sessions, or runtime secret keys are required for this site.

## Main routes

- `/` — Home
- `/projects` — Project index
- `/projects/canovia` — Canovia case study
- `/about` — Current profile and product-development philosophy
- `/blog` — Development notes and migrated historical articles
- `/blog/dream-hackathon` — 2024 Dream hackathon article + 2026 retrospective

## Development

Requires Node.js 22.12.0 or later.

```bash
npm install
npm run dev
```

Build for production:

```bash
npm run build
```

The production output is generated in `dist/`.

## Images

Site-owned images should be committed to `public/images/` so they are versioned with the site and deployed together with the static build.

Recommended structure:

```text
public/images/
├─ projects/
│  └─ canovia/
│     ├─ overview.webp
│     └─ dashboard.webp
├─ blog/
└─ profile/
```

Large screenshots should be converted to a web-friendly format such as WebP before committing.

## Render

This repository includes `render.yaml` for a Render Static Site.

- Build command: `npm install && npm run build`
- Publish directory: `dist`

The previous Railway/Django site should remain available until this static site has been deployed and verified. After migration is complete, the old runtime can be retired independently.
