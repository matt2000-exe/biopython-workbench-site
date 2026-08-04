# Downloads folder

This folder is no longer where the live download link points.

The site's download buttons now point at a stable GitHub Releases URL:

```
https://github.com/matt2000-exe/biopython-workbench-site/releases/download/latest/BiopythonWorkbench.exe
```

That link never changes, so shipping a new build does **not** require
redeploying the Netlify site. To publish a new build:

```
gh release upload latest downloads/BiopythonWorkbench.exe --clobber
```

(Run from the repo root, with the new `BiopythonWorkbench.exe` in this folder.
`--clobber` replaces the existing asset in place.)

This folder still exists as a local staging spot for the exe before you
upload it — it stays gitignored (`downloads/*.exe`) since the binary itself
never needs to go into git.
