# Using the CV and cover letter

A step-by-step walkthrough, from opening the files to sending a finished PDF. The [README](../README.md) has the short
version.

## 1. Open the files

### Overleaf

1. Download [`cv/cv.tex`](../cv/cv.tex) (and [`cover-letter/cover-letter.tex`](../cover-letter/cover-letter.tex) if you
   want the letter).
2. In Overleaf choose **New Project**, then **Upload Project** to upload the `.tex` file.
3. Open **Menu**, set **Compiler** to **XeLaTeX** and press **Recompile**.

> [!IMPORTANT]
> The default compiler is pdfLaTeX, which cannot load the fonts these files use. A `fontspec` error means the compiler
> setting has not changed yet.

### On your own computer

- **Tectonic:** install it, then run `tectonic cv/cv.tex`. The PDF appears next to the source.
- **TeX Live or MacTeX:** run `latexmk -xelatex cv.tex` inside the `cv` folder.

### In Word

Open [`cv/cv.docx`](../cv/cv.docx) or [`cover-letter/cover-letter.docx`](../cover-letter/cover-letter.docx) in
Word, Pages or Google Docs and replace the example text. The layout is simpler than the PDF, but the sections and
the order are the same, so the steps below still apply. Set your name in **File** then **Properties**. Save
as PDF unless the employer asks for Word.

## 2. Fill in the header

Near the top of the document is the name, then two short columns of contact details. Replace the name and each
contact line with your own. Delete the phone line if you would rather not share a number. Each link has a display
text and an address: change both.

Set the same name in `pdfauthor`, `pdfcreator` and `pdftitle` near the top of the file, so the PDF's properties show
it.

## 3. Fill in each section

Every entry follows the same shape:

| Line | What goes there |
| --- | --- |
| Bold title on the left | The project, job or qualification |
| On the right | Links, the organisation or the dates |
| Italic second line | The tools, skills or subtitle, with the dates on the right |
| Bullets | What you did and what came of it |

Good bullets start with a verb, stay within one or two lines and include something that can be checked, such as a
number, a result or a link.

## 4. Add, remove or reorder

- **Add an entry:** copy a whole entry (from its bold title to the end of its bullets) and paste it where you want it.
- **Remove an entry:** delete the same block.
- **Remove a section:** delete its `\section{...}` line together with everything up to the next section.
- **Reorder sections:** move each block, heading included. Put the sections that matter most to the job first.

## 5. Tailor a copy for each application

Keep one full version with everything in it, then save a copy for each application and cut it down:

- Move the projects and experience closest to the advert to the top.
- Use the advert's own words for skills you genuinely have, since recruitment systems match on them.
- Keep the CV to one or two full pages. A half-empty last page looks unfinished.

## 6. Write the cover letter

Every part to change in [`cover-letter.tex`](../cover-letter/cover-letter.tex) is in square brackets on a highlight.

1. Search the file for `\ph{` to find each one.
2. Replace the whole `\ph{[...]}` (brackets included) with plain text.
3. Recompile and check nothing is still highlighted.

Use "Yours sincerely" when you address someone by name and "Yours faithfully" for "Dear Hiring Team". Keep the
letter to one page.

## 7. Check before sending

- Open the PDF, select all the text, copy it and paste it into a plain text editor. What appears there is what a
  recruitment system reads. Check names, dates and links come through whole.
- Click every link in the PDF.
- Name the file clearly, for example `Firstname_Lastname_CV.pdf`.

> [!TIP]
> Keep the `.tex` source with each version you send, so you can see later exactly what went to each employer.
