# Accessibility

How the CV and cover letter read for people and for software.

## What the files do

- **Contrast:** body text is near-black on white and links are dark blue, both well above WCAG AA contrast.
- **Links are not colour alone:** every link is also underlined, so it still reads as a link when printed in greyscale.
- **Real text:** everything is selectable text, never an image of text, so screen readers and parsers can read it.
- **Icons are decorative:** the header icons carry empty `ActualText`, so they are skipped by text extraction and do not add noise.
- **Placeholders:** the cover letter marks them three ways (square brackets, bold and a highlight), so they can be found without seeing colour.
- **Reading order:** a single column below the header keeps the reading order the same as the visual order.

## Known limitations

- The PDFs are not tagged PDF/UA documents, so a screen reader gets the text in order but no heading structure. Tagging is possible with `\DocumentMetadata` in a recent LaTeX.
- Some parsers read the two-column header row by row. Name, location, email and phone come first either way.

## The shared statement

> [!NOTE]
> The wider accessibility statement is in [zaccesss/accessibility](https://github.com/zaccesss/accessibility) and on [isaacadjei.me/accessibility](https://isaacadjei.me/accessibility). This file takes precedence where the two differ.
