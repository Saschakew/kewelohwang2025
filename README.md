# kewelohwang2025

Frozen static deployment of the Keweloh-Wang 2025 SVAR visualizer.

This repository was split out from `Saschakew/Illustrations`, folder `visualization6`, so the production subdomain can be hosted on GitHub Pages without the AWS EC2/Nginx server.

## Hosting

- Public domain: `https://kewelohwang2025.sascha-keweloh.com/`
- GitHub Pages source: `.github/workflows/deploy.yml`
- Build step: none
- Deployed artifact: repository root
- Custom domain file: `CNAME`

The site is plain static HTML/CSS/JS: `index.html`, `public/css`, `public/js`, and `public/sections`.

## Local Preview

From the repository root:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000/`.

## DNS Migration

When ready to move production traffic from AWS to GitHub Pages, replace the Route 53 record for `kewelohwang2025.sascha-keweloh.com` with a CNAME pointing to:

```text
saschakew.github.io
```

Do not terminate the AWS EC2 instance until DNS and HTTPS have been verified against GitHub Pages.