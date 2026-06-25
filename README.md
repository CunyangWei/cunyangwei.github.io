# cunyangwei.github.io

Personal academic website of **Cunyang Wei**, Ph.D. student at the University of
Maryland, College Park. Built with [Jekyll](https://jekyllrb.com/) and the
[al-folio](https://github.com/alshedivat/al-folio) theme (v1.x).

Live site: https://cunyangwei.github.io

## Local development

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Content

- Bio: `_pages/about.md` (profile photo: `assets/img/prof_pic.png`)
- Publications: `_bibliography/papers.bib` (PDFs in `assets/pdf/`)
- News: `_news/`
- CV: `_data/cv.yml` and `_pages/cv.md` (PDF at `assets/pdf/CV_Cunyang_Wei.pdf`)
- Social links: `_data/socials.yml`

## Deployment

Pushes to `master` are built and deployed to the `gh-pages` branch by
`.github/workflows/deploy.yml`. Configure GitHub Pages (Settings → Pages) to serve
from the **gh-pages** branch.

## Credits

Theme: [al-folio](https://github.com/alshedivat/al-folio) (MIT License).
