# Mohammad Alvi Refat - Curriculum Vitae

Main file: `cv.tex`. Compile with PDFLaTeX and Biber, or run:

```sh
latexmk -pdf cv.tex
```

On Overleaf, set `cv.tex` as the main document and use PDFLaTeX.
The existing `biblatex` setup uses Biber. The project also requires
`fontawesome5`; retain the original package dependencies.

## Revision notes

- Uses the uploaded LaTeX project as the source of truth.
- Keeps Education, Research Interests, Research Experience, Publications, Academic Presentations, Professional Appointments, Courses Taught, Technical Skills, and Outreach in that order.
- Renumbers the section files so their filenames match their order in `cv.tex`.
- Preserves the official presentation titles and the existing Talks/Posters subsections.
- Removes presentation author lists and their associated layout code.
- Removes the duplicated year from `CUNY Masters Graduation 2025`; the year remains in the date column.
- Retains useful venue/location or host information for presentations while avoiding duplicated metadata.
- Moves Technical Skills after Professional Appointments and Courses Taught.
- Leaves the research-experience wording, overall template, website files, and automation files otherwise unchanged.

## Editing a research heading

The command now takes six arguments in this order:

```tex
\researchentry
  {Project title}
  {Institution}
  {Role}
  {Advisor name}
  {Dates}
  {Output links}
```

For example, the master's project uses separate `{M.S. Thesis Researcher}` and
`{Dr. Lucy Lu}` arguments. It displays `M.S. Thesis Researcher | Advisor: Dr. Lucy Lu`.
Do not include `Advisor:` or the separator in either argument; the command adds
them. Leave the role or output-links argument as `{}` when not needed. To change
their display order globally later, edit the metadata row in `cv.tex` rather than
rewriting each project's content.

## Validation status

The complete project was compiled successfully with `latexmk -pdf cv.tex`, including
Biber/biblatex and Font Awesome. The resulting CV is three pages. All three pages
were rendered and visually checked after the edits; no clipping, overlap, broken
glyphs, or orphaned Posters heading was found.
