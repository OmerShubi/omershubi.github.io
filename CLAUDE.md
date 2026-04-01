# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Rules

- When encountering author names that use only a first initial (e.g., "C. A. Hadar", "K. Gruteke Klein"), always ask the user for the full first name. Do not guess or assume what the initial stands for.

## Architecture

Plain HTML + CSS personal academic website based on the [Jon Barron template](https://github.com/jonbarron/jonbarron.github.io), adapted from [Keren Gruteke Klein's fork](https://github.com/KerenGruteke/KerenGruteke.github.io). Deployed to **GitHub Pages** via GitHub Actions (`.github/workflows/hugo.yml`).

No build step required — the site is a single `index.html` file with a `stylesheet.css`.

### Key Files

- `index.html` — The entire website (single page: bio, publications, talks, media, CV)
- `stylesheet.css` — Lato font, link colors (#1772d0 blue, #f09228 orange hover)
- `images/` — Profile photo and publication thumbnails
- `data/` — Local PDFs for publications and talks
- `googled98bb8c924bffabb.html` — Google Search Console verification
- `.github/workflows/hugo.yml` — GitHub Actions workflow for static site deployment

### Content Sections (in index.html)

1. **Header** — Name, bio, social links (Scholar, GitHub, LinkedIn, ORCID), profile photo
2. **Publications** — All papers with titles, authors, venues, links, abstracts, and BibTeX citations. Featured papers have yellow background (`bgcolor="#ffffd0"`). Equal contributions marked with asterisk (*).
3. **Talks & Presentations** — Bulleted list of conference talks and tutorials
4. **Media Coverage** — Press mentions
5. **Bio** — Education, Awards, Industry Experience, Teaching

### Adding a New Publication

Add a new `<tr>` row in the publications `<table>` in `index.html`. Follow the existing pattern:
- Image in left column (20% width), content in right column (80%)
- Use `<strong>Omer Shubi</strong>` for self-citation (bold)
- Use `bgcolor="#ffffd0"` on `<tr>` for featured/highlighted papers
- Add BibTeX in a hidden `<div>` with `showCite`/`hideCite` toggle

### Deployment

Push to `main` triggers GitHub Actions which deploys the root directory as a static site to GitHub Pages. No build step needed.
