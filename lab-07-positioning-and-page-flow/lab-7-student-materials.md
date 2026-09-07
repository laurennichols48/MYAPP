# Lab 7: Student Materials

## Lab Files

- [Positioning playground](resources/positioning-playground.html)
- [Playground stylesheet](resources/positioning-playground.css)
- [Broken positioning challenge](resources/broken-positioning.html)
- [Completed positioning challenge](resources/completed-positioning.html)
- [Float example](resources/float-example.html)

## Positioning and Page Flow

### Guiding Question

When should an element stay in normal page flow, and when should it be positioned?

### Lab Goals

After completing this lab, you will be able to:

- Distinguish block and inline behavior.
- Explain normal document flow.
- Compare static, relative, absolute, and fixed positioning.
- Use relative positioning to establish a containing block.
- Place a small overlay with absolute positioning.
- Use and clear a limited image float.
- Avoid positioning the entire page manually.

---

## Part 1: Observe Normal Flow

Open the positioning playground.

Change the highlighted elements between:

```css
display: block;
display: inline;
display: inline-block;
```

Before testing each value, predict its behavior. Then make the change and record what actually happens.

| Display value | Prediction | Starts on a new line? | Can width and height be applied as expected? | Neighboring content |
|---|---|---|---|---|
| block |  |  |  |  |
| inline |  |  |  |  |
| inline-block |  |  |  |  |

What is normal flow?

________________________________________________________________

---

## Part 2: Test Position Values

Change only the `.test-box` rule.

### Static

```css
position: static;
```

### Relative

```css
position: relative;
top: 12px;
left: 20px;
```

### Absolute

```css
position: absolute;
top: 12px;
right: 12px;
```

### Fixed

```css
position: fixed;
bottom: 12px;
right: 12px;
```

Before each test, predict how the box will behave. Then apply the value and observe:

| Position | Prediction | Does its original space remain? | What is it positioned relative to? | Does it move while scrolling? |
|---|---|---|---|---|
| static |  |  |  |  |
| relative |  |  |  |  |
| absolute |  |  |  |  |
| fixed |  |  |  |  |

The box you positioned with `absolute` jumped to a spot relative to the whole page, not the dashed reference container around it — because that container was never given a `position` value of its own. The nearest ancestor with a `position` other than `static` is called its **containing block**. An absolutely positioned element is placed relative to its containing block, or to the page itself if there isn't one.

Restore the original stylesheet after the investigation.

---

## Part 3: Repair an Escaping Badge

Open the broken positioning challenge.

The “Featured” badge should sit in the upper-right corner of the featured project card, but it escapes to another part of the page.

Repair the layout without assigning page coordinates.

Hint:

- Which element should be the badge’s containing block?
- Which position value creates that containing block without removing the card from flow?

Record the two key declarations:

```css
.featured-card {
  __________________________________________
}

.badge {
  __________________________________________
}
```

Compare with the completed challenge.

---

## Part 4: Use a Limited Float

Open the float example.

Observe how the paragraph wraps around the image.

Then remove the clearing rule from the later heading.

What happens?

________________________________________________________________

Restore the clearing rule.

A float can still be useful for text wrapping around an image. It should not be the default tool for navigation bars, card rows, or full-page layouts.

---

## Part 5: Portfolio Checkpoint

Add at most one purposeful positioned detail, such as:

- A small “Featured” label inside a project card.
- A caption overlay inside an image container.
- A back-to-top link fixed near a viewport corner.
- A subtle decorative shape positioned inside a section.

Requirements:

- The main page layout must remain in normal flow, Flexbox, or Grid.
- An absolutely positioned child must have an intentional containing block.
- The detail must not cover text at narrow widths.
- Keyboard users must still be able to reach interactive content.
- The page must remain usable when the positioned detail is removed.

---

## Exit Questions

1. What is normal document flow?

   ________________________________________________________________

2. What is the difference between relative and absolute positioning?

   ________________________________________________________________

3. Why did the badge escape its card?

   ________________________________________________________________

4. When is fixed positioning useful?

   ________________________________________________________________

5. Why should floats have a limited role in modern layout?

   ________________________________________________________________

6. What is one question you still have about positioning?

   ________________________________________________________________
