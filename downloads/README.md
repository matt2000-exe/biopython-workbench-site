# Downloads folder

This folder is no longer where the live download link points.

The site's download buttons now point at a stable GitHub Releases URL, hosted
on the app's own repo (not this site repo):

```
https://github.com/matt2000-exe/BioPythonWorkbench/releases/download/latest/BiopythonWorkbench.exe
```

That link never changes, so shipping a new build does **not** require
redeploying the Netlify site. To publish a new build, from the
`BioPythonWorkbench` project (wherever the built exe comes out):

```
gh release upload latest BiopythonWorkbench.exe --clobber --repo matt2000-exe/BioPythonWorkbench
```

`--clobber` replaces the existing asset in place.

This folder still exists as a local staging spot for the exe before you
upload it — it stays gitignored (`downloads/*.exe`) since the binary itself
never needs to go into git.
