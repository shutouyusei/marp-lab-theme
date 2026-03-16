---
name: create-slide
description: Create a new weekly meeting slide deck from template. Use when starting a new presentation for the weekly meeting.
disable-model-invocation: true
allowed-tools: Read, Write, Edit, Bash, Glob
---

Create a new weekly meeting slide deck.

## Arguments

`$ARGUMENTS` should be one of:
- A date in `MM-DD` format (e.g., `03-25`) — uses current year
- A date in `YYYY/MM-DD` format (e.g., `2026/03-25`)
- Empty — uses the next upcoming meeting date (assume weekly on Wednesdays)

## Steps

1. Determine the target date from arguments
2. Create the folder `<year>/<MM-DD>/` if it doesn't exist
3. Create an `images/` subfolder inside it
4. Copy `template.md` to `<year>/<MM-DD>/slides.md`
5. Update the title slide with the correct date and author name "Yusei"
6. Report the created file path

## Rules

- All slide content MUST be written in English
- Use the project's `template.md` as the base
- Do not overwrite existing `slides.md` — warn the user if it already exists
- Follow folder convention: `<year>/<MM-DD>/`
