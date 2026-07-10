# SciScope Human Evaluation Web App

This folder contains a static annotation page. It does not require a backend.

## Files

- `index.html`: annotation interface.
- `data.js`: assigned items for annotators `A01`--`A10`.

## Recommended External-User Workflow

1. Send each annotator their personal link, such as `index.html?annotator=A01`.
2. The annotator rates 24 paper-path items and 6 evolution-node items.
3. For evolution-node items, the page shows evidence papers across years, so annotators can judge lifecycle/trend support.
4. The browser saves draft answers locally.
5. After all 30 items are complete, the annotator clicks `Submit` on the last item.
6. Submission downloads a JSON file and locks that annotator's local responses.
7. Collect the submitted JSON files and place them in one result folder for analysis.

## Hosting Options

- Static hosting: GitHub Pages, Netlify, Vercel, Cloudflare Pages, or any ordinary web server.
- Direct file mode: annotators can open `index.html` locally after unzipping the folder.
- Live collection mode: if automatic collection is needed, put this static page behind a small backend or Google Form endpoint. The current version intentionally avoids server-side collection, so external annotators submit by sending back the downloaded JSON file.

## Annotation Load

- 10 annotators.
- 30 items per annotator.
- 24 paper-path assignments and 6 evolution nodes per annotator.
- Each unique item is assigned to 2 annotators.
