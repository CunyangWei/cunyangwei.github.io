# Project Website

Interactive homepage for **"The Case of the Elusive Application Performance on Production GPU Supercomputers"** (Wei, Pradeep, Bhatele — IPDPS 2026).

Built directly from the paper's LaTeX source as a self-contained static site (no build step, no dependencies).

## Files

```
website/
├── index.html        # Single-page site
├── styles.css        # Styling (light/dark themes, responsive)
├── script.js         # Theme toggle, scroll reveal, lightbox, BibTeX copy
└── assets/
    ├── paper.pdf     # Full paper
    └── figs/         # All figures (PNG)
```

## View locally

Just open `index.html` in a browser, or serve the folder:

```bash
cd website
python3 -m http.server 8000
# visit http://localhost:8000
```

## Features

- Responsive layout with sticky nav and reading-progress bar
- Light / dark mode (respects system preference, remembers choice)
- Click any figure to zoom (lightbox)
- All six paper "Takeaway" boxes, contributions, machine specs, and the workload table
- One-click BibTeX copy
- Works without JavaScript (content remains fully visible)

## Deploy

Drop the `website/` folder on any static host — GitHub Pages, Netlify, Vercel, or a university web server. For GitHub Pages, push the folder and point Pages at it (no configuration needed since it's plain HTML/CSS/JS).
