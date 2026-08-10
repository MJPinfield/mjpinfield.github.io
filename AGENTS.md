# AGENTS.md

Personal site of Max Pinfield — security engineer portfolio at [mjpinfield.co.uk](https://mjpinfield.co.uk). Single-page static site, GitHub Pages.

## Location

Local clone lives at `~/Coding/mjpinfield.github.io`. It was moved out of `~/Documents/Coding` (2026-08) because `~/Documents` is iCloud-synced ("Desktop & Documents") and macOS evicted ~9,400 files in `node_modules` to iCloud, making every build hang on on-demand re-downloads. **Do not keep active node projects under `~/Documents`.**

## Stack

- **Astro 5** (static output) + **Tailwind CSS v4** via `@tailwindcss/vite` plugin (see `astro.config.mjs`)
- **JetBrains Mono** self-hosted via `@fontsource-variable/jetbrains-mono` (imported in `global.css`)
- **Catppuccin Mocha** palette — all colors are `@theme` tokens in `src/styles/global.css` (e.g. `bg-base`, `text-mauve`)
- No JS framework; the only client JS is one inline `<script is:inline>` at the bottom of `src/pages/index.astro` (the streaming text effect)

## Commands

```bash
npm install     # or npm ci
npm run dev     # localhost:4321
npm run build   # → dist/
npm run preview
```

## Where things live

- **All page content**: `src/pages/index.astro` — hero/about/contact copy inline; `skillGroups` and `stats` arrays at the top of the frontmatter
- **Theme tokens + streaming CSS**: `src/styles/global.css`
- **HTML shell/meta**: `src/layouts/Layout.astro`
- **Deploy**: `.github/workflows/deploy.yml` (withastro/action → actions/deploy-pages). GitHub Pages source must stay set to **GitHub Actions**, not "deploy from branch".

## Conventions / design decisions (intentional, don't "fix")

- Terminal aesthetic: hero is a macOS-style terminal window; section headers use `# name` comment style
- The LinkedIn CTA is deliberately **not a button** — it's a text row styled like opencode's session epilogue: dim `Connect` label in a `w-[10ch]` column + bold `linkedin.com/in/mjpinfield` value
- Employer is kept generic ("a hedge fund") — do not name it
- Name appears once (hero); don't plaster it across sections
- LinkedIn is the only external link
- `CV.pdf` is gitignored on purpose — keep it uncommitted

## Gotchas

- **GitHub Pages caches HTML for ~10 min** — when verifying a deploy, hard-refresh or append a query string (`?v=...`)
- Streaming effect requirements: the `.js` class gate in `Layout.astro` + `[data-stream]`/`[data-fade]`/`[data-hide]` pre-hiding in `global.css` keep content visible for no-JS and `prefers-reduced-motion` users — preserve that pattern
- Each stream must create its **own** cursor element; a shared cursor across concurrent streams interleaves their text (bug fixed 2026-08-09)
- Hero vertical centering relies on `py-8` on the `min-h-svh` section — larger padding breaks centering on short viewports
