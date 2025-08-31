# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an academic personal website built with Jekyll and the Academic Pages theme, forked from Minimal Mistakes. The site is hosted on GitHub Pages and serves as a portfolio for Cunyang Wei, showcasing publications, talks, teaching, and CV information.

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll liveserve

# Clean the site
bundle clean
```

### JavaScript Build (if needed)
```bash
# Install npm dependencies
npm install

# Build minified JavaScript
npm run build:js

# Watch JavaScript files for changes
npm run watch:js
```

## Site Architecture

### Content Collections
- **`_publications/`** - Research publications (markdown files)
- **`_talks/`** - Conference talks and presentations 
- **`_teaching/`** - Teaching experience entries
- **`_posts/`** - Blog posts
- **`_portfolio/`** - Project portfolio items
- **`_pages/`** - Static pages (About, CV, etc.)

### Key Configuration Files
- **`_config.yml`** - Main Jekyll configuration and site metadata
- **`_config.dev.yml`** - Development-specific overrides
- **`_data/navigation.yml`** - Site navigation structure
- **`_data/authors.yml`** - Author information

### Layout System
- **`_layouts/`** - Page templates (single, archive, talk, etc.)
- **`_includes/`** - Reusable template components
- **`_sass/`** - Stylesheets organized by component

### Content Generation
- **`markdown_generator/`** - Jupyter notebooks and Python scripts to generate markdown files from TSV data
  - `publications.ipynb` - Generate publication pages from `publications.tsv`
  - `talks.ipynb` - Generate talk pages from `talks.tsv`
  - Run notebooks to batch-create content from structured data

### Static Assets
- **`files/`** - PDFs and documents (CV, papers)
- **`images/`** - Profile photos and site images
- **`assets/`** - CSS, JavaScript, and font files

## Content Management

### Adding Publications
1. Add entry to `markdown_generator/publications.tsv`
2. Run `publications.ipynb` to generate markdown files
3. Or manually create markdown file in `_publications/`

### Adding Talks
1. Add entry to `markdown_generator/talks.tsv` 
2. Run `talks.ipynb` to generate markdown files
3. Or manually create markdown file in `_talks/`

### Updating Profile
- Edit author information in `_config.yml` (lines 84-119)
- Replace profile image in `images/` directory
- Update CV PDF in `files/` directory

## GitHub Pages Deployment

The site auto-deploys to GitHub Pages on pushes to master branch. Local development uses `bundle exec jekyll liveserve` for testing changes before deployment.

## File Organization Notes

- Jekyll collections output individual pages for publications, talks, teaching, and portfolio items
- The `talkmap/` directory contains geographic visualization of talks
- Static comments are handled via Staticman configuration
- Site excludes development files like `node_modules`, `Gemfile`, etc. from builds