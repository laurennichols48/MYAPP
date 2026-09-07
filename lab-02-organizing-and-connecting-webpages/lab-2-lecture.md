# Lab 2: Lecture

## Organizing and Connecting Webpages

## Semantic HTML

Semantic elements communicate the purpose of their content.

```html
<body>
  <header>...</header>
  <nav>...</nav>
  <main>
    <section>...</section>
  </main>
  <footer>...</footer>
</body>
```

A `<div>` is a generic container. Use it when no more meaningful element fits.

## Heading Hierarchy

```html
<h1>Neighborhood Book Club</h1>
<h2>Upcoming Events</h2>
<h3>Saturday Discussion</h3>
```

Heading levels communicate structure, not only visual size.

## Multi-Page Websites

A multi-page website connects separate HTML files.

```html
<nav>
  <a href="index.html">Home</a>
  <a href="about.html">About the club</a>
</nav>
```

A relative path describes a file's location compared with the current file.

## Introductory Accessibility

Use:

```html
<html lang="en"></html>
```

Give each page a meaningful title:

```html
<title>About | Neighborhood Book Club</title>
```

Prefer descriptive links:

```html
<a href="schedule.html">View the meeting schedule</a>
```

rather than:

```html
<a href="schedule.html">Click here</a>
```

## Inline CSS

Inline CSS is written in the opening tag:

```html
<h1 style="color: darkgreen;">Neighborhood Book Club</h1>
```

Inline styles are useful for a quick experiment or a one-off visual change on a single element.

```html
<nav style="background-color: lightgray; padding: 10px;">
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
</nav>
```

Use inline CSS when you want to test a style quickly, but avoid copying the same `style` attribute across many elements or pages. If a style should apply to several elements, use a shared stylesheet instead.
