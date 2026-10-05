# Mohammad Alvi Refat - Physics PhD CV project

Editable LaTeX source for a Physics PhD application CV, targeted to
computational materials physics while retaining the broader computational
physics framing. The documented research, publication, presentation, teaching,
outreach, and technical-skills information is preserved.

## Files

- `cv.tex` is the main document.
- `Sections/` contains the editable CV sections.
- `ref.bib` contains the peer-reviewed article and master's thesis records.
- `index.html`, `CNAME`, and `.github/workflows/` are the existing portfolio
  site files and are included unchanged.

## Compile

Compile with PDFLaTeX and Biber, or run:

```sh
latexmk -pdf cv.tex
```

On Overleaf, set `cv.tex` as the main document and select PDFLaTeX. The
bibliography uses `biblatex` with the Biber backend.

## Content notes

- Research interests foreground computational materials physics, molecular
  materials, and atomistic simulation while describing molecular dynamics as
  an interest rather than completed research experience.
- C++ and LAMMPS are marked as foundational/introductory; Java is marked as
  basic.
- The source archive omits a precompiled PDF; compile the editable project to
  produce one.
