# Console Craft — website

A single-page static site for Console Craft, ready for GitHub Pages. No build step — it's plain HTML/CSS/JS.

## Files

```
index.html      the whole page
styles.css      all styling
script.js       small scroll-reveal effect, no dependencies
images/         optimized .webp screenshots used on the page
```

## Go live on GitHub Pages tonight

**Option A — new repo dedicated to the site**
1. Create a repo (e.g. `console-craft-site`) on GitHub.
2. Push these files to the `main` branch, at the repo root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
5. Save. GitHub gives you a URL like `https://<your-username>.github.io/console-craft-site/` within a minute or two.

**Option B — same repo as the app, docs folder**
1. Put these files inside a `/docs` folder in your existing Console Craft repo.
2. **Settings → Pages** → Source: `Deploy from a branch`, branch `main`, folder `/docs`.
3. Save.

**Option C — GitHub organization/user page**
If the repo is named `<your-username>.github.io`, push these files to `main` at the root and Pages serves it at `https://<your-username>.github.io/` automatically, no settings change needed.

## Before you publish

Two placeholders need real URLs — search `index.html` for these two lines near the bottom (`id="github-link"` and `id="releases-link"`) and swap the `href="#"` for:
- your GitHub repo URL
- your latest release / download URL (or point it at the repo's Releases page if there's no packaged build yet)

Everything else — copy, screenshots, styling — is ready as-is.

## Local preview

Any static server works, e.g.:
```
cd site
python3 -m http.server 8000
```
then open `http://localhost:8000`.
