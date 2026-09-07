# Lab 8: Lecture

## Building Layouts with Flexbox

## 1. Flexbox Is One-Dimensional

Flexbox arranges items primarily along one main axis at a time.

## 2. Flex Container and Items

```css
.navigation {
  display: flex;
}
```

The direct children of `.navigation` become flex items.

## 3. Main and Cross Axes

```css
.navigation {
  flex-direction: row;
}
```

In a row:

- Main axis: horizontal.
- Cross axis: vertical.

In a column, those directions switch.

## 4. Main-Axis Distribution

```css
.navigation {
  justify-content: space-between;
}
```

`justify-content` distributes space along the main axis.

## 5. Cross-Axis Alignment

```css
.navigation {
  align-items: center;
}
```

`align-items` aligns items across the cross axis.

## 6. Gap

```css
.navigation {
  gap: 16px;
}
```

`gap` creates consistent space between flex items without assigning margins to every child.

## 7. Wrapping

```css
.card-list {
  display: flex;
  flex-wrap: wrap;
}
```

Items can move to another line when they no longer fit.

## 8. Flexible Sizing

```css
.card {
  flex: 1 1 220px;
}
```

The three values represent growth, shrinkage, and preferred basis.

## 9. Source Order

A layout should remain understandable in HTML order. Visual rearrangement should not create a conflicting keyboard or reading sequence.

## 10. Good Flexbox Uses

- Navigation bars.
- Button groups.
- Rows of summary information.
- Image-and-text sections.
- Card groups that flow primarily in one direction.

## Check for Understanding

Ask students to identify:

1. The flex container in a sample.
2. The main axis.
3. A property for repeated spacing.
4. A property that permits wrapping.
