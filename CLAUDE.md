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
- `_pages/` - Main pages (about.md, cv.md, publications.md, projects.md, photos.md, profiles.md, teaching.md, repositories.md, news.md, etc.)
- `_posts/` - Blog posts (named YYYY-MM-DD-title.md)
- `_projects/` - Project descriptions displayed on projects page
- `_news/` - News items displayed on the about page
- `_photos/` - Photo gallery items with PhotoSwipe integration
- `_books/` - Book reviews and reading list
- `_bibliography/papers.bib` - Publications in BibTeX format
- `_data/` - Data files (cv.yml, repositories.yml, socials.yml, coauthors.yml, citations.yml, venues.yml)
- `_layouts/` - HTML templates for pages (about.liquid, post.liquid, bib.liquid, profiles.liquid, book-review.liquid, book-shelf.liquid, etc.)
- `_includes/` - Reusable HTML components
- `_sass/` - SCSS stylesheets
- `_plugins/` - Custom Jekyll plugins for citations, external posts, caching, etc.
- `_scripts/` - Helper scripts for development and maintenance
- `assets/` - Static assets (images, PDFs, JS, CSS)
  - `assets/json/resume.json` - CV in JSON Resume format (takes precedence over \_data/cv.yml)
  - `assets/img/` - Images (automatically optimized to WebP with responsive sizes)

### Content Management

**Publications**: Managed through `_bibliography/papers.bib`. The Jekyll Scholar plugin automatically generates the publications page. Supported BibTeX fields include: abstract, pdf, code, slides, website, blog, arxiv, doi, video, poster.

**CV**: Two options:

1. JSON format at `assets/json/resume.json` (preferred, follows jsonresume.org standard)
2. YAML fallback at `_data/cv.yml`

**Collections**: Jekyll collections are defined in `_config.yml` under the `collections` key:
- `news` - News announcements (output: true)
- `projects` - Research projects (output: true)
- `books` - Book reviews and reading list (output: true)
- `photos` - Photo gallery with PhotoSwipe lightbox support (output: true)

**Data Files**: YAML files in `_data/` directory:
- `cv.yml` - CV data (fallback if resume.json not present)
- `repositories.yml` - GitHub repository showcase
- `socials.yml` - Social media links
- `coauthors.yml` - Co-author information for publications
- `citations.yml` - Citation data (auto-updated by Google Scholar workflow)
- `venues.yml` - Publication venue abbreviations and full names

### Plugin System

**Custom Plugins** in `_plugins/`:

- `google-scholar-citations.rb` - Fetches citation counts from Google Scholar
- `inspirehep-citations.rb` - Fetches citation counts from InspireHEP
- `external-posts.rb` - Integrates external blog posts from Medium, RSS feeds, or direct URLs
- `download-3rd-party.rb` - Downloads third-party libraries when `third_party_libraries.download: true`
- `cache-bust.rb` - Adds cache busting parameters to assets
- `details.rb` - Custom Liquid tag for collapsible details/summary elements
- `file-exists.rb` - Checks if files exist before including them
- `hide-custom-bibtex.rb` - Filters custom BibTeX fields from display
- `remove-accents.rb` - Normalizes accented characters in URLs and slugs

**Jekyll Plugins** (installed via Gemfile):

- `jekyll-archives-v2` - Archive pages for blog posts by year, tags, categories
- `jekyll-email-protect` - Protects email addresses from spam
- `jekyll-feed` - Generates Atom feed for blog posts
- `jekyll-get-json` - Fetches external JSON data (used for resume.json)
- `jekyll-imagemagick` - Generates responsive WebP images
- `jekyll-jupyter-notebook` - Converts Jupyter notebooks to blog posts
- `jekyll-link-attributes` - Adds attributes to external links
- `jekyll-minifier` - Minifies HTML and CSS
- `jekyll-paginate-v2` - Advanced pagination for posts
- `jekyll-regex-replace` - Regex replacement in Liquid templates
- `jekyll/scholar` - Manages academic publications and citations
- `jekyll-sitemap` - Generates sitemap.xml
- `jekyll-tabs` - Tabbed content support
- `jekyll-terser` - JavaScript minification with Terser
- `jekyll-toc` - Table of contents generation
- `jekyll-twitter-plugin` - Embeds tweets
- `jemoji` - GitHub-flavored emoji support

### Deployment

The site deploys automatically via GitHub Actions (`.github/workflows/deploy.yml`) when pushing to `main` or `master` branch. The workflow:

1. Builds the Jekyll site with ImageMagick support for responsive images
2. Converts Jupyter notebooks using nbconvert
3. Purges unused CSS with PurgeCSS
4. Deploys to `gh-pages` branch

**Important**: The `gh-pages` branch is auto-generated - never edit it directly. All changes must be made to the `main` branch.

### GitHub Actions Workflows

Available workflows in `.github/workflows/`:

- `deploy.yml` - Main deployment workflow (builds and deploys to GitHub Pages)
- `deploy-image.yml` - Builds and pushes Docker image to GitHub Container Registry
- `deploy-docker-tag.yml` - Tags and releases Docker images
- `docker-slim.yml` - Builds slim Docker image variant
- `update-citations.yml` - Automatically updates Google Scholar citation counts
- `update-tocs.yml` - Updates table of contents in documentation
- `prettier.yml` - Checks code formatting with Prettier
- `prettier-comment-on-pr.yml` - Comments formatting issues on PRs
- `prettier-html.yml` - Formats HTML files
- `broken-links.yml` - Checks for broken links in markdown files
- `broken-links-site.yml` - Checks for broken links in deployed site
- `lighthouse-badger.yml` - Generates Lighthouse performance badges
- `axe.yml` - Runs accessibility tests with Axe
- `codeql.yml` - Security analysis with CodeQL

## Configuration Notes

### Site Settings (\_config.yml)

**Basic Settings**:
- `url`: Base URL (https://heejyang.github.io)
- `baseurl`: Subpath (/NPClab) - required for project pages
- `title`: Site title shown in browser and header
- `email`: Contact email (protected from spam crawlers)
- `google_scholar`: Google Scholar ID for citation tracking

**Layout & Navigation**:
- `navbar_fixed: true` - Fixed navigation bar at top
- `footer_fixed: true` - Fixed footer at bottom
- `search_enabled: true` - Site-wide search functionality
- `socials_in_search: true` - Include social profiles in search
- `posts_in_search: true` - Include blog posts in search
- `bib_search: true` - Search within bibliography
- `max_width: 930px` - Maximum content width

**Publication Settings**:
- `scholar.last_name` and `scholar.first_name`: Used to highlight author name in publications (shown as **Yang, Heejung**)
- `max_author_limit: 3`: Shows first 3 authors, rest revealed on click
- `enable_publication_thumbnails: true` - Show preview images for papers
- `enable_publication_badges`: Configure badges (Altmetric, Dimensions, Google Scholar, InspireHEP)

### Jekyll Scholar

Publications are sorted by year (descending) by default. Configuration in `_config.yml`:

- `source: /_bibliography/`
- `bibliography: papers.bib`
- `bibliography_template: bib` - Uses `_layouts/bib.liquid` for rendering
- `style: apa` - Citation style
- `locale: en` - Language for citations
- `group_by: year` - Group publications by year
- `group_order: descending` - Newest first
- `bibtex_filters: [latex, smallcaps, superscript]` - Preprocessing filters
- `query: "@*"` - Include all BibTeX entry types

**Filtered BibTeX Keywords**: These fields are used internally and hidden from display:
- `abbr`, `abstract`, `additional_info`, `altmetric`, `annotation`, `arxiv`, `award`, `award_name`, `bibtex_show`, `blog`, `code`, `google_scholar_id`, `html`, `inspirehep_id`, `pdf`, `poster`, `preview`, `selected`, `slides`, `supp`, `video`, `website`

### Blog & Pagination

Blog settings in `_config.yml`:

- `blog_name: al-folio` - Blog name displayed on blog page
- `blog_description` - Blog subtitle
- `permalink: /blog/:year/:title/` - URL structure for posts
- `pagination.enabled: true` - Enable pagination
- `related_blog_posts.enabled: true` - Show related posts
- `related_blog_posts.max_related: 5` - Number of related posts to show

**External Posts**: Configure in `external_sources` to include posts from Medium or other blogs via RSS feeds or direct URLs.

### Comments

**Giscus** (recommended, configured but repo not set):
- Powered by GitHub Discussions
- Configure `giscus.repo` and `giscus.repo_id` to enable
- Supports reactions, light/dark themes
- Follow setup at https://giscus.app/

**Disqus** (deprecated):
- Legacy comment system
- Configure `disqus_shortname` if needed

### Third-Party Libraries

Managed in `_config.yml` under `third_party_libraries`. Set `download: false` to use CDN links, or `download: true` to download locally (useful for offline development).

Includes: Bootstrap Table, Chart.js, D3, ECharts, Plotly, Vega-Lite, MathJax, Mermaid, PhotoSwipe, Swiper, Leaflet, Lightbox2, Medium Zoom, and many more.

### Image Optimization

**ImageMagick Integration** (`imagemagick.enabled: true`):
- Automatically generates responsive images at multiple widths (480px, 800px, 1400px)
- Converts images to WebP format for better performance
- Processes images from `assets/img/` directory
- Supports .jpg, .jpeg, .png, .tiff, .gif formats
- **Requirement**: ImageMagick must be installed (`convert -version` to verify)

**Lazy Loading** (`lazy_loading_images: true`):
- All images use `loading="lazy"` attribute by default
- Improves initial page load performance
- Can be overridden per image with `loading=""` attribute

### Optional Features

Key feature flags in `_config.yml`:

- `enable_google_analytics: false` - Google Analytics tracking
- `enable_darkmode: true` - Light/dark theme toggle
- `enable_masonry: true` - Automatic project card arrangement
- `enable_project_categories: true` - Categorize projects
- `enable_math: true` - MathJax for LaTeX equations
- `enable_medium_zoom: true` - Image zoom on click (Medium-style)
- `enable_progressbar: true` - Scroll progress indicator
- `enable_navbar_social: false` - Social links in navbar
- `enable_tooltips: false` - Auto-generated tooltips for section titles
- `enable_video_embedding: false` - Embed videos in BibTeX entries (if false, opens in new window)

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

### Adding Photo Galleries

Create a file in `_photos/` with frontmatter:

```yaml
---
layout: page
title: Gallery 2024
year: 2024
photos:
  - url: img/photo1.jpg
    caption: "Photo caption here"
  - url: img/photo2.jpg
    caption: "Another caption"
---
Optional description text.
```

Photos use PhotoSwipe lightbox for fullscreen viewing and navigation.

### Adding Book Reviews

Create a file in `_books/` with frontmatter:

```yaml
---
layout: book-review
title: "Book Title"
author: "Author Name"
date: 2024-01-26
rating: 5
categories: [fiction, science]
---
Your book review content here.
```

Books are displayed on the book shelf page (`/books/`) with covers and ratings.

### Adding Projects

Create a file in `_projects/` with frontmatter:

```yaml
---
layout: page
title: Project Title
description: Short project description
img: assets/img/project_thumbnail.jpg
importance: 1
category: research
---
Your project content here with detailed description, images, results, etc.
```

Projects are displayed on the projects page (`/projects/`) with masonry layout if `enable_masonry: true`.

### Modifying Styles

Theme colors are in `_sass/_themes.scss` (change `--global-theme-color` variable). Other style variables are in `_sass/_variables.scss`.

## Troubleshooting

### BibTeX Changes Not Appearing
- Delete `.jekyll-cache/` directory: `rm -rf .jekyll-cache/`
- Rebuild the site: `bundle exec jekyll serve`

### Images Not Displaying or Not Responsive
- Verify ImageMagick is installed: `convert -version`
- Check that images are in `assets/img/` directory
- Ensure image paths in markdown are correct (relative to site root)
- Wait for image processing to complete (shows in build logs)

### Site Not Updating After Config Changes
- Stop Jekyll server (Ctrl+C)
- Clear cache: `rm -rf .jekyll-cache/ _site/`
- Restart: `bundle exec jekyll serve`

### Docker Issues
- Pull latest image: `docker compose pull`
- Rebuild: `docker compose up --build`
- Check port conflicts (8080 for full, 8080 for slim)

### Search Not Working
- Ensure `search_enabled: true` in `_config.yml`
- Check that `assets/js/search/*.js` files exist
- Verify search index is being generated in `_site/`

### Dark Mode Not Working
- Ensure `enable_darkmode: true` in `_config.yml`
- Check browser console for JavaScript errors
- Clear browser cache

## Important Notes

- Always test locally before pushing to main
- Changes to `_config.yml` require rebuilding the site (`bundle exec jekyll serve --livereload` for auto-reload)
- When using Docker, the site auto-reloads on file changes
- BibTeX entries are cached by Jekyll Scholar - delete `.jekyll-cache/` if changes don't appear
- ImageMagick must be installed for responsive images to work (`convert -version` to check)
- The site uses collections (news, projects, books, photos) defined in `_config.yml`
- Responsive images are generated at build time - initial build may be slower
- JavaScript is minified with Terser (not Jekyll Minifier) - see `jekyll-minifier.compress_javascript: false`
- External links automatically get `rel="external nofollow noopener"` and `target="_blank"` via `jekyll-link-attributes`
- Google Scholar citations can be auto-updated via GitHub Actions workflow (`.github/workflows/update-citations.yml`)
- PhotoSwipe is used for photo galleries, Swiper for image carousels, Lightbox2 for general lightbox needs
- The site supports Jupyter notebooks in `_posts/` - they're converted to HTML automatically
- Prettier is configured for code formatting - run `npx prettier --write .` before committing

## Project Structure Reference

Quick reference for file locations:

- Configuration: `_config.yml`
- Pages: `_pages/*.md`
- Blog posts: `_posts/YYYY-MM-DD-title.md`
- Projects: `_projects/*.md`
- Publications: `_bibliography/papers.bib`
- News: `_news/*.md`
- Photos: `_photos/*.md`
- Books: `_books/*.md`
- Layouts: `_layouts/*.liquid`
- Includes: `_includes/*.liquid`
- Plugins: `_plugins/*.rb`
- Styles: `_sass/*.scss`
- Data: `_data/*.yml`
- Resume: `assets/json/resume.json`
- Images: `assets/img/`
- PDFs: `assets/pdf/`
