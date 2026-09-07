# Lab 1: Lecture Guide

## Related Lab Files

- [Completed example HTML](resources/completed-example.html)
- [Corrected HTML example](resources/corrected-example.html)

## Lecture Purpose

The lecture should formalize the concepts students explored during the guided-discovery lab. Refer back to specific changes and errors students encountered rather than presenting the ideas as entirely new information.

## Suggested Lecture Sequence

### 1. What HTML Does

- HTML stands for HyperText Markup Language.
- HTML describes the structure and meaning of webpage content.
- A browser reads HTML and uses it to construct the displayed page.

### 2. HTML, CSS, and JavaScript

- **HTML** provides structure and content.
- **CSS** controls visual presentation and layout.
- **JavaScript** adds behavior and interactivity.

A useful comparison:

- HTML is the structure of a house.
- CSS is its appearance and decoration.
- JavaScript controls things that move, respond, or change.

### 3. Basic HTML Document Structure

Introduce the purpose of each part:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>

  <body>
    <h1>Visible Page Heading</h1>
    <p>Visible page content goes inside the body.</p>
  </body>
</html>
```

- `<!DOCTYPE html>` tells the browser to interpret the document as modern HTML.
- `<html>` contains the HTML document.
- `<head>` contains information about the page.
- `<title>` controls the title shown in the browser tab.
- `<body>` contains the content displayed on the webpage.

### 4. Anatomy of an HTML Element

Use:

```html
<p>Welcome to my website.</p>
```

Identify:

- Opening tag: `<p>`
- Content: `Welcome to my website.`
- Closing tag: `</p>`
- Complete element: `<p>Welcome to my website.</p>`

### 5. Tags Versus Elements

- A tag is a piece of HTML syntax, such as `<p>` or `</p>`.
- An element is the complete unit, including its tags and content.

### 6. Attributes and Attribute Values

Use:

```html
<a href="about.html">Learn more about us</a>
```

Identify:

- Element name: `a`
- Attribute: `href`
- Attribute value: `"about.html"`
- Visible content: `Learn more about us`

Explain that attributes provide additional information about an element and are usually written inside the opening tag.

### 7. Parent and Child Relationships

Use:

```html
<p>This word is <strong>important</strong>.</p>
```

- The `<p>` element is the parent.
- The `<strong>` element is the child.
- The child element is nested inside the parent element.

### 8. Correct Nesting

Correct:

```html
<p>This word is <strong>important</strong>.</p>
```

Incorrect:

```html
<p>This word is <strong>important.</p></strong>
```

Explain that the element opened most recently should usually be closed first.

### 9. Headings and Heading Hierarchy

```html
<h1>Main Page Title</h1>
<h2>Main Section</h2>
<h3>Smaller Subsection</h3>
```

- `<h1>` represents the main heading.
- `<h2>` represents a major section beneath it.
- `<h3>` represents a subsection.
- Heading levels communicate structure, not only text size.

### 10. Paragraphs

```html
<p>This is a paragraph.</p>
```

Paragraph elements group related written content.

### 11. Ordered and Unordered Lists

Unordered list:

```html
<ul>
  <li>Apples</li>
  <li>Bananas</li>
  <li>Oranges</li>
</ul>
```

Ordered list:

```html
<ol>
  <li>Open the file.</li>
  <li>Make a change.</li>
  <li>Refresh the browser.</li>
</ol>
```

Each `<li>` element must be placed inside a `<ul>` or `<ol>` element.

### 12. Images

Images show pictures on a page. Use the `src` attribute to point to the image file and the `alt` attribute to describe it for people who cannot see the image.

```html
<img src="resources/garden.png" alt="A colorful garden path" />
```

- `src` tells the browser where to find the image.
- `alt` provides text for screen readers and appears if the image does not load.
- Images are part of the page content and should still be described clearly.

### 13. Links and the `href` Attribute

```html
<a href="https://example.com">Visit Example</a>
```

- The text between the tags is what the user sees.
- The `href` value tells the browser where the link should go.

### 13. Indentation and Readability

Compare:

```html
<body>
  <h1>My Page</h1>
  <p>Hello!</p>
</body>
```

with:

```html
<body>
  <h1>My Page</h1>
  <p>Hello!</p>
</body>
```

Both may display similarly, but indentation makes the relationships among elements easier to understand.

### 14. How Browsers Handle Incorrect HTML

Browsers often attempt to repair or interpret incorrect HTML. This is why a page may display even when tags are missing or incorrectly nested.

Correct HTML remains important because it:

- Produces more predictable results.
- Improves accessibility.
- Makes code easier to read and maintain.
- Reduces differences among browsers.
- Makes future CSS and JavaScript work easier.

### 15. Viewing an HTML File

Review the basic workflow:

1. Write or edit the HTML file.
2. Save the file.
3. Open it in a browser.
4. Refresh the browser after each saved change.
5. Return to the source code to continue editing.

## Lecture Check for Understanding

Ask students to identify the parts of:

```html
<a href="contact.html">Contact us</a>
```

Then ask:

1. Which text will appear on the page?
2. Which part is the attribute?
3. Which part is the attribute value?
4. Is the full line a tag or an element?
5. What file will the browser try to open?

---
