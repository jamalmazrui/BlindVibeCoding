# Accessibility

This repository holds the sources, build scripts and publishing script of *Blind Vibe Coding: Building Apps Nonvisually with AI*, a Kindle ebook by Jamal Mazrui, and the GitHub Pages directory of the same name. Both are made by a blind author for screen reader users, so accessibility is the point of the project rather than a feature of it.

## What we aim for

- The book: an EPUB that reads well with a screen reader: real headings, a linked table of contents, a Start of Content landmark, a linked glossary, numbered notes that link to their sources, a text description of the cover, and the EPUB accessibility metadata that says all of this. The target is the EPUB Accessibility 1.1 features Pandoc and this build can supply, with WCAG 2.2 AA as the general standard.
- The directory page: plain Markdown rendered by GitHub Pages, with one level 2 heading per category, one level 3 heading per resource, fields as lists rather than tables, alternative text on every image, and links whose text names the resource.
- The scripts: everything runs from a Command Prompt, reports in short sentences, and writes a log that can be read later, so that no step depends on seeing a screen.

## Tested with

- JAWS and NVDA on Windows 11, with speech, by the author, who uses them daily; VoiceOver on iOS for the directory page. Braille output has not yet been tested; reports from braille display users are welcome.
- The EPUB's internal links are checked by the build on every run (zero broken links at the last build), and its accessibility metadata is written by the build. Ace by DAISY and EPUBCheck have not yet been run on the shipped EPUB, because the build machine could not reach the npm registry; the metadata therefore carries no conformance claim.

## Known barriers

- The notes in the book do not link back to the text they came from; use the reader's Back command.
- Kindle apps vary in how they expose EPUB landmarks and accessibility metadata; the book was not tested in every Kindle app.
- The publishing script drives a browser, and the first run needs a sign-in to KDP in that browser, which works with a screen reader but is a manual step.

## Reporting a barrier

Open an issue in this repository, or write to the author through the contact on his GitHub profile. Say which file or page, which screen reader and version, what you expected to hear, and what you heard. The one-problem-per-report form in `templates\Bug_Report.md` helps.

## Ownership

Jamal Mazrui maintains this project. This statement was written on 3 October 2026 and is revised with each release.
