# Hack Chalmers

Website for **Hack Chalmers** — a 24-hour hackathon at Chalmers in Gothenburg, October 3–4, 2026.
Registration lives on Luma: https://luma.com/a1irv5xj

Static site, no build step. Open `index.html` in a browser to preview.

```
index.html    the page
styles.css    all styling, including the gradients
favicon.svg   gradient square
og-cover.jpg  social preview image
```

## Editing

- All copy is in `index.html`.
- Colors live in the `:root` block at the top of `styles.css` (`--g-blue`, `--g-cyan`, …).
  The gradient classes `.grad-a` through `.grad-e` are built from those and are reused
  everywhere the site would otherwise use an image.
- Prizes are currently `TBA` in the "Judging & prizes" section — replace that text when known.

## Deploying to GitHub Pages

```sh
git init
git add .
git commit -m "Hack Chalmers site"
gh repo create hack-chalmers --public --source=. --push
```

Then in the repo: **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**.
The site goes live at `https://<user>.github.io/hack-chalmers/`.

For a custom domain, add a file named `CNAME` containing just the domain
(e.g. `hackchalmers.se`), push it, and point the domain's DNS at GitHub Pages.
