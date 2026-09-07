# Lab 9: Student Materials

## Lab Files

- [Grid playground](resources/grid-playground.html)
- [Playground stylesheet](resources/grid-playground.css)
- [Broken Grid challenge](resources/broken-grid-layout.html)
- [Completed Grid challenge](resources/completed-grid-layout.html)
- [Flex or Grid comparison](resources/flex-or-grid.html)

## Building Layouts with CSS Grid

### Guiding Question

How can rows and columns be designed together without positioning every item separately?

### Lab Goals

After completing this lab, you will be able to:

- Identify grid containers, items, rows, and columns.
- Create and resize grid tracks.
- Add row and column gaps.
- Span a featured item across columns.
- Build a responsive grid with `repeat()`, `minmax()`, and `auto-fit`.
- Choose between Grid and Flexbox.
- Build a responsive portfolio project layout.

---

## Part 1: Build Explicit Columns

Open the Grid playground.

Begin with:

```css
.playground {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

Answer:

1. How many columns are created? _________________________________
2. What does `fr` appear to represent? ____________________________

3. Before editing the rule, predict what will change if it becomes `2fr 1fr 1fr`.

   Prediction: ________________________________________________________________

   Now make the change. What actually happens?

   ________________________________________________________________

4. Before adding it, predict what `gap: 24px` will change.

   Prediction: ________________________________________________________________

   Now add it. What actually changes?

   ________________________________________________________________

Try:

```css
grid-template-columns: 180px 1fr;
```

Which column stays fixed? Which column absorbs remaining space?

________________________________________________________________

---

## Part 2: Span a Featured Item

Add the following rule to the featured card:

```css
.featured {
  grid-column: span 2;
}
```

Observe the layout at wide and narrow widths.

Answer:

1. How many column tracks does the item occupy?

   ________________________________________________________________

2. Does the visual order still match the HTML order?

   ________________________________________________________________

3. What problem can occur if only one column fits?

   ________________________________________________________________

Restore the starting file after the investigation.

---

## Part 3: Create a Responsive Gallery

Replace the explicit columns with:

```css
grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
```

Resize the browser.

Complete:

- `repeat()` helps ________________________________________________.
- `auto-fit` allows _______________________________________________.
- `minmax(220px, 1fr)` prevents tracks from _______________________.
- The layout changes without _____________________________________.

Record the approximate number of columns at three widths.

| Browser width | Number of columns |
|---|---:|
| Narrow |  |
| Medium |  |
| Wide |  |

---

## Part 4: Repair the Grid Layout

Open the broken Grid challenge.

Problems include:

- Grid properties are placed on the children instead of the parent.
- Columns use rigid pixel widths that overflow.
- The featured card spans nonexistent tracks.
- Spacing is repeated with margins.
- The layout lacks a narrow-screen plan.

Repair the layout using:

- One grid container.
- Responsive track sizing.
- `gap`.
- A featured card that spans only when space permits.
- A simple media query when needed.

A media query applies a rule only when the browser width matches a condition:

```css
@media (min-width: 720px) {
  .featured {
    grid-column: span 2;
  }
}
```

The declarations inside only take effect at or above the given width, so the featured card can span two tracks on wider screens and stay a single column on narrow ones.

Compare with the completed version.

---

## Part 5: Flexbox or Grid?

Four of these are built in the comparison file — open it and see how each was actually done. For the other two, there's nothing to inspect; reason them out from what you've learned in this lab and Lab 8.

| Layout problem | Flexbox, Grid, or either? | Reason |
|---|---|---|
| Horizontal navigation links (in the file) |  |  |
| Project gallery with rows and columns (in the file) |  |  |
| Button and icon aligned in one control (reason it out) |  |  |
| Page with sidebar and main region (in the file) |  |  |
| Tags that wrap onto new lines (in the file) |  |  |
| Dashboard-like card arrangement (reason it out) |  |  |

There can be more than one valid answer. Your reason matters.

---

## Part 6: Portfolio Checkpoint

Use CSS Grid for your projects, interests, or experience page.

Requirements:

- [ ] The shared parent is the grid container.
- [ ] Cards use a reusable class.
- [ ] Gaps are controlled by the parent.
- [ ] Columns adapt at narrow widths.
- [ ] Text does not overflow its card.
- [ ] HTML order remains meaningful.
- [ ] A featured item spans only when the layout can support it.
- [ ] Grid solves a two-dimensional problem better than manual positioning.

---

## Exit Questions

1. What is a grid track?

   ________________________________________________________________

2. What does `1fr` mean?

   ________________________________________________________________

3. Why is `minmax()` useful in a responsive grid?

   ________________________________________________________________

4. Give one layout better suited to Flexbox and one better suited to Grid.

   ________________________________________________________________

5. What changed in your portfolio project layout?

   ________________________________________________________________

6. What is one question you still have about Grid?

   ________________________________________________________________
