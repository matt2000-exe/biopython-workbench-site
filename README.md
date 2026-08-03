# Biopython Workbench — website

Static marketing/download site: plain HTML/CSS/JS, no build step, no framework.

```
index.html
css/style.css
js/script.js
assets/favicon.svg
downloads/            <- put the packaged BiopythonWorkbench.exe here
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

## Before publishing

Replace the placeholder in `downloads/` with the real PyInstaller-built
`BiopythonWorkbench.exe`. The download buttons already point at
`downloads/BiopythonWorkbench.exe`.
