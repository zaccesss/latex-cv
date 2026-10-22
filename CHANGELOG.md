# Changelog

All notable changes to this project are recorded here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### Added

- Word versions of the CV and the cover letter, `cv/cv.docx` and `cover-letter/cover-letter.docx`
- A step-by-step guide in `guides/using-it.md`, linked from the README and the support page

### Changed

- Spoken Languages becomes Additional Information with Languages, Certifications and Interests rows
- Every entry in Leadership and Volunteering has a skills line under its title, as in Experience
- The research entry keeps the publisher and date on the right
- A one-line Profile opens the CV, saying what drives the work and the role or placement wanted
- Sections run Projects, Experience, Leadership and Volunteering, then Research and Publications
- The skills list ends with a Professional row for ways of working. The example CV keeps one job entry so it stays on one page
- Every date sits on the second line of its entry in italics, so education, experience and leadership dates line up the same way
- Project dates show the year only
- The Volunteering section is now Leadership and Volunteering, so it also holds society and representative roles
- The header and link icons are black, so only the link text carries the link colour
- The CV and the cover letter each live in their own folder, `cv/` and `cover-letter/`, with their compiled PDFs

### Fixed

- The build refreshes the package list before installing poppler, so the page check no longer fails on a stale mirror

## [1.0.0] - 2026-10-15

### Added

- `cv.tex`: a CV with a two-column contact header, linked project entries and standard section names
- `cover-letter.tex`: a one-page letter with the same header and highlighted placeholders
- Compiled examples and preview images
- A workflow that compiles both files on every pull request
