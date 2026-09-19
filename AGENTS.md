# AGENTS.md

## Project overview
This repository contains a single-page LaTeX CV. The main document is `cv.tex`, and the content is split into reusable section files under `sections/`.

## Quick start for a fresh clone
1. Clone the repository.
2. Open a terminal in the project root.
3. Compile the CV with PDFLaTeX:

```bash
git clone <repo-url>
cd <repo-root>
pdflatex -interaction=nonstopmode -halt-on-error cv.tex
```

4. If `latexmk` is installed, the same project can also be built with:

```bash
cd <repo-root>
latexmk -pdf -interaction=nonstopmode cv.tex
```

The generated output will be `cv.pdf` in the project root.

## Working conventions
- Keep the CV as a simple LaTeX project: no heavy tooling, no bibliography, and no multi-pass builds beyond the standard PDFLaTeX workflow.
- The main document compiles from `cv.tex` and includes section files in this order:
  - `sections/header.tex`
  - `sections/education.tex`
  - `sections/research_experience.tex`
  - `sections/publications.tex`
  - `sections/professional_experience.tex`
  - `sections/achievements.tex`
  - `sections/references.tex`
- Shared formatting lives in `styles/cv-style.tex`; avoid changing the global layout unless the update is intentionally document-wide.
- Each section is usually a standalone `.tex` file and should remain self-contained enough to be reused or edited individually.
- Preserve UTF-8 input and avoid introducing packages unless they are clearly necessary.

## Editing guidance
- Prefer editing the relevant section file instead of rewriting the entire document.
- Keep content concise and consistent with the existing CV structure.
- Reuse the established commands such as `\cvsection{...}`, `\entry{...}{...}{...}`, and `\entrytwo{...}{...}` to match the layout and tone.
- Do not add unrelated tooling, scripts, or project scaffolding.
- If a compile error appears, check the `.tex` source and section inputs before adding new packages or dependencies.

## Key files
- `README.md` — repository summary and quick context
- `cv.tex` — document entry point
- `styles/cv-style.tex` — shared formatting and helper commands
- `sections/*.tex` — CV content sections

## Practical agent behavior
When working in this repo, prefer surgical edits, preserve the current LaTeX style, and validate by compiling the document after meaningful changes. The project is intentionally lightweight and should remain easy to clone, edit, and compile in a plain LaTeX environment.
