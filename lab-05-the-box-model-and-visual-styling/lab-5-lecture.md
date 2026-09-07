# Lab 5: Lecture

## The Box Model and Visual Styling

## 1. Every Element Is a Box

From inside to outside:

```text
content → padding → border → margin
```

## 2. Content

The content area contains text, images, or child elements.

```css
.card {
  width: 240px;
}
```

By default, `width` describes the content area.

## 3. Padding

Padding creates space inside the border.

```css
.card {
  padding: 16px;
}
```

The element’s background extends through its padding.

## 4. Border

```css
.card {
  border: 1px solid #bbb;
}
```

The border surrounds the content and padding.

## 5. Margin

```css
.card {
  margin-bottom: 24px;
}
```

Margin creates space outside the border.

## 6. Total Width

With the default content-box model:

```text
total visible width =
content width + left/right padding + left/right border
```

Margins affect occupied space but are outside the visible box. This is why adding padding or a border can make a box wider than its neighbor even when the declared width stays the same.

## 7. Border Box

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

Now the declared width includes content, padding, and border. This makes layout behavior more predictable when you add spacing or borders around a box.

## 8. Typography

Readable typography depends on more than font choice.

```css
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #222;
}
```

## 9. Image Sizing

```css
img {
  max-width: 100%;
  height: auto;
}
```

This prevents an image from exceeding its container while preserving its aspect ratio.

## 10. Reusable Cards

```css
.project-card {
  padding: 24px;
  border: 1px solid #ccc;
  border-radius: 8px;
}
```

One shared class keeps related elements consistent.

## 11. Consistent Spacing

A small spacing scale produces stronger rhythm than unrelated values.

```text
8px, 16px, 24px, 32px
```

## 12. Footers

A footer should be structurally and visually distinct, but it should not compete with the main content.

## Check for Understanding

Ask students to:

1. Calculate a box’s visible width.
2. Explain why background color does not fill the margin.
3. Choose between padding and margin for a scenario.
4. Identify one repeated style that belongs in a class.
