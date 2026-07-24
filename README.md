# Rosewood Key

Source for rosewoodkey.com, built with Hugo.

## Structure
- `content/_index.md` — homepage front matter
- `layouts/` — custom layouts (no theme), mirrors alexkasper.com's approach
- `data/brands.yaml` — brand cards on the homepage; add an entry here to list a new brand
- `static/` — logo and stylesheet
- `.github/workflows/hugo.yml` — builds and deploys to GitHub Pages on push to `main`

## Local development
```
hugo server
```

## Deploying
1. Push this repo to GitHub as `rosewoodkey.com` (or any name).
2. In repo Settings → Pages, set Source to "GitHub Actions".
3. Push to `main` — the workflow builds and publishes automatically.
4. Point the `rosewoodkey.com` DNS at GitHub Pages and set the custom domain in repo Settings → Pages (this also needs a `static/CNAME` file containing `rosewoodkey.com`).

## Adding a brand later
Add a new entry to `data/brands.yaml`:
```yaml
- name: "Kasper Academy"
  url: "https://kasper.academy"
  tagline: "..."
  description: "..."
```
