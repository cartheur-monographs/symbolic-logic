# Berkeley Living Robots LaTeX Edition

This directory contains a modern LaTeX facsimile edition of:

- `Edmund C. Berkeley, The Construction of Living Robots (1952)`

Because the source PDF in `sources/` is image-only and local OCR tooling is not
available in this environment, this edition is currently a LaTeX-wrapper
facsimile rather than a full retyped critical transcription.

OCR tooling is now available, and working OCR artifacts have been generated.
However, the quality of the scan means the extracted text is still noisy and
should be treated as a draft transcription aid rather than a publication-ready
text.

## Files

- `main.tex`: LaTeX source for the facsimile edition
- `main.pdf`: compiled PDF output
- `artifacts/living-robots-ocr.pdf`: OCR-processed searchable PDF
- `artifacts/living-robots-ocr.txt`: raw extracted OCR text

## Source

The facsimile pages are drawn from:

- `../../sources/Berkeley--The Construction of Living Robots.pdf`

## Build

```bash
cd editions/berkeley-living-robots
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

## OCR workflow used

```bash
ocrmypdf --skip-text "sources/Berkeley--The Construction of Living Robots.pdf" /tmp/living-robots-ocr.pdf
pdftotext /tmp/living-robots-ocr.pdf -
```

The resulting text is usable for guided cleanup and transcription work, but not
yet accurate enough to replace the facsimile by itself.
