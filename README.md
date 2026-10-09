# ICCUB Claude Guide

Source of the ICCUB Claude Guide website, built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

- The site is bilingual (English at the root, Catalan under `/ca/`). Every page has an English file `page.md` and a Catalan file `page.ca.md`, and every change is made in both. See `CLAUDE.md`.
- Pages live in `docs/`. The menu is set in `mkdocs.yml` (Catalan menu titles under `nav_translations`).
- Preview locally: `pip install -r requirements.txt`, then `mkdocs serve` and open http://127.0.0.1:8000.
- Every push to `main` publishes the site to GitHub Pages (`.github/workflows/deploy.yml`).
- To add an example, copy `docs/assets/example-template.txt` to `docs/examples/<area>/<name>.md` (and its Catalan version `example-template.ca.txt` to `<name>.ca.md`), add it to `nav` in `mkdocs.yml` and to the area's `index.md`. Contributors without GitHub email their file to vmathieu@ub.edu.
