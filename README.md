# Author Manuscript

A template repository that contains the latex code structure for a nice, simple author manuscript.

## Features
- (coming soon) A configurable docker container builder + helper scripts to build the paper with latex;
- (coming soon) An automatic github actions hook to build the output pdf on every push;
- `a4` "article" format;
- [`Atkinson Hyperlegible`](https://brailleinstitute.org/freefont) font for maximum readability;
- [`Fira Code`](https://github.com/tonsky/FiraCode) as a monospace font;
- Nicely formatted headings;
- Support journal-like author listings with affiliation and contact information;
- Built-in `bibtex` support with the modern `biber`;
- Supported hyperlinks with nice default colors;
- Code blocks with custom colors, with custom Python, R and shell highlighting;
- Helper commands like `\mono{text}` for inline monospace text;
- Support for images with a sensible width default;
- Support for captions, subcaptions, and nice footnotes;
- Support for appendices, with custom figure numeration;
- Automatic glossary and table of abbreviations;
- Support for nice abstracts;
- Nicely supported metadata fields, like conflicts of interest and funding;
- Separate files for all main parts of the paper;
- Plain, commented, customizable latex code (`main.tex`).
- Default draft headers and footers to signal the draft.

# How to use
On github, click "Use this template". Follow the guide to use the template.
Then clone and write!
```bash
git clone git@github.com:your/repo
```

## Editing the bibliography
Update the `bibliography.bib` file with your favorite citation manager.

## Editing the glossary
To add a new acronym, add a line to `src/resources/glossary.tex` like:
```latex
% \newacronym{shortcode}{ACRONYM}{Long-form acronym}
\newacronym{nes}{NES}{Normalized Enrichment Score}
```
To add a new acronym with a different "long" plural form than just the singular + `s`:
```latex
\newacronym[
  longplural={Ion Channels and Transporters}
]{ict}{ICT}{Ion Channel and Transporter}
```

## Adding figures
Add figures to the `/src/resources/images` folder, and use them as normal in the code.
