# Lab 2: Student Materials

## Lab Files

- [Page organization example](resources/page-organization.html)
- [Broken navigation practice file](resources/broken-navigation.html)
- [Starter site: Home page](resources/starter-site/index.html)
- [Starter site: About page](resources/starter-site/about.html)
- [Completed site example](resources/completed-site/index.html)
- [Basic styling reference](resources/basic-styling-reference.md)

## Organizing and Connecting Webpages

### Guiding Question

How can we organize webpage content so that people and browsers understand it?

### Lab Goals

After completing this lab, you will be able to:

- Organize content with `<header>`, `<nav>`, `<main>`, `<section>`, and `<footer>`.
- Explain the difference between a semantic element and a generic `<div>`.
- Use headings to communicate page structure.
- Connect two HTML files using relative links.
- Create a simple navigation menu.
- Use descriptive link text.
- Add simple inline CSS with the `style` attribute.

---

## Part 1: Inspect Page Organization

Open `resources/page-organization.html`.

Complete the table.

| Content                  | Element |
| ------------------------ | ------- |
| Page introduction        |         |
| Navigation links         |         |
| Main page content        |         |
| Related group of content |         |
| Ending information       |         |

Answer:

1. Do element names such as `<header>` appear as visible text?

   ***

2. What do these names communicate to someone reading the code?

   ***

3. Could the page display if every container were a `<div>`?

   ***

## Part 2: Choose an Element

Use this word bank:

`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<div>`

| Content                              | Best Element |
| ------------------------------------ | ------------ |
| Site title and introduction          |              |
| Main site links                      |              |
| Unique central content               |              |
| A group of upcoming events           |              |
| Copyright information                |              |
| A container needed only for grouping |              |

Add one new `<section>` to `page-organization.html`. Include an `<h2>` and a paragraph.

## Part 3: Connect Two Pages

Open:

- `resources/starter-site/index.html`
- `resources/starter-site/about.html`

Add this navigation to both pages:

```html
<nav>
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
</nav>
```

Save both files and test the links.

## Part 4: Repair Navigation

Open `resources/broken-navigation.html`.

Find and correct:

- A Home link pointing to the wrong filename.
- An About link using incorrect capitalization.
- A link with no destination.
- A link with vague text.

| Error | Correction | Why It Matters |
| ----- | ---------- | -------------- |
|       |            |                |
|       |            |                |
|       |            |                |
|       |            |                |

## Part 5: Accessibility Check

Update both starter pages.

- [ ] Add `lang="en"` to `<html>`.
- [ ] Give each page a different, useful `<title>`.
- [ ] Use one `<h1>` on each page.
- [ ] Use `<h2>` for major sections.
- [ ] Place site links inside `<nav>`.
- [ ] Use descriptive link text.

## Part 6: Add Inline CSS

Not sure what to try? See the [basic styling reference](resources/basic-styling-reference.md).

Add at least two inline styles.

Examples:

```html
<h1 style="color: darkgreen;">Neighborhood Book Club</h1>
```

```html
<nav style="background-color: lightgray; padding: 10px;"></nav>
```

| Element | Style Added | Result |
| ------- | ----------- | ------ |
|         |             |        |
|         |             |        |

What problem might occur if the same inline styles are copied across ten pages?

---

---

## Portfolio Checkpoint

Apply what you practiced today to your own portfolio site.

- [ ] Create `index.html`, `about.html`, and a third page (projects, interests, or experience).
- [ ] Use semantic elements (`<header>`, `<nav>`, `<main>`, `<footer>`) instead of only `<div>`.
- [ ] Add working navigation that links every page to every other page.
- [ ] Give each page a unique, descriptive `<title>`.
- [ ] Use one `<h1>` per page and a logical heading order.
- [ ] Use descriptive link text throughout.

---

## Exit Questions

1. What is the purpose of `<nav>`?

   ***

2. When might a `<div>` be appropriate?

   ***

3. What does `href="about.html"` control?

   ***

4. Why should link text describe its destination?

   ***

5. What is one limitation of inline CSS?

   ***

6. What is one question you still have about organizing or connecting webpages?

   ***
