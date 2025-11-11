
# My Website

This repository holds the source files for my personal website [omershubi.github.io](https://omershub.github.io).

The website is published with [Wowchemy](https://wowchemy.com/) and based on the [Hugo Academic Theme](https://github.com/wowchemy/starter-hugo-academic).

## Editing

* Change favicon in `assets/media/icon.png`.
* Add icons in `assets/media/icons/`.
* Update personal info in `content/authors/admin/_index.md`.
* Add pulications in `content/publication`. See upload options and specific format in the [docs](https://wowchemy.com/docs/content/publications/). Basically:

    ```bash
    conda activate academic
    academic import --bibtex data/publications.bib
    ```

    Then edit the generated files in `content/publication/` to add pdfs, links, etc.

* Update website name in `config/_default/config.yaml`.
* Update site settings, including footer in `config/_default/params.yaml`.
* For main page updates - `content/_index.md`.

Additional documentation:

* [https://wowchemy.com/docs/](https://wowchemy.com/docs/getting-started/get-started/)
* [Using the CMS](https://wowchemy.com/docs/getting-started/hugo-cms/)
