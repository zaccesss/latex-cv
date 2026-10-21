# latex-cv

A clean LaTeX CV and a one-page cover letter in a matching style, written so applicant tracking systems read every word.
Open the `.tex` files, replace the example text with your own and compile. The [step-by-step guide](guides/using-it.md)
walks through every part.

| CV | Cover letter |
| --- | --- |
| ![First page of the CV: a name in small capitals with contact details in two columns, then Education, Technical Skills, Projects and Experience sections with bold titles, italic detail lines and short bullets](images/cv-1.png) | ![The cover letter: the same header, then the date, recipient and subject, with highlighted placeholders in square brackets throughout the body](images/cover-letter-1.png) |

## What is in it

| File | What it is |
| --- | --- |
| [`cv/cv.tex`](cv/cv.tex) | The CV: education, skills, projects, experience, publications, leadership and volunteering, achievements and languages |
| [`cover-letter/cover-letter.tex`](cover-letter/cover-letter.tex) | A one-page letter with the same header and highlighted placeholders to fill in |
| [`cv/cv.pdf`](cv/cv.pdf), [`cover-letter/cover-letter.pdf`](cover-letter/cover-letter.pdf) | The compiled examples |
| [`cv/cv.docx`](cv/cv.docx), [`cover-letter/cover-letter.docx`](cover-letter/cover-letter.docx) | Word versions of the same example text, for anyone not using LaTeX |
| [`images/`](images) | The preview images shown above |
| [`guides/using-it.md`](guides/using-it.md) | A step-by-step guide from opening the files to sending the PDF |

## Build it

Both files need **XeLaTeX** (or LuaLaTeX), because they load fonts through `fontspec`. Every font and package they use
ships with TeX Live, so nothing extra has to be installed.

- **Overleaf:** upload the `.tex` file, then open Menu, set Compiler to XeLaTeX and recompile.
- **Tectonic:** `tectonic cv/cv.tex` downloads what it needs on the first run and writes the PDF beside the source.
- **TeX Live or MacTeX:** `cd cv && latexmk -xelatex cv.tex`

> [!IMPORTANT]
> pdfLaTeX will not compile these files. If Overleaf shows a `fontspec` error, the compiler is still set to pdfLaTeX.

> [!NOTE]
> The Word files are a simpler copy for when an employer asks for Word or LaTeX is not to hand. The `.tex` files
> are the main version and changes are made there first.

## Fill it in

- **Header:** replace the name, location, email, phone and the three links at the top. The phone line can be deleted.
- **Entries:** each entry has a bold title with links or the organisation on the right, then an italic line with the
  tools or skills and the dates, then bullets. Copy a whole entry to add another.
- **Bullets:** start with a verb, keep to one or two lines and give a number someone could check.
- **Cover letter:** every part to change is **in square brackets on a highlight**. Search for `\ph{` to find them all,
  then replace each one with plain text.
- **Metadata:** set your name in `pdfauthor`, `pdfcreator` and `pdftitle` near the top so the PDF's properties carry
  it.

## Reading by recruitment systems

- The contact icons are marked with empty `ActualText`, so text extraction skips them instead of returning stray
  symbols.
- Ligatures are switched off, so words such as "office" are not read as "o ice".
- Hyphenation is off, so no word is split across two lines.
- Section names are standard (Education, Experience, Projects, Skills), which parsers recognise.

Check a finished PDF by copying all of its text into a plain text editor: what appears there is what a parser reads.

## Licence

[MIT](LICENSE). See also the [changelog](CHANGELOG.md), [accessibility notes](ACCESSIBILITY.md),
[contributing guide](CONTRIBUTING.md) and [support](SUPPORT.md).
