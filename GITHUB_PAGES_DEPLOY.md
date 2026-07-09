# GitHub Pages Deployment

This folder can be deployed directly as a GitHub Pages static site.

## Option A: Web Upload

1. Create a GitHub repository, for example `sciscope-human-eval`.
2. Upload all files in this folder to the repository root:
   - `index.html`
   - `data.js`
   - `.nojekyll`
   - `README.md`
3. Open repository settings.
4. Go to `Pages`.
5. Set source to `Deploy from a branch`.
6. Select branch `main` and folder `/root`.
7. Wait for GitHub Pages to publish the site.

Then send annotators links such as:

```text
https://<user-or-org>.github.io/sciscope-human-eval/index.html?annotator=A01
https://<user-or-org>.github.io/sciscope-human-eval/index.html?annotator=A02
...
https://<user-or-org>.github.io/sciscope-human-eval/index.html?annotator=A10
```

## Option B: Command Line

```bash
cd human_eval_web_20260709
git init
git add index.html data.js .nojekyll README.md GITHUB_PAGES_DEPLOY.md
git commit -m "Add SciScope human evaluation web app"
git branch -M main
git remote add origin git@github.com:<user-or-org>/sciscope-human-eval.git
git push -u origin main
```

Then enable GitHub Pages in repository settings.

## Privacy Note

This static app contains paper titles, topic paths, node definitions, and annotator
assignment ids. It does not contain API keys or private credentials. If you use a
public GitHub Pages repository, anyone with the URL can view the annotation items.
For stricter access control, use a private repository with GitHub Pages support,
Netlify password protection, Cloudflare Access, or a small authenticated server.
