# CV

LaTeX sources for my CV, resume and cover letter, based on the [Awesome-CV](https://github.com/posquit0/Awesome-CV) template.

Every push to `main` triggers a GitHub Actions workflow that compiles all three documents with XeLaTeX and publishes them to GitHub Pages.

## Documents

- `cv.tex` — full academic-style CV
- `resume.tex` — short resume
- `coverletter.tex` — cover letter

## Local build

Requires a TeX Live distribution with XeLaTeX.

```bash
latexmk -xelatex cv.tex
latexmk -xelatex resume.tex
latexmk -xelatex coverletter.tex
```

## Published output

After the workflow runs, the PDFs are available at:

- https://so77id.github.io/CV/cv.pdf
- https://so77id.github.io/CV/resume.pdf
- https://so77id.github.io/CV/coverletter.pdf
