# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an academic website for NPClab (Neural Processing and Cognition Lab) at Kangwon National University, built using the [al-folio Jekyll theme](https://github.com/alshedivat/al-folio). The site is deployed to GitHub Pages at https://heejyang.github.io/NPClab/.

## Development Commands

### Local Development (Docker - Recommended)

```bash
# Pull and run the site locally
docker compose pull
docker compose up

# Access at http://localhost:8080
```

For a slimmer docker image (<100MB):

```bash
docker compose -f docker-compose-slim.yml up
```

### Local Development (Ruby/Jekyll)

```bash
# Install dependencies
bundle install
pip install jupyter

# Serve the site locally
bundle exec jekyll serve
# Access at http://localhost:4000
```

### Build Commands

```bash
# Production build
export JEKYLL_ENV=production
bundle exec jekyll build

# Purge unused CSS
npm install -g purgecss
purgecss -c purgecss.config.js
```

### Code Quality

```bash
# Format with Prettier
npx prettier --write .
```

## Architecture

### Site Structure

This is a Jekyll static site with the following key directories:

- `_config.yml` - Main configuration file containing site metadata, Jekyll Scholar settings, plugin configurations
- `_pages/` - Main pages (about.md, cv.md, publications.md, etc.)
- `_posts/` - Blog posts (named YYYY-MM-DD-title.md)
- `_projects/` - Project descriptions
- `_news/` - News items displayed on the about page
- `_photos/` - Photo gallery items
- `_bibliography/papers.bib` - Publications in BibTeX format
- `_data/` - Data files (cv.yml, repositories.yml, socials.yml, coauthors.yml, citations.yml, venues.yml)
- `_layouts/` - HTML templates for pages (about.liquid, post.liquid, bib.liquid, etc.)
- `_includes/` - Reusable HTML components
- `_sass/` - SCSS stylesheets
- `_plugins/` - Custom Jekyll plugins for citations, external posts, etc.
- `assets/` - Static assets (images, PDFs, JS, CSS)
  - `assets/json/resume.json` - CV in JSON Resume format (takes precedence over \_data/cv.yml)

### Content Management

**Publications**: Managed through `_bibliography/papers.bib`. The Jekyll Scholar plugin automatically generates the publications page. Supported BibTeX fields include: abstract, pdf, code, slides, website, blog, arxiv, doi, video, poster.

**CV**: Two options:

1. JSON format at `assets/json/resume.json` (preferred, follows jsonresume.org standard)
2. YAML fallback at `_data/cv.yml`

**Collections**: Jekyll collections for news, projects, books, and photos are defined in `_config.yml` under the `collections` key.

### Plugin System

Key plugins in `_plugins/`:

- `google-scholar-citations.rb` - Fetches citation counts from Google Scholar
- `inspirehep-citations.rb` - Fetches citation counts from InspireHEP
- `external-posts.rb` - Integrates external blog posts
- `download-3rd-party.rb` - Downloads third-party libraries when `third_party_libraries.download: true`

### Deployment

The site deploys automatically via GitHub Actions (`.github/workflows/deploy.yml`) when pushing to `main` or `master` branch. The workflow:

1. Builds the Jekyll site with ImageMagick support for responsive images
2. Converts Jupyter notebooks using nbconvert
3. Purges unused CSS with PurgeCSS
4. Deploys to `gh-pages` branch

**Important**: The `gh-pages` branch is auto-generated - never edit it directly. All changes must be made to the `main` branch.

## Configuration Notes

### Site Settings (\_config.yml)

- `url`: Base URL (https://heejyang.github.io)
- `baseurl`: Subpath (/NPClab) - required for project pages
- `scholar.last_name` and `scholar.first_name`: Used to highlight author name in publications
- `max_author_limit: 3`: Shows first 3 authors, rest revealed on click

### Jekyll Scholar

Publications are sorted by year (descending) by default. Configuration in `_config.yml`:

- `source: /_bibliography/`
- `bibliography: papers.bib`
- `style: apa`
- `group_by: year`
- `group_order: descending`

### Third-Party Libraries

Managed in `_config.yml` under `third_party_libraries`. Set `download: false` to use CDN links, or `download: true` to download locally (useful for offline development).

## Common Tasks

### Adding Publications

Edit `_bibliography/papers.bib` and add BibTeX entries. Example:

```bibtex
@article{yang2024example,
  title={Example Title},
  author={Yang, Heejung and Others},
  journal={Journal Name},
  year={2024},
  pdf={example.pdf},
  code={https://github.com/user/repo},
  abstract={Your abstract here}
}
```

Place PDF files in `assets/pdf/`.

### Creating Pages

Create a new Markdown file in `_pages/` with frontmatter:

```yaml
---
layout: page
permalink: /yourpage/
title: Your Page Title
description: Optional description
nav: true
nav_order: 5
---
```

### Adding News Items

Create a file in `_news/` with frontmatter:

```yaml
---
layout: post
date: 2024-01-26
inline: true
---
Your news content here.
```

### Modifying Styles

Theme colors are in `_sass/_themes.scss` (change `--global-theme-color` variable). Other style variables are in `_sass/_variables.scss`.

## Important Notes

- Always test locally before pushing to main
- Changes to `_config.yml` require rebuilding the site
- When using Docker, the site auto-reloads on file changes
- BibTeX entries are cached by Jekyll Scholar - delete `.jekyll-cache/` if changes don't appear
- ImageMagick must be installed for responsive images to work
- The site uses collections (news, projects, books, photos) defined in `_config.yml`
