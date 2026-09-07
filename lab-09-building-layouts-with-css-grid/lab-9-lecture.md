# Lab 9: Lecture

## Building Layouts with CSS Grid

## 1. Grid Is Two-Dimensional

Grid can coordinate rows and columns at the same time.

## 2. Grid Container and Items

```css
.project-grid {
  display: grid;
}
```

Direct children become grid items.

## 3. Defining Columns

```css
.project-grid {
  grid-template-columns: 1fr 1fr 1fr;
}
```

This creates three equal flexible columns.

## 4. Fraction Units

`fr` divides available space after fixed sizes and gaps are considered.

```css
grid-template-columns: 2fr 1fr;
```

The first flexible track receives twice the share of the second.

## 5. Gap

```css
.project-grid {
  gap: 24px;
}
```

The container controls spacing between tracks.

## 6. Spanning

```css
.featured {
  grid-column: span 2;
}
```

The item occupies two column tracks.

## 7. Responsive Track Repetition

```css
.project-grid {
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
}
```

The browser fits as many usable columns as the container allows.

## 8. Minimum and Maximum

`minmax(220px, 1fr)` means:

- Do not make the track smaller than 220px.
- Allow it to grow and share remaining space.

## 9. Media Queries for Bigger Changes

`auto-fit` and `minmax()` handle most responsive resizing on their own. A media query is for a larger, deliberate change, such as letting an item span tracks only once there is room:

```css
@media (min-width: 720px) {
  .featured {
    grid-column: span 2;
  }
}
```

The rule inside `{ }` is ignored below the given width and applied at or above it. `min-width` is the most common condition because it matches the mobile-first habit of styling the narrow layout first and adding rules for wider screens.

## 10. Grid Versus Flexbox

Use Flexbox when the main problem is arranging items along one axis. Use Grid when row and column relationships both matter.

They can be combined:

- Grid for the page or gallery.
- Flexbox inside a card or navigation bar.

## 11. Source Order Still Matters

Grid placement should not create a visual reading order that conflicts with the HTML, keyboard navigation, or narrow-screen sequence.

## Check for Understanding

Ask students to:

1. Predict the columns created by a rule.
2. Explain `fr`.
3. Describe what changes at a narrow width.
4. Choose Grid or Flexbox for a sample layout.
