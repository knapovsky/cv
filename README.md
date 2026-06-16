# CV — Martin Knapovský

This repository contains the source files for Martin Knapovský's technical CV/resume.

The CV is maintained as a LaTeX document so it can be version-controlled, reviewed, and exported consistently to PDF or other formats when needed.

## Profile

Martin Knapovský is a Senior Project Engineer based in Perth, Western Australia, with experience across managed services, Microsoft 365, cloud migrations, networking, virtualisation, infrastructure operations, web development, automation, and self-hosted systems.

## Repository contents

```text
.
├── cv.tex              # Main LaTeX CV source
├── assets/             # Profile images used by the CV
├── README.md           # Project documentation
└── .gitignore          # Ignores generated/private CV artefacts
```

Generated exports such as PDFs, DOCX files, build logs, and private reference material are intentionally not stored in this repository.

## Building the CV

Install a LaTeX distribution such as TeX Live or MacTeX, then run:

```bash
pdflatex cv.tex
```

For a cleaner rebuild, run it twice so references and layout metadata settle:

```bash
pdflatex cv.tex
pdflatex cv.tex
```

The expected output is:

```text
cv.pdf
```

`cv.pdf` is ignored by git and should be treated as a generated artefact.

## Editing workflow

1. Update `cv.tex`.
2. Build locally with `pdflatex cv.tex`.
3. Open the generated PDF and review layout, spacing, page breaks, and contact details.
4. Commit only source changes, not generated files.

Useful cleanup command after a local build:

```bash
rm -f *.aux *.log *.out *.toc *.fls *.fdb_latexmk *.synctex.gz
```

## Privacy notes

The public repository intentionally avoids storing:

- exact residential address
- third-party reference email addresses
- private reference sheets
- generated PDFs/DOCX exports
- local LaTeX build artefacts

Use a private overlay file or local-only branch for sensitive versions of the CV.

## Suggested private/local files

The `.gitignore` allows keeping local files such as:

```text
cv-private.tex
references.tex
private/
```

These can be used for private contact details or reference information without committing them.

## License

No explicit license is included. Treat the content as personal copyrighted material unless the owner adds a license.
