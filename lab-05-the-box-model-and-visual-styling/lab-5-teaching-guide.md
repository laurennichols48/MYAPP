# Lab 5: Teaching Guide

## The Box Model and Visual Styling

## Purpose

Students connect visible spacing to the box-model layers and use that understanding to repair a small card layout. The lab treats visual design as a system of reusable choices rather than a collection of random declarations.

## Preparation

- Verify the box-model measurements before class.
- Make browser developer tools available when possible.
- Keep the placeholder SVG files beside the card examples.
- Encourage students to change one layer at a time.
- Do not make exact arithmetic the only goal; connect the arithmetic to layout behavior.
- Pair students before Part 5's peer review.
- Optionally assign `resources/font-selection-guide.md` as pre-lab reading. It's linked directly from Part 4 either way, so reading it ahead of time isn't required, but it can save time during the Visual System discussion.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-add padding, then a border, then a margin to one box, narrating the running width total after each addition. Then skip `box-sizing: border-box`, watch a card overflow its container, and think out loud about diagnosing "my declared width is right but the box is too big" — the same problem Part 3's cards have.

**Scaffold:** The box model playground and broken card challenge are the scaffold — students measure and repair inside files you already built.

**Fade:** The Portfolio Checkpoint (consistent box model and visual system) is the fade step.

## Suggested Timing

| Part                  |       Time |
| --------------------- | ---------: |
| Measure a box         |  8 minutes |
| Change one layer      |  8 minutes |
| Repair project cards  | 14 minutes |
| Build a visual system |  7 minutes |
| Peer review           |  5 minutes |
| Portfolio checkpoint  |  9 minutes |
| Exit questions        |  4 minutes |

## Answer Guidance

For the initial box using the default content-box model:

- Content width: `240px`
- Horizontal padding: `40px`
- Horizontal border: `10px`
- Visible box width: `290px`
- Horizontal space including margins: `350px`

With `box-sizing: border-box`, the declared `240px` includes content, padding, and border.

## Facilitation Guidance

### Part 1

Ask students to point to each layer visually. Developer tools are useful, but students should still explain the model in words.

### Part 2

Clarify:

- Padding belongs inside the border.
- Margin sits outside the border.
- Background color extends through the padding but not the margin.
- The border surrounds content and padding.

### Part 3

Accept different visual choices when they solve the structural problems. The completed example is a reference, not the only valid design.

Look for:

- `*, *::before, *::after { box-sizing: border-box; }`
- Shared card rules.
- Consistent image treatment.
- Reasonable maximum content width.
- Separation between main content and footer.
- Reduced duplication.

### Part 4

A visual system should be small enough to remember. Students do not need a professional design system. A few fonts, colors, and spacing values are enough. Trial runs showed students need explicit limits here, not just examples — hold them to the stated maximums (one body font plus at most one heading font, four colors, four to five spacing values) rather than letting the system grow unchecked.

### Part 5

Require a specific, visible answer for each reviewer statement — reject "it looks good" the same way Lab 6's peer review rejects "I like it." A revision does not need to be large; changing one color or collapsing two similar spacing values both count.

## Common Student Difficulties

### Width appears not to work

Check whether padding and borders are added outside the declared width and whether the element is constrained by a parent.

### Images look stretched

Avoid setting both width and height without considering aspect ratio. Use `height: auto` or `object-fit: cover` for an intentional crop.

### Students add margins everywhere

Ask whether spacing belongs inside an element, between neighboring elements, or between groups. Choose padding, margin, or container gap accordingly.

### Cards use unique classes for identical designs

Encourage one reusable class with only small modifier classes when truly needed.

## Completion Check

Students should:

- Correctly identify content, padding, border, and margin.
- Predict the total width of the starting box.
- Use `border-box`.
- Repair the provided cards.
- Keep the visual system within the stated limits (fonts, colors, spacing values).
- Complete a peer review with a specific, actionable suggestion.
- Apply a consistent visual system to the portfolio.
