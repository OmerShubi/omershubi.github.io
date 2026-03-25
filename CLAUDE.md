# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Rules

- When encountering author names that use only a first initial (e.g., "C. A. Hadar", "K. Gruteke Klein"), always ask the user for the full first name. Do not guess or assume what the initial stands for.

## Build & Dev Commands

- **Local dev server:** `hugo server --buildDrafts --disableFastRender` (port 1313)
- **Production build:** `hugo --gc --minify`
- **Update theme modules:** `hugo mod get -u ./... && hugo mod tidy`

## Architecture

Hugo academic website using the **Wowchemy Academic theme v5** (via Go modules). Deployed to **GitHub Pages** via GitHub Actions (`.github/workflows/hugo.yml`).

### Key Files

- `config/_default/config.yaml` — Hugo config, module imports, permalinks
- `config/_default/params.yaml` — Theme appearance, SEO, features, footer
- `config/_default/menus.yaml` — Navigation menu items
- `content/_index.md` — **Homepage layout**: defines all homepage sections (About, Experience, Featured Publications, Talks, Recent Publications, Contact) as Wowchemy widget blocks. Experience entries are inline YAML here, not separate files.
- `content/authors/admin/_index.md` — Author profile (bio, interests, education, social links). `admin` is the key used to reference "Omer Shubi" in publication author lists.
- `layouts/_default/baseof.html` — Local override of Wowchemy's baseof.html to fix `.File.UniqueID` bug for Hugo 0.123+ compatibility. Do not remove.
- `layouts/partials/analytics/google_analytics.html` — Override for Hugo 0.120+ deprecation of `.Site.GoogleAnalytics`.

### Content Types

- **Publications** (`content/publication/<slug>/index.md`): Use `publication_types: ["1"]` for conference papers, `["2"]` for journal articles. Use `admin` for Omer Shubi in the `authors` list. Set `featured: true` for papers to appear in the Featured Publications homepage section. Use `author_notes: ["Equal contribution", "Equal contribution"]` for shared first-authorship (marked with * in papers).
- **Events/Talks** (`content/event/<slug>/index.md`): Rendered at `/talk/<slug>/` (see permalinks config).
- **Author profiles** (`content/authors/<name>/_index.md`): `admin` is the primary author.

### Deployment

Push to `main` triggers GitHub Actions which runs `hugo mod get -u ./...` (auto-updates modules), builds with Hugo extended 0.152.2, and deploys to GitHub Pages. The `netlify.toml` is legacy and unused.
