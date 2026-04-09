# timo-goetz-ai.de — Portfolio

Personal portfolio and project showcase for Timo Goetz — KI-Beauftragter & AI Engineer.

**Live:** [timo-goetz-ai.de](https://timo-goetz-ai.de)  
**Account:** ai_studio@timo-goetz-ai.de  
**Deploy:** Vercel (auto on push to `main`)

## Stack

- [Astro](https://astro.build/) — Static site generator
- Tailwind CSS — Utility-first styling
- TypeScript
- Vercel — Hosting & CI/CD

## Local Development

```bash
npm install
npm run dev       # http://localhost:4321
npm run build     # Production build
```

No environment variables required.

## Structure

```
src/
├── content/projects/   # Project entries (Markdown + frontmatter)
├── layouts/            # BaseLayout
├── pages/              # Routes: /, /about, /contact, /projects/[slug]
└── styles/             # Global CSS (design tokens via CSS variables)
```

## Adding a Project

Create `src/content/projects/my-project.md`:

```yaml
---
title: "Project Name"
problem: "What problem does it solve?"
solution: "How it solves it."
stack: ["Tech", "Stack"]
status: "live"   # live | dev | wip
order: 5
demo: "https://github.com/timo-goetz-ai/..."
kpi: "Measurable outcome"
---

Markdown content here.
```

Push to `main` → Vercel deploys automatically.
