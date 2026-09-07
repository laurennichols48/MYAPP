# Lab 5: Student Materials

## Lab Files

- [Box model playground](resources/box-model-playground.html)
- [Playground stylesheet](resources/box-model-playground.css)
- [Broken card challenge](resources/broken-cards.html)
- [Broken card stylesheet](resources/broken-cards.css)
- [Completed card challenge](resources/completed-cards.html)
- [Completed card stylesheet](resources/completed-cards.css)
- [Font selection guide](resources/font-selection-guide.md)

## The Box Model and Visual Styling

### Guiding Question

Why can an element occupy more space than its width suggests?

### Lab Goals

After completing this lab, you will be able to:

- Identify the four layers of the box model.
- Predict how padding and borders affect total size.
- Use `box-sizing: border-box`.
- Style type, colors, images, spacing, borders, and footers.
- Build reusable project-card styles.
- Refactor inconsistent visual rules.

---

## Part 1: Measure a Box

Open the box model playground.

The `.measurement-box` begins with:

```css
width: 240px;
padding: 20px;
border: 5px solid;
margin: 30px;
```

Before changing the code, predict:

1. Content width: __________________
2. Left and right padding combined: __________________
3. Left and right border combined: __________________
4. Visible box width, not including margin: __________________
5. Horizontal space including margin: __________________

Use the browser’s developer tools when available to inspect the box.

Record what you observe.

________________________________________________________________

---

## Part 2: Change One Layer at a Time

For each property:

1. Predict what will change.
2. Edit the CSS.
3. Save and refresh.
4. Describe the actual result.

| Change | Prediction | Actual result |
|---|---|---|
| Set `padding` to `0`. |  |  |
| Restore padding and set `border` to `0`. |  |  |
| Restore the border and set `margin` to `0`. |  |  |
| Add `box-sizing: border-box`. |  |  |

Complete:

- Padding creates space __________________________________________.
- Margin creates space ___________________________________________.
- A border appears _______________________________________________.
- With `border-box`, the declared width includes __________________.

---

## Part 3: Repair Uneven Project Cards

Open the broken card challenge.

Problems include:

- Cards use different one-off spacing values.
- Images stretch to inconsistent sizes.
- Padding makes some cards wider than intended.
- Similar declarations are repeated.
- Text is difficult to scan.
- The footer has no deliberate spacing of its own — it only looks separated from the content above it because of a leftover card margin.

Repair the stylesheet.

Your result should include:

- A universal `box-sizing: border-box` rule.
- A reusable `.project-card` class.
- Consistent card padding, border, and margin or gap.
- Images with a controlled width and `height: auto` or an intentional crop.
- A readable line height.
- A footer with separation from the main content.

Record three changes.

| Change | Why it improved the page |
|---|---|
|  |  |
|  |  |
|  |  |

Compare with the completed version after you finish.

---

## Part 4: Build a Small Visual System

Choose a limited set of values for your portfolio.

Keep to these limits so the system stays small enough to remember:

- One body font, plus at most one additional heading font. Reusing the body font for headings is a valid choice.
- No more than four colors total: main text, background, accent, and link.
- A spacing scale of four to five values, reused everywhere — avoid introducing a new one-off pixel value elsewhere in your CSS.
- Every choice should have a reason you could explain to a partner, not just "it looked fine."

### Typography

Not sure what to pick? See the [font selection guide](resources/font-selection-guide.md).

- Body font: ______________________________________
- Heading font, when different: _____________________
- Body line height: _________________________________

### Color

- Main text color: __________________________________
- Background color: _________________________________
- Accent color: _____________________________________
- Link color: _______________________________________

### Spacing

Choose a small spacing scale, for example:

```text
8px, 16px, 24px, 32px
```

Your scale:

____________________________________________________

Use repeated spacing values instead of choosing a new value for every element.

---

## Part 5: Peer Review Your Visual System

Exchange your typography, color, and spacing choices with a partner before applying them to your portfolio.

The reviewer should complete these statements:

- The text and background colors are ______________________ to read.
- The font choices feel ______________________ together.
- The spacing scale is ______________________ to remember.
- One change I'd suggest is ______________________.

The designer should select one revision to make before the checkpoint.

Revision made:

________________________________________________________________

---

## Part 6: Portfolio Checkpoint

Update your portfolio stylesheet.

Required additions:

- `box-sizing: border-box`.
- A page font and readable line height.
- A maximum width for the main content.
- Consistent page padding.
- A reusable card, panel, or section class.
- Image sizing that does not distort images.
- A footer with clear separation.
- Consistent heading and link colors.

### Visual Review

- [ ] Text is readable against its background.
- [ ] Content does not touch the browser edge.
- [ ] Cards or sections use consistent spacing.
- [ ] Images do not stretch.
- [ ] The same kind of element looks consistent across pages.
- [ ] The footer is visually separate but not distracting.
- [ ] No rule is repeated when one reusable class would work.

---

## Exit Questions

1. Name the four box-model layers from inside to outside.

   ________________________________________________________________

2. What is the difference between padding and margin?

   ________________________________________________________________

3. What problem does `box-sizing: border-box` solve?

   ________________________________________________________________

4. Why is a spacing scale useful?

   ________________________________________________________________

5. What repetitive CSS did you refactor?

   ________________________________________________________________

6. What is one question you still have about the box model or visual styling?

   ________________________________________________________________
