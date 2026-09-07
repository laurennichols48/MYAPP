# Basic Styling Reference

Use this when deciding what to try in Part 6.

## Color

```css
color: darkgreen;
background-color: lightyellow;
```

`color` changes text. `background-color` changes the space behind an element. Use a named color (`darkgreen`, `steelblue`) or a hex code (`#2e7d32`) — both work the same way.

## Spacing

```css
padding: 10px;
margin: 10px;
```

`padding` adds space *inside* an element, between its border and its content. `margin` adds space *outside* an element, pushing neighboring content away.

## Text

```css
font-size: 20px;
font-weight: bold;
text-align: center;
```

## Borders

```css
border: 1px solid gray;
```

A border needs all three parts to show up: a width (`1px`), a style (`solid`, `dashed`), and a color.

## A few combinations to try

| Goal | Declarations |
|---|---|
| Make a heading stand out | `color: darkgreen; font-weight: bold;` |
| Give a section breathing room | `padding: 10px;` |
| Center a piece of text | `text-align: center;` |
| Set an element apart from its neighbors | `border: 1px solid gray; padding: 10px;` |

Pick two or three properties rather than trying everything at once — Part 6 only asks for two styled elements.
