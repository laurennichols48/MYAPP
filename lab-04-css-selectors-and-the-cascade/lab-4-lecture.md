# Lab 4: Lecture

## CSS Selectors and the Cascade

## Selector Types

Element:

```css
p {
  color: navy;
}
```

Class:

```css
.notice {
  background-color: lightyellow;
}
```

ID:

```css
#featured {
  border: 2px solid black;
}
```

Attribute:

```css
a[target="_blank"] {
  font-weight: bold;
}
```

## Classes and IDs

Classes are reusable:

```html
<p class="notice">First notice</p>
<p class="notice">Second notice</p>
```

IDs identify one unique element:

```html
<p id="featured">Featured message</p>
```

## The Cascade

The cascade decides which declaration applies when rules conflict.

For this lesson:

1. More specific selectors beat less specific selectors.
2. If specificity is equal, the later rule wins.
3. Some properties are inherited from parent elements.

Basic specificity order for this lab:

```text
ID selector (#featured) > class or attribute selector (.notice, [target="_blank"]) > element selector (p, h2)
```

So the rule for `#featured` beats the rule for `.notice` and the rule for `p`, even if the other rules appear later.

## Inheritance

Properties such as `color` and `font-family` often pass from a parent to its children. Properties such as `border`, `margin`, and `padding` generally do not.
