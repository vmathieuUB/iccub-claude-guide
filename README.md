# ICCUB Claude Guide

Source of the ICCUB Claude Guide website, built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

- Pages live in `docs/`. The menu is set in `mkdocs.yml`.
- Preview locally: `pip install -r requirements.txt`, then `mkdocs serve` and open http://127.0.0.1:8000.
- Every push to `main` publishes the site to GitHub Pages (`.github/workflows/deploy.yml`).
- To add an example, copy `docs/contribute/example-template.md` into `docs/examples/<area>/` and add it to `nav` in `mkdocs.yml`.
