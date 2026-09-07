# Lab 3: Student Materials

## Lab Files

- [Inline CSS example](resources/inline-example.html)
- [Internal CSS example](resources/internal-example.html)
- [External CSS example](resources/external-example.html)
- [Refactor starter file](resources/refactor-starter.html)
- [Refactor completed example](resources/refactor-completed.html)
- [Broken stylesheet link practice file](resources/broken-stylesheet-link.html)

## Why Do We Need CSS?

### Guiding Question

Where should styling instructions live when a website grows?

### Lab Goals

After completing this lab, you will be able to:

- Explain the different roles of HTML and CSS.
- Identify inline, internal, and external CSS.
- Identify selectors, properties, values, and declarations.
- Connect HTML to an external stylesheet.
- Compare the maintenance costs of three styling methods.
- Refactor repeated inline styles.
- Repair a broken stylesheet link.

---

## Part 1: Compare Three Versions

Open:

- `resources/inline-example.html`
- `resources/internal-example.html`
- `resources/external-example.html`

| Version | Where Is the CSS Stored? |
|---|---|
| Inline |  |
| Internal |  |
| External |  |

Which version uses a separate `.css` file?

________________________________________________________________

## Part 2: Change and Observe

Change the main heading color in each version.

| Version | File and Location Changed | Result |
|---|---|---|
| Inline |  |  |
| Internal |  |  |
| External |  |  |

Which version would be easiest to update if five pages shared the same design? Explain.

________________________________________________________________

## Part 3: Find Repetition

Open `resources/refactor-starter.html`.

Count repeated declarations.

| Declaration | Number of Copies |
|---|---:|
| `color: darkgreen;` |  |
| `background-color: honeydew;` |  |
| `padding: 10px;` |  |

What could happen if one copy changes and the others do not?

________________________________________________________________

## Part 4: Refactor

### A. Internal CSS

Add a `<style>` element inside `<head>`. Move repeated declarations into CSS rules and remove the matching `style` attributes.

Example:

```html
<style>
  h1 {
    color: darkgreen;
  }
</style>
```

### B. External CSS

Move the CSS rules into `resources/refactor-styles.css`.

Add this inside `<head>`:

```html
<link rel="stylesheet" href="refactor-styles.css">
```

Save both files and refresh.

What advantage does the external file provide?

________________________________________________________________

## Part 5: Repair the Connection

Open `resources/broken-stylesheet-link.html`.

Repair the `<link>` element so that it loads `styles.css`.

| Original Problem | Correction | Evidence It Worked |
|---|---|---|
|  |  |  |

---

## Portfolio Checkpoint

Apply what you practiced today to your own portfolio site.

- [ ] Create one external stylesheet, for example `styles.css`.
- [ ] Link every portfolio page to the same stylesheet.
- [ ] Remove any inline `style` attributes added in Lab 2.
- [ ] Move any page-specific `<style>` rules into the shared external stylesheet where they apply to more than one page.
- [ ] Confirm all pages look consistent after the change.

---

## Exit Questions

1. What is the main job of HTML?

   ________________________________________________________________

2. What is the main job of CSS?

   ________________________________________________________________

3. What is one benefit of external CSS?

   ________________________________________________________________

4. What does a selector identify?

   ________________________________________________________________

5. What is the difference between a property and a value?

   ________________________________________________________________

6. Suppose one page has both inline CSS and an external stylesheet, and both set the same property on the same element. Which do you think wins? Take a guess — you'll test it next lab.

   ________________________________________________________________

7. What is one question you still have about styling with CSS?

   ________________________________________________________________
