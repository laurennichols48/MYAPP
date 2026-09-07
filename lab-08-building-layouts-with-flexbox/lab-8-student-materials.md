# Lab 8: Student Materials

## Lab Files

- [Flexbox playground](resources/flexbox-playground.html)
- [Playground stylesheet](resources/flexbox-playground.css)
- [Broken Flexbox challenge](resources/broken-flex-layout.html)
- [Completed Flexbox challenge](resources/completed-flex-layout.html)

## Building Layouts with Flexbox

### Guiding Question

How can a group of items share and rearrange space along one main direction?

### Lab Goals

After completing this lab, you will be able to:

- Identify flex containers and items.
- Map the main and cross axes.
- Align and distribute items.
- Add consistent gaps.
- Change direction and wrapping.
- Build responsive navigation and content rows.
- Remove positioning rules that Flexbox replaces.

---

## Part 1: Map the Axes

Open the Flexbox playground.

Begin with:

```css
.playground {
  display: flex;
  flex-direction: row;
}
```

Draw or describe:

- Main-axis direction: ____________________________________________
- Cross-axis direction: __________________________________________

Change `flex-direction` to `column`.

- Main-axis direction: ____________________________________________
- Cross-axis direction: __________________________________________

Complete:

`justify-content` controls alignment along the __________________ axis.

`align-items` controls alignment along the __________________ axis.

---

## Part 2: Test Alignment

Try the following values one at a time.

### `justify-content`

- `flex-start`
- `center`
- `space-between`
- `space-around`

### `align-items`

- `stretch`
- `flex-start`
- `center`
- `flex-end`

### `gap`

- `0`
- `8px`
- `24px`

Record two useful combinations.

| Goal | Declarations |
|---|---|
| Put equal space between navigation groups |  |
| Center items along the cross axis |  |

---

## Part 3: Make Items Wrap

Reduce the browser width.

Before adding either rule below, predict what will happen to the items when they no longer fit in one row.

Prediction: ________________________________________________________________

Add:

```css
flex-wrap: wrap;
```

Then test a flexible item rule:

```css
.item {
  flex: 1 1 220px;
}
```

Answer:

1. What does the layout actually do when all items no longer fit? Did it match your prediction?

   ________________________________________________________________

2. Why is a flexible basis more useful than a single fixed width?

   ________________________________________________________________

3. Does Flexbox preserve the HTML reading order?

   ________________________________________________________________

---

## Part 4: Repair the Flex Layout

Open the broken challenge.

Problems include:

- `display: flex` is applied to individual links instead of their shared parent.
- Navigation spacing is created with repeated margins.
- Project cards use absolute positioning.
- Cards cannot wrap on narrow screens.
- Vertical alignment is inconsistent.

Repair the layout using:

- One flex container for the navigation.
- One flex container for the project list.
- `gap`.
- `align-items`.
- `flex-wrap`.
- Flexible card sizing.
- No absolute positioning for the card row.

Compare with the completed version.

---

## Part 5: Portfolio Checkpoint

Use Flexbox for at least two appropriate groups.

Recommended:

1. Navigation.
2. A row containing text and an image, buttons, tags, or summary information.

Requirements:

- [ ] `display: flex` is on the parent.
- [ ] Children are arranged along a clear main axis.
- [ ] `gap` is used for repeated spacing.
- [ ] The layout wraps or changes direction when needed.
- [ ] Content remains readable at a narrow width.
- [ ] HTML order still makes sense without CSS.
- [ ] Flexbox is not used merely because it was the current lesson.

---

## Exit Questions

1. What becomes a flex item?

   ________________________________________________________________

2. How does `flex-direction` affect the main axis?

   ________________________________________________________________

3. What is the difference between `justify-content` and `align-items`?

   ________________________________________________________________

4. What does `flex-wrap` allow?

   ________________________________________________________________

5. Which part of your portfolio now uses Flexbox, and why?

   ________________________________________________________________

6. What is one question you still have about Flexbox?

   ________________________________________________________________
