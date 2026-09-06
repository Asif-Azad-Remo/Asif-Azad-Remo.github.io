# Asif-Azad-Remo.github.io

Personal portfolio website of **Asif Azad Remo** — Civil &amp; Environmental
Engineer (Disaster Risk Reduction, GIS &amp; Remote Sensing, Construction QA/QC).

A static site: a single `index.html` with a downloadable CV, published to
GitHub Pages via GitHub Actions.

- **Live site:** https://asif-azad-remo.github.io/
- **CV:** `Asif_Azad_Remo_CV.pdf`

## Deploy

Open this folder in VS Code and tell **Claude Code**: `Deploy it`
(see `CLAUDE.md` for what it does).

Or deploy manually:

```bash
git init
git add -A
git commit -m "Deploy portfolio site"
git branch -M main
git remote add origin https://github.com/Asif-Azad-Remo/Asif-Azad-Remo.github.io.git
git push -u origin main
```

Pushing to `main` triggers `.github/workflows/deploy.yml`, which publishes the
site to GitHub Pages.

## Structure

```
.
├── index.html                 # the portfolio
├── Asif_Azad_Remo_CV.pdf      # downloadable CV (linked from the site)
├── .github/workflows/deploy.yml
├── CLAUDE.md                  # deploy instructions for Claude Code
└── README.md
```
