# Lab 7: Lecture

## Positioning and Page Flow

## 1. Normal Flow

Without special layout rules, the browser places elements according to their document order and formatting behavior.

## 2. Block and Inline

Block elements generally form vertical boxes. Inline elements participate inside lines of text.

```css
span {
  display: inline;
}

section {
  display: block;
}
```

## 3. Static Positioning

```css
.box {
  position: static;
}
```

Static is the default. Offset properties such as `top` do not reposition a static element.

## 4. Relative Positioning

```css
.card {
  position: relative;
}
```

The element remains in normal flow. It can be offset and can establish a reference for an absolutely positioned child.

## 5. Absolute Positioning

```css
.badge {
  position: absolute;
  top: 8px;
  right: 8px;
}
```

The element leaves normal flow. Its offsets use the nearest positioned ancestor.

## 6. Fixed Positioning

```css
.back-to-top {
  position: fixed;
  right: 16px;
  bottom: 16px;
}
```

A fixed element stays relative to the viewport during scrolling.

## 7. Positioning Is Not a Full Layout System

Manually assigning coordinates breaks when:

- Text length changes.
- The viewport changes.
- Users zoom.
- Content is translated.
- New sections are added.

Use Flexbox or Grid for the main layout.

## 8. Floats

```css
.profile-image {
  float: left;
  margin: 0 16px 8px 0;
}
```

Floats were designed to allow content such as text to wrap around an element.

## 9. Clearing

```css
.next-section {
  clear: both;
}
```

Clearing prevents a later element from continuing beside a float.

## Check for Understanding

Ask students to choose a technique for:

1. A badge inside a card.
2. A page-wide project layout.
3. Text wrapping around a small image.
4. A persistent back-to-top control.
