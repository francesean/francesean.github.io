# afrancese.com

Source of my personal website, [www.afrancese.com](https://www.afrancese.com).

The site is built with [Quarto](https://quarto.org/) and rendered to static HTML.

## Structure

```
_quarto.yml              site configuration (navbar, footer, theme)
_brand.yml               fonts and colours
index.qmd                home / about page
research/index.qmd       list of papers (auto-generated from the folders below)
research/working-papers/<paper>/index.qmd
html/theme.scss          custom styles
html/research/           listing template and title block for paper pages
assets/                  images
```

## Local preview

```bash
quarto preview
```

## Adding a paper

Create `research/working-papers/<slug>/index.qmd` with the front matter used in
`research/working-papers/family-firms/index.qmd` and it will appear on the
Research page automatically.

## Deployment

Every push to `main` renders the site with GitHub Actions and publishes it to
GitHub Pages (see `.github/workflows/publish.yml`). In the repository settings,
set *Pages → Build and deployment → Source* to **GitHub Actions**.
