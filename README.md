# Biopython Workbench — website

Static marketing/download site: plain HTML/CSS/JS, no build step, no framework.

```
index.html
css/style.css
js/script.js
assets/favicon.svg
downloads/            <- just README.md; exe + sample data are hosted on GitHub Releases
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

## Shipping a new build or sample data update

The download buttons (exe and sample data) all point at stable GitHub
Releases URLs hosted on the
[BioPythonWorkbench](https://github.com/matt2000-exe/BioPythonWorkbench) app
repo, not this site repo — so updating either does **not** require touching
the Netlify site:

```
gh release upload latest BiopythonWorkbench.exe --clobber --repo matt2000-exe/BioPythonWorkbench
gh release upload latest data/_ncbi_example_sequences.fasta data/_ncbi_example_pbr322.gb --clobber --repo matt2000-exe/BioPythonWorkbench
```

Only push/redeploy the site itself when the HTML/CSS/JS changes, or when a
sample file's name/content changes enough that the description text on the
Downloads section needs updating. See `downloads/README.md` for details.
