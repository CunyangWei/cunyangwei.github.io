# Project Website — IATF (ICPP 2022)

Interactive homepage for **"IATF: An Input-Aware Tuning Framework for Compact BLAS Based on ARMv8 CPUs"** (Wei, Jia, Zhang, Xu, Qi — ICPP '22).

Self-contained static site built from the paper's LaTeX source (no build step, no dependencies). EPS figures were rendered to PNG.

## Files
- `index.html` — single-page site
- `styles.css`, `script.js` — shared framework (light/dark, scroll reveal, lightbox, BibTeX copy)
- `assets/paper.pdf`, `assets/figs/*.png`

## View locally
Open `index.html`, or serve: `python3 -m http.server 8000` then visit http://localhost:8000

## Deploy
Drop the `website/` folder on any static host (GitHub Pages, Netlify, Vercel). Works without JavaScript.
