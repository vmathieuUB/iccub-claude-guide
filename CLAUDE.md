# Working on the ICCUB Claude Guide

## Rule: every change is made in English and Catalan

The site is bilingual. English is the working language and the default (served at the site root); Catalan is served under `/ca/`.

- Every page exists twice, side by side: `page.md` (English) and `page.ca.md` (Catalan).
- Any change to one language (adding, editing, moving or deleting a page or a paragraph) is made in the other language in the same commit. This applies in both directions.
- A new page also needs its menu entry in `nav` in `mkdocs.yml`, and its Catalan menu title under `nav_translations` in the `i18n` plugin section.
- Downloadable files follow the same pattern: `docs/assets/example-template.txt` and `docs/assets/example-template.ca.txt`.
- Keep link targets identical in both files (e.g. `../getting-started/data-and-privacy.md`); the build points Catalan pages to Catalan targets automatically.

## Catalan style

- Standard central Catalan, addressing the reader with "tu".
- Product, feature and button names stay in English as they appear in the Claude interface (Projects, Artifacts, Claude Code, **Settings → Connectors**).
- Prompts to type to Claude are translated into Catalan; code, commands, paths and URLs are not.
- Tags: Research → Recerca, Teaching → Docència, Outreach → Divulgació, Admin → Gestió, Writing → Redacció, Coding → Programació, Local models → Models locals, Chat → Xat, Email → Correu electrònic, Calendar → Calendari. Feature names stay in English.

## Build

`pip install -r requirements.txt`, then `mkdocs serve`. A push to `main` publishes the site.
