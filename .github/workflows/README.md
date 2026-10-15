# Workflows

| Workflow | Runs on | What it does |
| --- | --- | --- |
| [`build.yml`](build.yml) | Push to `main`, every pull request | Installs Tectonic, compiles `cv/cv.tex` and `cover-letter/cover-letter.tex` and fails if the cover letter is longer than one page |
| [`markdownlint.yml`](markdownlint.yml) | Push to `main`, every pull request | Lints every markdown file against [`.markdownlint.json`](../../.markdownlint.json) |

Both can be run manually via `workflow_dispatch` from the Actions tab.
