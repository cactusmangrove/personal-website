# Personal Website

A reusable map and data-story portfolio built with [Astro](https://astro.build)
and Tailwind CSS. It includes responsive gallery pages, static and interactive
article templates, metadata validation, a sitemap, and GitHub Pages deployment.

## Start here

```bash
npm install
npm run dev      # local development server
npm run build    # production site in dist/
```

Before publishing, replace the starter identity and links in:

- `src/components/Header.astro`
- `src/components/Footer.astro`
- `src/pages/index.astro`
- `src/pages/about.astro`
- `src/pages/maps/index.astro`
- `src/pages/maps/[...slug].astro`

Search for `Your Name` to find every identity placeholder.

## Create an article

Copy one of the Markdown templates in `src/content/maps/`, rename it, and edit
the frontmatter and article body. Put its preview image in `public/maps/`.

```markdown
---
title: "Project title"
description: "One-sentence card and search description."
date: 2026-01-01
image: /maps/project-preview.png
tools: [QGIS, JavaScript]
tags: [cartography, open-data]
draft: false
---

Write the project story here.
```

For an interactive project, also add:

```yaml
embedUrl: https://example.com/embeddable-map
externalUrl: https://example.com/full-screen-map
tallEmbed: false
```

An interactive article must provide both `embedUrl` and `externalUrl`. Static
articles omit both. Set `draft: true` to exclude unfinished work from the build.

When adding a non-language item to `tools`, register its official URL in
`src/data/tool-links.ts`. Tool links and article metadata are checked at build
time.

Use real, cited data in published work. Remove placeholder claims and link to
authoritative sources or documented reproducible calculations.

## GitHub Pages

The repository is configured for the project URL:

`https://ameliarowland.github.io/personal-website/`

If you fork or rename it, update `site` and `base` in `astro.config.mjs`. Then
choose **Settings → Pages → Source → GitHub Actions**. A push to `main` runs the
workflow in `.github/workflows/deploy.yml`.

## Customize the design

Global colors, typography, and long-form article styles live in
`src/styles/global.css`. The favicon is `public/favicon.svg`.
