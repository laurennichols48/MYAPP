# Lab 10: Lecture

## Bootstrap and Responsive Website Build

## 1. What a Framework Provides

Bootstrap supplies:

- A responsive grid.
- Prewritten components.
- Utility classes.
- Consistent defaults.
- JavaScript for selected interactive components.

It does not choose your content, hierarchy, visual identity, or accessibility decisions.

## 2. Loading Bootstrap

The framework stylesheet belongs before custom CSS.

```html
<link href="bootstrap.css" rel="stylesheet">
<link rel="stylesheet" href="custom.css">
```

The supplied files use official Bootstrap 5.3.8 CDN links.

## 3. Containers

```html
<main class="container">
  ...
</main>
```

Containers center and constrain content with responsive horizontal spacing.

## 4. Rows and Columns

```html
<div class="row">
  <div class="col-12 col-md-6">...</div>
  <div class="col-12 col-md-6">...</div>
</div>
```

Columns use a 12-unit grid.

## 5. Mobile-First Breakpoints

`col-12 col-md-6` means:

- Full width at the smallest sizes.
- Half width at the medium breakpoint and above.

## 6. Utilities

Examples:

```text
p-3      padding
mb-4     margin-bottom
d-flex   display: flex
gap-3    gap
text-center
```

Utilities are useful for small, clear adjustments.

## 7. Components

Cards, navigation bars, buttons, and alerts provide tested structure and styling. Students still need meaningful HTML content and correct attributes.

## 8. JavaScript Components

A collapsing navigation bar requires the Bootstrap JavaScript bundle. Static grid and utility styles do not.

## 9. Customization

```css
:root {
  --portfolio-accent: #315e42;
}

.navbar {
  border-bottom: 3px solid var(--portfolio-accent);
}
```

Custom CSS should express the student’s visual system.

## 10. Avoid Framework Dependence Without Understanding

Students should be able to explain:

- Which class creates the layout.
- What changes at each breakpoint.
- Which styles come from Bootstrap.
- Which styles come from their own stylesheet.

## 11. Final Responsive Review

A responsive site should be tested for:

- Wrapping and stacking.
- Navigation.
- Image sizing.
- Text overflow.
- Keyboard use.
- Zoom.
- Heading and link clarity.

## Check for Understanding

Ask students to:

1. Decode `col-12 col-lg-4`.
2. Explain why custom CSS loads later.
3. Identify a component that needs JavaScript.
4. Name one design decision Bootstrap cannot make.
