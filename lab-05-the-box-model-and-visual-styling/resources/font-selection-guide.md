# Font Selection Guide

Use this when filling out Part 4's typography choices.

## Pick one body font

The body font is used for most of the text on the page — it should be easy to read at small sizes.

Reliable choices already installed on most computers (no extra loading required):

- `Arial, Helvetica, sans-serif`
- `Georgia, 'Times New Roman', serif`
- `'Segoe UI', Verdana, sans-serif`

## Pick a heading font, or reuse the body font

Using the same font for headings and body text is a valid, common choice — it's one fewer decision and still looks consistent. If you want headings to stand out, pick a second font with a different feel (serif heading + sans-serif body, or a bolder sans-serif for both).

## Always write a fallback stack

Never set only one font name. Browsers may not have it installed, and without a fallback the browser picks its own default:

```css
body {
  font-family: Georgia, 'Times New Roman', serif;
}
```

The last value in the list should always be a generic family: `serif`, `sans-serif`, or `monospace`. That guarantees some readable font is used even if nothing earlier in the list is available.

## Using a font that isn't installed by default

Google Fonts (fonts.google.com) provides free web fonts with a `<link>` snippet you add to your page's `<head>`. If you use one, still include a fallback stack in case the font fails to load:

```css
body {
  font-family: 'Open Sans', Arial, sans-serif;
}
```

## Quick pairing rule of thumb

Two fonts is usually enough for a small site. If you're unsure, one serif and one sans-serif paired together reads as intentional; two similar sans-serif fonts next to each other often just look like a mistake.
