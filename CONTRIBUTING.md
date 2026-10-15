# Contributing

Improvements to the layout, the build instructions or how well parsers read the PDFs are welcome.

## Before you start

- Open an issue first for anything larger than a small fix, so the change can be agreed before you spend time on it.
- Keep the example text neutral: never commit a real name, phone number, email or employer.
- Both files must still compile with XeLaTeX and the letter must stay on one page.

## Making a change

1. Fork the repository and create a branch.
2. Edit `cv/cv.tex` or `cover-letter/cover-letter.tex`.
3. Compile with `tectonic cv/cv.tex` (or `latexmk -xelatex` inside the folder) and check the result by copying the PDF text into a plain text editor.
4. Regenerate the compiled PDFs and the preview images in `images/` if the layout changed.
5. Open a pull request that explains what changed and why.

## Commit messages

Use a short type prefix and an imperative subject, for example `fix: keep long titles on one line` or `docs: explain the Overleaf compiler setting`. Types: `feat`, `fix`, `docs`, `refactor`, `chore`.

## Code of conduct

Everyone taking part is expected to follow the [code of conduct](CODE_OF_CONDUCT.md). See [isaacadjei.me](https://isaacadjei.me) for more.
