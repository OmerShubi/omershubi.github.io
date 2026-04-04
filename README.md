# omershubi.github.io

Personal academic website for [Omer Shubi](https://omershubi.github.io) — PhD candidate in Data Science at the Technion.

## Structure

Plain HTML + CSS, no build step required.

- `index.html` — The entire website (bio, publications, talks, media, CV)
- `stylesheet.css` — Styles (Lato font, link colors)
- `images/` — Profile photo and publication thumbnails
- `data/` — PDFs for publications and talks

## Deployment

Push to `main` triggers a GitHub Actions workflow (`.github/workflows/hugo.yml`) that deploys the root directory as a static site to GitHub Pages.

## Credits

Based on the [Jon Barron template](https://github.com/jonbarron/jonbarron.github.io), adapted from [Keren Gruteke Klein's fork](https://github.com/KerenGruteke/KerenGruteke.github.io).
