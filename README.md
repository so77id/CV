# Resume

[![Build and Publish CV](https://github.com/so77id/CV/actions/workflows/build.yml/badge.svg)](https://github.com/so77id/CV/actions/workflows/build.yml)
[![Download EN](https://img.shields.io/badge/download-resume--en.pdf-blue)](https://so77id.github.io/CV/resume-en.pdf)
[![Download ES](https://img.shields.io/badge/download-resume--es.pdf-red)](https://so77id.github.io/CV/resume-es.pdf)

LaTeX sources for my resume, based on the [Awesome-CV](https://github.com/posquit0/Awesome-CV) template.

Every push to `main` triggers a GitHub Actions workflow that compiles `resume.tex` with XeLaTeX and publishes it to GitHub Pages.

## Structure

- `resume.tex` — shared master template
- `resume-en.tex` / `resume-es.tex` — language wrappers that set `\lang` and include the master
- `resume/macros.tex` — i18n helpers (`\iflang`, `\daterange`, `\datefrom`) and polyglossia setup
- `resume/en/` / `resume/es/` — per-language content (parallel structure)

To add a new section, add the `\input` in `resume.tex` once and create the same filename under both `resume/en/` and `resume/es/`.

## Local build

Requires a TeX Live distribution with XeLaTeX and the `polyglossia` package.

```bash
latexmk -xelatex resume-en.tex
latexmk -xelatex resume-es.tex
```

## Published output

- https://so77id.github.io/CV/resume-en.pdf
- https://so77id.github.io/CV/resume-es.pdf
