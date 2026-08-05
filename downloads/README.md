# Downloads folder

This folder is no longer where the live download links point. Everything
downloadable — the exe and the sample data — is hosted as assets on the
`latest` GitHub Release of the app's own repo (not this site repo):

```
https://github.com/matt2000-exe/BioPythonWorkbench/releases/download/latest/BiopythonWorkbench.exe
https://github.com/matt2000-exe/BioPythonWorkbench/releases/download/latest/_ncbi_example_sequences.fasta
https://github.com/matt2000-exe/BioPythonWorkbench/releases/download/latest/_ncbi_example_pbr322.gb
```

Those links never change, so shipping a new build or updated sample data
does **not** require redeploying the Netlify site. To publish an update,
from the `BioPythonWorkbench` project:

```
gh release upload latest BiopythonWorkbench.exe --clobber --repo matt2000-exe/BioPythonWorkbench
gh release upload latest data/_ncbi_example_sequences.fasta data/_ncbi_example_pbr322.gb --clobber --repo matt2000-exe/BioPythonWorkbench
```

`--clobber` replaces the existing asset in place.

Only touch the site (and redeploy to Netlify) if the sample data's
filenames change, or if the description text on the Downloads section
needs updating to match what's actually in the files.
