# alvi-cv

My CV, written in LaTeX. The document entry point is `cv.tex`; its content is maintained in reusable files under `sections/`, with shared formatting commands in `styles/cv-style.tex`.

## Build

Compile from the repository root with PDFLaTeX:

```bash
pdflatex -interaction=nonstopmode -halt-on-error cv.tex
```

This produces `cv.pdf` in the repository root.

## Document structure

`cv.tex` includes these sections in order:

1. `sections/header.tex`
2. `sections/education.tex`
3. `sections/research_experience.tex`
4. `sections/publications.tex`
5. `sections/professional_experience.tex`
6. `sections/projects.tex`
7. `sections/achievements.tex`
8. `sections/references.tex`

Edit the relevant section file to update CV content. Shared layout and helper commands are defined in `styles/cv-style.tex`.
