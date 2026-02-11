# Custom Gotham Template (Overleaf + GitHub)

This folder is a self-contained Beamer template based on Gotham.

Use this when you want:
- one clean Overleaf project you can reuse,
- one place for your branding defaults,
- a simple repo you can push to GitHub.

## What Is Included

- `main.tex`: starter presentation.
- `gotham-personal.tex`: your customization layer (edit this first).
- `sections/`: sample section files.
- `assets/`: place your logos/backgrounds here.
- Gotham theme files:
  - `beamerthemegotham.sty`
  - `beamercolorthemegotham.sty`
  - `beamerfontthemegotham.sty`
  - `beamerinnerthemegotham.sty`
  - `beamerouterthemegotham.sty`

## Quick Start In Overleaf

1. Create a new blank project in Overleaf.
2. Upload everything from this folder.
3. Open `main.tex`.
4. (Recommended) Set compiler to XeLaTeX for best Gotham font behavior.
5. Edit `gotham-personal.tex` and metadata in `main.tex`.

## Your Main Edit File

Edit `gotham-personal.tex` to set:
- colors,
- logo paths,
- title page background/logo,
- progress bar/numbering defaults,
- section and ToC behavior.

Keep most customizations there so updates are easy.

## Branding Assets

Place files in `assets/` with these names (optional):
- `logo-square.pdf`
- `logo-circle.pdf`
- `logo-title.pdf`
- `title-bg.pdf`

If files are missing, the template still compiles.

## Publish To GitHub

Run these commands from this folder:

```bash
git init
git add .
git commit -m "Initialize custom Gotham Overleaf template"

# Option A: with GitHub CLI
gh repo create your-gotham-template --private --source=. --remote=origin --push

# Option B: manual remote
git remote add origin git@github.com:<your-user>/<your-gotham-template>.git
git branch -M main
git push -u origin main
```

## Overleaf <-> GitHub

After pushing to GitHub, in Overleaf:
- use "Import from GitHub", or
- connect an existing Overleaf project to the GitHub repo.

This gives you version history and repeatable template reuse.
