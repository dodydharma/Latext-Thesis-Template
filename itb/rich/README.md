# Thesis Template

A LaTeX template for a PhD / Master's thesis, adapted from a University of
Leeds thesis and generalised for reuse.

## What you are looking at

This folder is **one** of six ready-to-use variants. They differ in two ways:

- **Branding:** `generic`, `leeds`, or `itb`
- **Detail level:** `rich` (worked, commented examples) or `minimal` (empty stubs)

See the `README.md` at the top of `thesis-template/` for the full picture and
help choosing. To tell which edition you have, open `main.tex` — the header
comment names it.

## Quick start

1. **Set your details.** Edit `thesis-metadata.tex` (title, author,
   supervisors, degree, university, school) and drop your institution's logo
   into `assets/` (the title page expects `assets/logo.png`).
2. **Write.** Replace the placeholder text in `sections/` with your content.
   Each chapter lives in `sections/chapterN/`. Long chapters can be split into
   several files and pulled in with `\input{...}` (see Chapter 2 in the *rich*
   edition for an example).
3. **Cite.** Add your sources to `references.bib`, then cite them with
   `\citep{key}` or `\citet{key}`.
4. **Figures.** Put image files in `figures/` and include them with
   `\includegraphics`.

## Compiling

### On Overleaf (easiest)
Upload this folder (or the whole repo), open `main.tex`, and use
**Menu → Main document → main.tex**. Press **Recompile**. Overleaf runs BibTeX
automatically.

### Locally
You need a TeX distribution (TeX Live, MiKTeX, or MacTeX). The bibliography
needs the classic four-step build:

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

Or, much simpler, use `latexmk`:

```
latexmk -pdf main.tex
```

## Folder layout

```
.
├── main.tex             # master file: preamble + document structure
├── thesis-metadata.tex  # <-- edit your title/author/etc. here
├── references.bib       # your bibliography database
├── assets/              # logo and other fixed images (logo.png)
├── figures/             # figures referenced from the text
└── sections/
    ├── declaration.tex
    ├── abstract.tex
    ├── acknowledgements.tex
    ├── appendixA.tex
    └── chapter1 ... chapter6/_index.tex
```

## Notes

- Check your university's regulations for the **exact** declaration wording,
  required **line spacing**, **margins**, and **title-page layout**, then adjust
  `main.tex`, `thesis-metadata.tex`, and `sections/declaration.tex` accordingly.
- The `\usepackage{lipsum}` lines and `\lipsum[..]` commands only generate dummy
  text. Remove them as you write real content.
