# Ideas for this repo

Backlog of ideas to evolve the CV repo beyond a single-PDF pipeline.

## Selected for current work

- [x] **Build badge in README** — status of the GitHub Actions build + direct link to the published PDF.
- [x] ~~**Improved landing page**~~ — dropped. The README badge is enough to reach the PDF.
- [x] **ES/EN versions** — compile Spanish and English resumes from shared sources. Publish as `resume-en.pdf` and `resume-es.pdf`. Spanish content starts as a copy of English and needs to be translated in `resume/es/*.tex`.

## Backlog

### Quick wins
- **GitHub Releases per version** — each push creates a release with the PDF attached so there's a downloadable history (`resume-2026-04.pdf`). Useful to know which version was sent to which company.

### Multi-variant
- **Role-specific resumes** — separate entry points (`resume-ml.tex`, `resume-backend.tex`, `resume-leadership.tex`) that share the same `resume/*.tex` fragments via selective `\input`. Workflow compiles all variants and publishes them side by side.

### AI-assisted tailoring
- **Tailoring by job posting** — script (Python + Claude API) that takes a job description and generates a `resume-tailored.tex` reordering bullets and tuning the summary. Runnable locally or as a manual workflow (`workflow_dispatch` with input).
- **Cover letter generator** — same pattern: feed the job posting and generate a cover letter `.tex`.

### Application tracking
- **Issues as tracker** — each application is a GitHub issue with labels (`applied`, `interview`, `rejected`, `offer`). Issue template with fields: company, role, date, link, CV version used.
- **Kanban board** — GitHub Project with columns for each application stage.

### Analytics
- **Link tracking** — short URLs (or a custom subdomain) to see who opens the CV and when.

## Notes

- Everything runs through the existing GitHub Actions workflow.
- LaTeX sources are Awesome-CV based (XeLaTeX).
