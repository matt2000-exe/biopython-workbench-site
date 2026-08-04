# Biopython Workbench — website

Static marketing/download site: plain HTML/CSS/JS, no build step, no framework.

```
index.html
css/style.css
js/script.js
assets/favicon.svg
downloads/            <- local staging spot for BiopythonWorkbench.exe before release upload
```

## Running it in VS Code

Two options — pick whichever you already have:

**Option A — Live Server extension (recommended, has auto-reload)**
1. Install the "Live Server" extension (VS Code will prompt you via the
   `.vscode/extensions.json` recommendation when you open this folder).
2. Right-click `index.html` → "Open with Live Server", or click "Go Live"
   in the bottom status bar.

**Option B — npm script (no extension needed, Node is already on this machine)**
1. Terminal → Run Task... → "Serve site (npm)", or just run:
   ```
   npm start
   ```
2. Open http://localhost:5500 in a browser.

## Shipping a new build of the app

The download buttons point at a stable GitHub Releases URL, not a file in
this repo, so a new build does **not** require touching the Netlify site:

```
gh release upload latest downloads/BiopythonWorkbench.exe --clobber
```

Only push/redeploy the site itself when the HTML/CSS/JS changes. See
`downloads/README.md` for details.
