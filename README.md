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
- Places Education, Research Interests, and Research Experience before teaching.
- Keeps Publications as one section with Peer-Reviewed Publications and Thesis
  subsections, filtered by BibLaTeX entry type.
- Moves Technical Skills ahead of presentations, appointments, and outreach.
- Focuses research descriptions on methods, contributions, and selected outcomes;
  preserves all five projects, dates, advisors, roles, and output links.
- Gives the role and advisor separate arguments in `\researchentry`, displaying
  the role before the advisor on a full-width line below the institution/date.
- Uses a general research-interest line covering computational materials physics,
  computational biophysics, and complex systems. Tailor it to each application.
- Preserves the official presentation titles, all 13 entries, and the existing
  talk/poster classifications. Includes the author lists supplied by the CV
  author for the 2021, 2023, and 2025 AAS posters, alongside the verified 2022
  AAS talk and 2024 Cool Stars poster lists. The seven-author 2021 list is
  shortened to its first three authors plus `et al.` to keep the CV at three
  pages. Separate speaker-only rows are omitted from the two linked videos.
- Leaves the existing website and automation files unchanged.

## Presentation author sources

- 2022 AAS talk: https://ui.adsabs.harvard.edu/abs/2022AAS...24021703R/abstract
- 2024 Cool Stars poster: https://ui.adsabs.harvard.edu/abs/2024csss.confE..81R/abstract
- 2025 AAS poster: https://ui.adsabs.harvard.edu/abs/2025AAS...24540315R/abstract
- 2023 AAS poster: https://ui.adsabs.harvard.edu/abs/2023AAS...24120402R/abstract
- 2021 AAS poster: https://ui.adsabs.harvard.edu/abs/2021AAS...23715410S/abstract
- 2025 video speaker: https://www.simonsfoundation.org/video/mohammad-refat-star-spot-inference-using-light-curve-inversion-techniques/
- 2019 video speaker: https://mohammadrefat23.github.io/events/2019-07-31-talk-2/

The CV author supplied the 2021, 2023, and 2025 AAS author lists directly from
ADS. The 2021 CV title and linked record use different titles; both have been
preserved as provided rather than silently renaming the presentation.

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

Presentation author/speaker credits use the optional argument:

```tex
\begin{presentation}[\textbf{M. Refat}, J. Vos, R. Luger, X. Tan]
{Title}{Venue}{Location}{Year}
\end{presentation}
```

Omit the square-bracket argument when authors have not been verified. Use an
explicit `Speaker:` label for a recording that identifies only its speaker.

## Validation status

The editing environment lacks `fontawesome5`, `biblatex`, and Biber, and package
installation is restricted. No compiled PDF or verified page count is included.
The changed research-heading command and presentation environment were compiled
in an isolated test document with the actual revised section contents, and the
rendered pages were inspected. This does not validate the complete CV's page
breaks or bibliography. Source structure and archive contents were also checked;
compile the full project in your normal LaTeX environment before submitting.
