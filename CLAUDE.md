# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based GitHub Pages site for mjpinfield.co.uk. The repository is currently in its initial state with basic Jekyll configuration.

## Development Commands

### Local Development (if Ruby/Jekyll is properly installed)
```bash
# Install GitHub Pages compatible dependencies
bundle install

# Serve the site locally with auto-reload
bundle exec jekyll serve

# Build the site for production
bundle exec jekyll build
```

### GitHub Pages Deployment
The site automatically deploys to GitHub Pages when changes are pushed to the main branch. The current setup uses:
- `github-pages` gem for maximum compatibility
- TailwindCSS via CDN (no build step required)
- Standard Jekyll structure

**Note**: Local development requires Ruby and Jekyll setup. If you encounter permission issues with system Ruby, consider using rbenv or rvm to manage Ruby versions locally.

### Current Status
The site structure is complete and ready for GitHub Pages deployment. The setup includes:
- Responsive homepage with hero section, about preview, skills showcase, and project grid
- Professional navigation and footer
- TailwindCSS styling via CDN
- SEO optimization with jekyll-seo-tag

## Jekyll Site Structure

When fully developed, this Jekyll site will typically include:
- `_config.yml` - Jekyll configuration
- `_layouts/` - HTML templates
- `_includes/` - Reusable HTML snippets
- `_posts/` - Blog posts (if using Jekyll blogging features)
- `_sass/` - Sass/SCSS stylesheets
- `assets/` - CSS, JS, images, and other static files
- `index.md` or `index.html` - Home page

## Important Notes

- This repository uses GitHub Pages Jekyll deployment
- The .gitignore is specifically configured for Jekyll and GitHub Pages
- Local `Gemfile.lock` should not be committed (GitHub Pages ignores it)
- Site builds automatically on push to main branch