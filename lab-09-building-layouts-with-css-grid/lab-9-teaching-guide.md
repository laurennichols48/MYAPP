# Lab 9: Teaching Guide

## Building Layouts with CSS Grid

## Purpose

Students use Grid for layouts that require coordinated rows and columns. The lab emphasizes responsive track definitions and a reasoned choice between Grid and Flexbox.

## Preparation

- Test examples at narrow, medium, and wide widths.
- Keep visible outlines on grid items during the investigation.
- Review direct-child behavior: the children of a grid container become grid items.
- Avoid teaching line numbers, named areas, and every placement property in this introductory lab.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-build a three-column grid. First put `grid-template-columns` on a card instead of the shared parent — the exact mistake in Part 4's repair challenge — show that nothing changes, then move the declaration to the parent grid container and narrate why that's the fix.

**Scaffold:** The Grid playground and broken layout challenge are the scaffold — students test and repair inside files you already built.

**Fade:** The Portfolio Checkpoint (Grid for the projects or experience page) is the fade step.

## Suggested Timing

| Part | Time |
|---|---:|
| Explicit columns | 8 minutes |
| Item spanning | 6 minutes |
| Responsive gallery | 9 minutes |
| Repair challenge | 12 minutes |
| Flex or Grid decisions | 6 minutes |
| Portfolio checkpoint and exit | 9 minutes |

## Answer Guidance

- `1fr 1fr 1fr` creates three equal columns.
- `fr` represents a fraction of available space.
- `2fr 1fr 1fr` gives the first track twice the flexible share of either remaining track.
- `gap` creates spacing between tracks.
- `repeat(auto-fit, minmax(220px, 1fr))` creates as many fitting tracks as possible, keeps each at least about 220px, and lets tracks grow.

## Facilitation Guidance

### Responsive Grid

Ask students to resize gradually and watch when a track drops to a new row. The important observation is that the browser can choose the column count from constraints.

### Spanning

A featured card should not depend on tracks that do not exist. A media query can limit spanning to wider layouts.

### Tool Choice

Avoid the slogan “Flexbox for rows, Grid for everything else.” Ask whether the layout primarily coordinates one dimension or two.

## Common Student Difficulties

### Grid declarations have no effect

Verify that `display: grid` and track declarations are on the shared parent.

### Items overflow

Check fixed track widths, long unbreakable content, images, and minimum sizing.

### A spanning item creates an empty-looking area

Review source order, implicit placement, and whether the spanning choice actually supports the content hierarchy.

### Students nest Grid everywhere

Use Grid where coordinated tracks provide value. A nested Flexbox may be simpler for one internal row.

## Completion Check

Students should:

- Create explicit columns.
- Explain `fr`.
- Build a responsive `auto-fit` grid.
- Repair the provided layout.
- Justify at least two Flexbox-versus-Grid decisions.
- Use Grid on the portfolio project page.
