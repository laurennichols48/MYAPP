# Lab 4: Student Materials

## Lab Files

- [Selector practice files](resources/selector-practice.html)
- [Cascade investigation files](resources/cascade-investigation.html)
- [Broken selectors challenge](resources/broken-selectors.html)
- [Completed selectors challenge](resources/completed-selectors.html)

## CSS Selectors and the Cascade

### Guiding Question

When several CSS rules could affect the same element, which rule wins?

In Lab 3, you saw that CSS can live inline, internally, or externally. Those locations have a pecking order too: inline beats the other two, while internal and external are tied and fall back to ordinary source order — the same idea Part 4 explores next among selectors.

### Lab Goals

After completing this lab, you will be able to:

- Use element, class, ID, and attribute selectors.
- Choose an appropriate selector for a styling task.
- Explain how source order affects equal-specificity rules.
- Recognize that IDs are more specific than classes and element selectors.
- Identify inherited properties.
- Diagnose rules that do not apply because of incorrect selectors.
- Avoid unnecessary overuse of IDs.
- Combine selectors to target an element more precisely.

---

## Part 1: Match Selectors

Open:

- `resources/selector-practice.html`
- `resources/selector-practice.css`

Identify what each selector targets.

| Selector             | Elements Affected |
| -------------------- | ----------------- |
| `p`                  |                   |
| `.notice`            |                   |
| `#featured`          |                   |
| `a[target="_blank"]` |                   |

## Part 2: Write Selectors

Add rules that:

1. Make every paragraph use `line-height: 1.5`.
2. Make every element with class `notice` italic.
3. Add `10px` of padding to the element with ID `featured`.
4. Underline links with `target="_blank"`.

Record the selector used for each task.

| Task                                  | Selector Used |
| -------------------------------------- | ------------- |
| Line height on every paragraph        |               |
| Italic text on `.notice` elements     |               |
| Padding on `#featured`                |               |
| Underline on `target="_blank"` links  |               |

## Part 3: Combine Selectors

Two elements were added to `selector-practice.html`: a `<div class="notice">` and a footer link outside `<main>`.

Add both of these rules to `selector-practice.css`:

```css
h1, .notice {
  color: blue;
}

main a {
  color: blue;
}
```

Before refreshing, predict:

1. Which elements will the first rule affect?

   ________________________________________________________________

2. Which elements will the second rule affect? Does that include the footer link?

   ________________________________________________________________

Refresh and record what actually happened.

| Rule          | Predicted elements | Actual elements |
| ------------- | ------------------- | ---------------- |
| `h1, .notice` |                      |                  |
| `main a`      |                      |                  |

### Compare the Punctuation

One selector uses a comma. The other uses a space. Now change the punctuation and see what breaks.

1. Change `h1, .notice` to `h1 .notice` (replace the comma with a space). Refresh. What happened to the color?

   ________________________________________________________________

2. Change `main a` to `maina` (delete the space). Refresh. What happened to the color?

   ________________________________________________________________

3. Restore both rules to their original, working form.

Based on what you just saw, complete these in your own words:

- A comma between two selectors ___________________________________.
- A space between two selectors ___________________________________.

Compare your answer:

- A comma groups separate selectors so they receive the same styles.
- A space targets an element located inside another element.

### Comma or Space?

For each goal below, decide whether you need a comma or a space, then write the selector and test it in `selector-practice.css`.

| Goal                                                                 | Comma or space? | Selector |
| --------------------------------------------------------------------- | ---------------- | -------- |
| Give `<h1>` and every `<p>` the same `line-height`, in one rule       |                   |          |
| Bold only the links inside `<main>`                                   |                   |          |
| Underline only the link inside the `<footer>`                         |                   |          |
| Give `#featured` and the `<div class="notice">` the same background color, in one rule |    |          |

---

## Part 4: Source Order

Open `resources/cascade-investigation.html` and its CSS file.

This part tracks only the plain paragraph — "Which color will this paragraph use?" — since it has no `class` or `id`. (The `.notice` and `#featured` paragraphs are controlled by more specific rules and will not change color in this part.)

Before refreshing, predict its color.

Move the two `p` rules so that their order is reversed.

| Rule Order                            | Predicted Color | Actual Color |
| ------------------------------------- | --------------- | ------------ |
| Navy rule first, dark red rule second |                 |              |
| Dark red rule first, navy rule second |                 |              |

What pattern do you observe?

Reflect: if a teammate says "my CSS isn't working" and you both find a rule that targets the right element, what should you check first, based on what you just saw?

---

## Part 5: Specificity

The featured paragraph matches:

- `p`
- `.notice`
- `#featured`

Predict which rule will control its color.

| Selector    | Specificity Level |
| ----------- | ----------------- |
| `p`         |                   |
| `.notice`   |                   |
| `#featured` |                   |

Which selector wins? Why?
Hint: `#featured` selects the element with `id="featured"`, and IDs are more specific than classes and elements.

Reflect: in Part 4, moving a rule later in the file changed which one won. Would moving `p` to the very bottom of this stylesheet change the answer here? Why or why not?

---

## Part 6: Inheritance

Add this rule:

```css
main {
  font-family: Georgia, serif;
  color: darkgreen;
}
```

Which child elements change without being selected directly?

---

Does a border applied to `<main>` automatically appear around each child?

---

## Part 7: Repair Broken Selectors

Open:

- `resources/broken-selectors.html`
- `resources/broken-selectors.css`

Correct each issue.

| Intended Target                 | Broken Selector | Correction |
| ------------------------------- | --------------- | ---------- |
| Elements with class `card`      |                 |            |
| Element with ID `featured-card` |                 |            |
| Links opening in a new tab      |                 |            |
| All `<h2>` elements             |                 |            |
| Paragraphs inside `.card` sections |             |            |

---

## Exit Questions

1. When should you use a class selector?

   ***

2. Why should IDs usually be unique?

   ***

3. What happens when equal-specificity rules conflict?

   ***

4. Which is more specific: a class or element selector?

   ***

5. What does inheritance mean in CSS?

   ***

6. What is the difference between `h1, .notice` and `h1 .notice`?

   ***

7. What is one question you still have about selectors or the cascade?

   ***
