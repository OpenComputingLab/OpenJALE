# OpenJALE
Open Jupyter Authoring and Learning Environment

Book site: https://opencomputinglab.github.io/OpenJALE/philosophy.html

Book site generated using a manually triggered Github action to createe the book files from a single `index.Rmd` document.

The `index.Rmd` document is  currently generated from a single markdown document using a manually run `jupytext` command on host:

```
jupytext --to Rmd --output index.Rmd example.md 
```
