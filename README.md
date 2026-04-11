# Intersections Reference Checker

A single-file, browser-based bibliographic reference checker for the Intersections journal editorial team. Paste a reference list, click Check, and the tool verifies each entry against CrossRef, OpenAlex, Semantic Scholar, Open Library, Google Books, and arXiv.

## Live version

Once GitHub Pages is enabled, the tool runs at:

`https://<your-github-username>.github.io/<repo-name>/`

No installation, no login, no backend — just open the URL in a browser.

## Supported citation styles

- OSCOLA (legal citation, including book and chapter forms)
- APA / Harvard author–date (with quoted, single-quoted, and unquoted titles)
- Chicago author–date and Chicago notes-bibliography
- MLA
- Mixed lists are handled automatically

## What it checks

For each parsed reference the checker queries multiple academic databases and reports:

- **Verified** — record found, author/title/year all match
- **Similar with discrepancies** — record found but something differs (year, authors, etc.)
- **Uncertain** — no matching record located in any database

## How to update

1. Edit `index.html` locally.
2. `git add index.html && git commit -m "describe change"`
3. `git push`

Within ~1 minute the live URL serves the new version. Tell colleagues to hard-reload (Ctrl+Shift+R / Cmd+Shift+R) if they have an old version cached.

## Tech notes

- Pure single-file HTML + vanilla JavaScript. No build step, no framework, no server.
- All API calls run client-side from the user's browser. CORS-friendly endpoints only.
- No API keys, no authentication, no tracking.
- Tested in current Chrome, Firefox, Safari, and Edge.
