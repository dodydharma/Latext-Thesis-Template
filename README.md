# Thesis LaTeX Template

A reusable LaTeX template for a PhD / Master's thesis, adapted from the thesis
*Neural Network-Based Surrogate Models of Lagrangian Continuum Simulators*
(Dody Dharma, University of Leeds) and generalised so students can use it for
their own writing.

## Pick a variant

This folder contains **six** ready-to-use copies of the template. Choose one,
copy that folder, and start writing — each copy is fully self-contained and
compiles on its own.

The copies vary along two axes:

|                     | **rich** (worked examples) | **minimal** (empty stubs) |
|---------------------|----------------------------|---------------------------|
| **generic** branding | `generic/rich/`           | `generic/minimal/`        |
| **Leeds** branding   | `leeds/rich/`             | `leeds/minimal/`          |
| **ITB** branding     | `itb/rich/`               | `itb/minimal/`            |

- **Branding** changes only the title page and declaration via a small
  `thesis-metadata.tex` file plus the logo in `assets/`:
  - `generic` — neutral placeholders (`University Name`, placeholder logo). Best
    if your students are at various institutions.
  - `leeds` — pre-filled for the University of Leeds, with the real logo.
  - `itb` — pre-filled for Institut Teknologi Bandung (logo is a placeholder to
    replace with the official one).
- **Detail level** changes only the chapter content:
  - `rich` — every chapter is a commented, worked example showing how to do
    figures, subfigures, tables, equations, citations, lists, cross-references,
    and code listings. Best for learning.
  - `minimal` — clean chapter stubs with section headings and `% TODO`
    comments. Best once you already know LaTeX.

**Suggestion for sharing with students:** start them on `generic/rich` (or
`leeds/rich` / `itb/rich` to match your institution). They get a thesis that
compiles immediately and doubles as a LaTeX tutorial.

## Getting started (any variant)

1. Copy your chosen variant folder somewhere of your own (or upload it to
   Overleaf).
2. Edit `thesis-metadata.tex` — title, author, supervisors, degree, university,
   school — and put your institution's logo at `assets/logo.png`.
3. Replace the placeholder text in `sections/` with your own writing.
4. Add references to `references.bib`; figures to `figures/`.
5. Compile (details in each variant's own `README.md`):
   - **Overleaf:** set `main.tex` as the main document and press *Recompile*.
   - **Locally:** `pdflatex main` → `bibtex main` → `pdflatex main` →
     `pdflatex main`, or simply `latexmk -pdf main.tex`.

## What each variant contains

```
main.tex             # preamble + document structure (identical across variants)
thesis-metadata.tex  # title/author/etc. (differs by branding)
references.bib       # bibliography database
README.md            # per-variant quick-start
assets/logo.png      # institution logo (differs by branding)
figures/             # figures (rich variants ship an example image)
sections/            # declaration, abstract, acknowledgements, chapters, appendix
```

## Notes for the maintainer

- The original thesis content lives in the parent folder and is untouched.
- A placeholder logo and example figure are generated images; the Leeds logo is
  the genuine one carried over from the original thesis.
- Before submission, always check your institution's regulations for the exact
  declaration wording, line spacing, margins, and title-page layout.
