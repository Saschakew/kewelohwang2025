# kewelohwang2025 Codex Notes

This repo is a frozen static copy of `Saschakew/Illustrations/visualization6` for GitHub Pages hosting.

## Rules

- Keep the site static. Do not add Flask, Node server code, databases, or runtime hosting assumptions.
- There is no build step. GitHub Pages deploys the repository root through `.github/workflows/deploy.yml`.
- Preserve `CNAME` with exactly `kewelohwang2025.sascha-keweloh.com` unless intentionally changing the production domain.
- Preserve `.nojekyll` so GitHub Pages serves static assets without Jekyll processing.
- Runtime files are `index.html`, `public/css`, `public/js`, and `public/sections`.
- Use relative asset paths that work from the domain root.
- The Route 53 DNS change is manual; do not change AWS or Route 53 from code unless the user explicitly asks.

## Validation

Recommended checks after changes:

```powershell
python -m http.server 8000
curl.exe -I http://localhost:8000/
curl.exe -I http://localhost:8000/public/css/style.css
curl.exe -I http://localhost:8000/public/js/main.js
```

For production after DNS migration, verify `Server: GitHub.com` for the root page and representative assets.