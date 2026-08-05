# Transcription Draft

This directory contains a cleaned LaTeX transcription draft of Edmund C.
Berkeley's *The Construction of Living Robots*.

Current scope:

- title page
- introduction
- contents page
- all of Part I in searchable text
- the main prose framework of Part II in searchable text
- image plates for the most figure-dense schematic pages
- Part III in searchable text

The transcription is based primarily on direct reading from the scan, with OCR
used only as a secondary aid. Figure-heavy pages are retained as embedded
plates where that better preserves Berkeley's original schematic presentation.

Related assets:

- full extracted page images: [`figures/berkeley-living-robots-pages/`](../../../figures/berkeley-living-robots-pages)
- figure-heavy subset: [`figures/berkeley-living-robots-plates/`](../../../figures/berkeley-living-robots-plates)

## Build

```bash
cd editions/berkeley-living-robots/transcription
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```
