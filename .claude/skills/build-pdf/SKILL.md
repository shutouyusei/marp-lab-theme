---
name: build-pdf
description: Build a PDF from Marp slides. Use before meetings to generate a presentation PDF.
disable-model-invocation: true
allowed-tools: Bash, Read, Glob
---

Build a PDF from Marp slides.

## Arguments

`$ARGUMENTS` should be one of:
- A path to a specific `slides.md` file
- A date folder like `2026/03-18` — will look for `slides.md` inside
- Empty — will find the most recent slide deck by date folder name

## Steps

1. Locate the target `slides.md` file
2. Run marp to build the PDF:
   ```
   npx marp <path>/slides.md -o <path>/slides.pdf --allow-local-files --html --theme theme.css
   ```
3. Verify the PDF was created and report its path and file size

## Notes

- The theme file is at the project root: `theme.css`
- Marp config is in `marp.config.mjs` with `allowLocalFiles: true` and `html: true`
- If the build fails, check that images referenced in the slides exist
