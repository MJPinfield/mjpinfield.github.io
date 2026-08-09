# mjpinfield.github.io

Personal site of Max Pinfield — Security Engineer. Built with Astro and Tailwind CSS v4.

🌐 **Live site**: [mjpinfield.co.uk](https://mjpinfield.co.uk)

## Tech Stack

- **Framework**: Astro (static output, one small inline script for the streaming text effect)
- **Styling**: Tailwind CSS v4 (via `@tailwindcss/vite`)
- **Theme**: Catppuccin Mocha, JetBrains Mono (self-hosted via Fontsource)
- **Hosting**: GitHub Pages with custom domain, deployed via GitHub Actions

## Development

### Prerequisites

- Node.js 20+

### Commands

```bash
npm install     # install dependencies
npm run dev     # dev server at http://localhost:4321
npm run build   # production build to dist/
npm run preview # preview the production build
```

## Project Structure

```
.
├── .github/workflows/deploy.yml  # GitHub Actions → GitHub Pages
├── astro.config.mjs              # Astro config (site URL, Tailwind plugin)
├── public/
│   ├── CNAME                     # custom domain
│   └── favicon.svg
└── src/
    ├── layouts/Layout.astro      # HTML shell + meta
    ├── pages/index.astro         # all page content (hero, about, skills)
    └── styles/global.css         # Tailwind + Catppuccin theme tokens
```

## Editing Content

All content lives in `src/pages/index.astro`:

- **Hero/about text** — edit the markup directly
- **Skills** — edit the `skillGroups` array at the top of the file
- **Colors/theme** — edit the `@theme` block in `src/styles/global.css`

## Deployment

Push to `main` — the GitHub Actions workflow builds and deploys automatically.
Requires the repo's Pages source to be set to **GitHub Actions** (Settings → Pages).
