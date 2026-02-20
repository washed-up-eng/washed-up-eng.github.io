# Personal Website (Astro)

This repository contains a personal website built with Astro and deployed to GitHub Pages.

## Local development

- Install dependencies: `npm install`
- Start dev server: `npm run dev`
- Build static site: `npm run build`
- Preview built site: `npm run preview`

## Deploy to GitHub Pages

This repo includes a workflow at `.github/workflows/deploy.yml`.

1. Push to the `main` branch.
2. In GitHub, open `Settings -> Pages`.
3. Set `Source` to `GitHub Actions`.
4. Wait for the `Deploy to GitHub Pages` workflow to complete.

The site URL is configured in `astro.config.mjs` as `https://washed-up-eng.github.io`.

## Customize content

- Main page content: `src/pages/index.astro`
- Base HTML metadata and global styles: `src/layouts/Layout.astro`
