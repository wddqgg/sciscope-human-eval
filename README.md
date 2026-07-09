# SciScope Human Evaluation Web App

This folder contains a static annotation page. It does not require a backend.

## Files

- `index.html`: annotation interface.
- `data.js`: assigned items for annotators `A01`--`A10`.

## Recommended External-User Workflow

1. Send each annotator their annotator id, such as `A01`.
2. Host this folder on any static file host, or send the folder directly.
3. Ask annotators to open `index.html` and select their annotator id.
4. The browser saves draft answers locally.
5. After finishing all 30 items, annotators click `Export JSON` or `Export CSV`.
6. Collect the exported files and place them in one result folder for analysis.

## Hosting Options

- Static hosting: GitHub Pages, Netlify, Vercel, Cloudflare Pages, or any ordinary web server.
- Direct file mode: annotators can open `index.html` locally after unzipping the folder.
- Live collection mode: if automatic collection is needed, put this static page behind a small backend or Google Form endpoint. The current version intentionally avoids server-side collection so external annotators do not need access to the lab intranet.

## Annotation Load

- 10 annotators.
- 30 items per annotator.
- 24 paper-path assignments and 6 evolution nodes per annotator.
- Each unique item is assigned to 2 annotators.
