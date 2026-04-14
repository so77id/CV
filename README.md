# CV

LaTeX sources for my CV, based on the [Awesome-CV](https://github.com/posquit0/Awesome-CV) template.

Every push to `main` triggers a GitHub Actions workflow that compiles `cv.tex` with XeLaTeX and publishes it to GitHub Pages.

## Local build

Requires a TeX Live distribution with XeLaTeX.

```bash
latexmk -xelatex cv.tex
```

## Published output

- https://so77id.github.io/CV/
- https://so77id.github.io/CV/cv.pdf
