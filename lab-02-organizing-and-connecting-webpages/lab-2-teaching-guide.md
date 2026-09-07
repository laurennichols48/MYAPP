# Lab 2: Teaching Guide

## Organizing and Connecting Webpages

**Estimated lab time:** 45–50 minutes

## Preparation

- Keep all files in their original folders.
- Confirm that the completed site links work.
- Show students how to save multiple HTML files in the same folder.
- Remind students that filenames and capitalization must match.
- Optionally assign `resources/basic-styling-reference.md` as homework before Part 6. Trial runs showed students unsure what to actually style once given a free choice; it's linked directly from Part 6 either way, so pre-reading isn't required.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-build the two-file navigation from scratch: create `index.html` and `about.html`, add a `<nav>` with two links, and narrate why you reached for `<nav>` instead of a `<div>`. Then deliberately misspell one `href` as `About.html`, refresh, click the broken link, and think out loud about how you would notice and track down a capitalization mismatch — the same category of bug in Part 4.

**Scaffold:** The starter site and broken-navigation file are the scaffold — students repair and extend files you already built rather than starting from nothing.

**Fade:** The Portfolio Checkpoint (three-page structure and navigation) is the fade step.

## Suggested Timing

| Part                      |       Time |
| ------------------------- | ---------: |
| Inspect page organization |  7 minutes |
| Choose semantic elements  |  7 minutes |
| Connect and repair pages  | 12 minutes |
| Accessibility check       |  7 minutes |
| Inline CSS experiment     |  8 minutes |
| Exit questions            |  4 minutes |

## Facilitation Notes

### Semantic Elements

Ask students what each part of the page is doing before naming the element.

- `<header>` introduces a page.
- `<nav>` contains major navigation links.
- `<main>` contains the page's primary content.
- `<section>` groups related content.
- `<footer>` contains ending information.
- `<div>` is a generic container when no more meaningful element fits.

### Navigation

When `index.html` and `about.html` are in the same folder:

```html
<a href="index.html">Home</a> <a href="about.html">About</a>
```

Common errors include:

- Wrong capitalization.
- Missing `.html`.
- Linking to `home.html` when the file is named `index.html`.
- Saving files in different folders.
- Using vague text such as `Click here`.

### Accessibility Introduction

Students should check:

- `<html lang="en">`
- A useful and unique `<title>` on each page.
- One main `<h1>` on each page.
- Logical heading order.
- Descriptive link text.
- Major navigation inside `<nav>`.

These are introductory practices, not a complete accessibility audit.

### Inline CSS

Use inline CSS only as an experiment:

```html
<h1 style="color: darkgreen;">Neighborhood Book Club</h1>
```

Point out that inline CSS can be helpful for testing a single style, but repeating the same `style` attribute on many elements makes the page harder to maintain. The next lab introduces external stylesheets for reusable styling.

## Answer Guidance

The broken navigation file contains:

- `home.html` instead of `index.html`.
- `About.html` instead of `about.html`.
- A link with no `href`.
- Vague `Click here` text.

## Completion Check

Students should have:

- Two connected pages.
- Working navigation in both directions.
- Semantic page structure.
- Logical headings.
- Descriptive links.
- At least two inline styles.
