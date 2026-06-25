# Project Website — IrGEMM (IEEE TPDS)

Interactive homepage for **"IrGEMM: An Input-Aware Tuning Framework for Irregular GEMM on ARM and X86 CPUs" (Wei, Jia, Zhang, Yao, Li, Cao).

Self-contained static site built from the paper's LaTeX source (no build step, no dependencies). EPS figures were rendered to PNG.

## Files
- `index.html` — single-page site
- `styles.css`, `script.js` — shared framework (light/dark, scroll reveal, lightbox, BibTeX copy)
- `assets/paper.pdf`, `assets/figs/*.png`

## View locally
Open `index.html`, or serve: `python3 -m http.server 8000` then visit http://localhost:8000

## Deploy
Drop the `website/` folder on any static host (GitHub Pages, Netlify, Vercel). Works without JavaScript.
