# Laboratory Report Templates (LaTeX)

Two independent, English-language LaTeX templates for physics and other
experimental-science laboratory reports.

| Format | Source | Example |
| --- | --- | --- |
| Single-column report | [single-column/main.tex](single-column/main.tex) | [PDF](previews/single-column.pdf) |
| Double-column report | [double-column/main.tex](double-column/main.tex) | [PDF](previews/double-column.pdf) |

The layouts are adapted from original laboratory-report formatting developed
by **Dr. Karol Cieślik** in 2017–2018. The samples are new and generic: there
are no historical measurements, student records, supervisors' names, or
university logos in the published templates.

## Quick start

1. Choose either `single-column/` or `double-column/`.
2. Upload **both** `main.tex` and `references.bib` from that folder into a
   new [Overleaf](https://www.overleaf.com/) project. Alternatively, compile
   locally using the commands below.
3. Edit the metadata commands near the beginning of `main.tex`:
   `\reporttitle`, `\reportauthor`, `\reportinstitution`, `\reportcourse`,
   and `\reportdate`.
4. Replace the example sections, table and graph with your own work.

These are standalone examples. Neither depends on files in the other folder.

## Compile locally

A reasonably complete TeX Live or MiKTeX installation is sufficient.
The document uses pdfLaTeX, BibTeX, TikZ/PGFPlots, and standard LaTeX packages.

From the chosen template directory:

```sh
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Or, if available:

```sh
latexmk -pdf main.tex
```

## Example content

The sample report describes an elementary Ohm's-law experiment, **solely to
demonstrate the layout**. Every numerical measurement is fictional. The chart
is drawn directly by PGFPlots, so no external image files or image rights are
involved. The bibliography contains only a bibliographic reference, not a
copy of the cited work.

The single-column layout gives figures and explanatory text more space.
The double-column layout is more compact and includes an optional, commented
full-width table example using `table*`. Uncomment that block when needed;
full-width floats may appear on the next page in a two-column document.

## License

The original template code and illustrative content in this repository are
provided under the [MIT License](LICENSE). The licence does not grant rights
to any external works cited in the bibliography.

## Attribution and history

Developed from the author's original LaTeX report layouts used in physics
laboratory coursework in 2017–2018, with the historic content and branding
removed, dependencies streamlined, and examples rewritten for public reuse.
