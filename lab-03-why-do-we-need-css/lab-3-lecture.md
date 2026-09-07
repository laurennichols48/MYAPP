# Lab 3: Lecture

## Why Do We Need CSS?

HTML describes content and structure:

```html
<h1>Community Garden Club</h1>
```

CSS describes presentation:

```css
h1 {
  color: darkgreen;
}
```

## CSS Rule Anatomy

```css
h1 {
  color: darkgreen;
  text-align: center;
}
```

- Selector: `h1`
- Properties: `color`, `text-align`
- Values: `darkgreen`, `center`

## Inline CSS

```html
<h1 style="color: darkgreen;">Community Garden Club</h1>
```

Fast for one experiment, but repetitive.

## Internal CSS

```html
<style>
  h1 {
    color: darkgreen;
  }
</style>
```

Useful for styles that belong to one page.

## External CSS

```html
<link rel="stylesheet" href="styles.css">
```

The separate file can be shared across many pages.

## Refactoring

Refactoring improves code organization without intentionally changing the result. Moving repeated styles into a shared rule reduces duplication and makes future changes easier.
