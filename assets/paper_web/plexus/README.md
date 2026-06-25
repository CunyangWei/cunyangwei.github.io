# Project Website — Plexus

Interactive homepage for **"Plexus: Taming Billion-edge Graphs with 3D Parallel Full-graph GNN Training" (Ranjan, Singh, Wei, Bhatele).

Self-contained static site built from the paper's LaTeX source (no build step, no dependencies).

## Files
- `index.html` — single-page site
- `styles.css`, `script.js` — shared framework (light/dark, scroll reveal, lightbox, BibTeX copy)
- `assets/paper.pdf` and `assets/figs/*.png` — paper and figures (PDF figures rendered to PNG)

## View locally
Open `index.html`, or serve: `python3 -m http.server 8000` then visit http://localhost:8000

## Deploy
Drop the `website/` folder on any static host (GitHub Pages, Netlify, Vercel). Works without JavaScript.
