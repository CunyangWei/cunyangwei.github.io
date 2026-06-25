# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Overview

Personal academic website of **Cunyang Wei**, built with Jekyll and the
[al-folio](https://github.com/alshedivat/al-folio) theme (v1.x, gem-based).
Hosted on GitHub Pages at https://cunyangwei.github.io.

al-folio v1 is a **thin Jekyll starter**: all layouts, includes, Sass, tags, and
feature JS live in published `al_*` / `al_folio_*` gems (see `Gemfile`). This repo
owns only configuration and content. Do **not** add `_layouts/`, `_includes/`, or
`_sass/` here unless intentionally overriding a gem-owned file.

## Where content lives

- `_pages/about.md` — home page bio, profile photo (`assets/img/prof_pic.png`)
- `_bibliography/papers.bib` — publications (rendered on the Publications page via
  jekyll-scholar). Mark `selected={true}` to feature a paper on the home page.
  PDFs referenced by `pdf = {file.pdf}` live in `assets/pdf/`.
- `_news/*.md` — short "news" items shown on the home page
- `_data/cv.yml` + `_pages/cv.md` — CV page (RenderCV format); `cv_pdf` points to
  `assets/pdf/CV_Cunyang_Wei.pdf`
- `_data/socials.yml` — email, Google Scholar, ORCID, LinkedIn, CV link
- `_projects/`, `_posts/` — currently empty; Projects/Blog pages are placeholders

## Local development

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000  (baseurl is empty)
```

## Deployment

Pushing to `master` triggers `.github/workflows/deploy.yml`, which builds the site
and publishes `_site/` to the `gh-pages` branch. **GitHub Pages must be configured
to serve from the `gh-pages` branch** (Settings → Pages → Source). Native
GitHub-Pages Jekyll builds will not work because the site uses custom plugins.

## Key config

- `_config.yml`: `url: https://cunyangwei.github.io`, `baseurl: ""` (user page),
  `theme: al_folio_core`, `scholar.last_name/first_name` set to highlight the author.
