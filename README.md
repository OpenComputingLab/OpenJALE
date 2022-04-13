# OpenJALE
__Open Jupyter Authoring and Learning Environment (Classic Notebook Edition)__

Book site: https://opencomputinglab.github.io/OpenJALE/


## Publishing Route

Book site generated using a manually triggered Github action to createe the book files from a single `index.Rmd` document.

The `index.Rmd` document is  currently generated from a single markdown document using a manually run `jupytext` command on host:

```
jupytext --to Rmd --output index.Rmd example.md 
```

We can make a very hacky, hardwired automation route to run this command and commit the generated `index.Rmd` file using `.git/hooks/pre-commit` file of the form:

```
#!/bin/bash
jupytext --to Rmd --output index.Rmd  example.md
git add index.Rmd
```

(You also need to check the file is executable: `chmod u+x .git/hooks/pre-commit`.)

Making any commit to the repo will run the Jupytext command and stage any updates to the Rmd file as part of the commit.
