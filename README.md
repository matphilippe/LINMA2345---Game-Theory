# LINMA2345 - Game Theory

This repository hosts source files for the
[LINMA2345 - Game Theory](https://uclouvain.be/en-cours-2021-linma2345) class
tought at the Université Catholique de Louvain.

## Tooling

We want onboarding to be as smooth as possible.
For this reason, we favor the usage of containers for the different actions
related to this repo, be them about linting, building the notes, etc...

## How-tos

In order to build a document, `cd` to the directory containing it's main `.tex` file, and build it.

For instance, the following command builds the course notes under `notes/LINMA2345-notes.pdf`: 

```bash
docker run -v $(pwd):/sources -w /sources/notes texlive/texlive:latest pdflatex LINMA2345-notes.tex
```

For another example, the following builds the exercises notes for the first practice session at `exercises/APE1/APE1-introduction.pdf`. 

```bash
docker run -v $(pwd):/sources -w /sources/exercises/APE1 texlive/texlive:latest pdflatex APE1-introduction.tex
```
