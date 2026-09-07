# Lab 3: Teaching Guide

## Why Do We Need CSS?

## Preparation

- Keep every resource in the same folder.
- Confirm that `external-example.html` loads `styles.css`.
- Confirm that `broken-stylesheet-link.html` initially appears unstyled.
- Remind students to save both HTML and CSS before refreshing.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-refactor one repeated inline style, such as `color: darkgreen;`, into a `<style>` rule, narrating why you're moving it. Then deliberately point the `<link>` at the wrong filename (`style.css` instead of `styles.css`), refresh, and think out loud about diagnosing an unstyled page — the same bug students meet in Part 5.

**Scaffold:** The three comparison files and refactor starter file are the scaffold — students observe, refactor, and repair inside files you already built.

**Fade:** The Portfolio Checkpoint (one shared external stylesheet) is the fade step.

## Suggested Timing

| Part | Time |
|---|---:|
| Compare styling methods | 8 minutes |
| Change and observe | 8 minutes |
| Find repetition | 6 minutes |
| Refactor | 15 minutes |
| Repair stylesheet link | 6 minutes |
| Exit questions | 4 minutes |

## Facilitation Notes

### Three Styling Methods

- Inline CSS appears inside a `style` attribute.
- Internal CSS appears in a `<style>` element in `<head>`.
- External CSS appears in a separate `.css` file.

### CSS Rule Anatomy

```css
h1 {
  color: darkgreen;
}
```

- Selector: `h1`
- Property: `color`
- Value: `darkgreen`
- Declaration: `color: darkgreen;`

### Refactoring

Students first move styles into a `<style>` block, then into `refactor-styles.css`.

Correct connection:

```html
<link rel="stylesheet" href="refactor-styles.css">
```

### Main Discovery

Inline CSS is quick for one element but repetitive. Internal CSS reduces repetition on one page. External CSS can be shared across several pages.

### Looking Ahead

Students now know three places CSS can live. Exit question 6 previews Lab 4: these locations also have a pecking order when their rules conflict — inline beats internal and external, which are otherwise decided by ordinary source order. Don't resolve the question now; let students guess and carry it into Lab 4.

## Answer Guidance

- `broken-stylesheet-link.html` links to `style.css`, but the file on disk is named `styles.css`. Correcting the `href` value to `styles.css` restores the styling.
- The page appears unstyled, not broken, before the link is repaired — this is useful evidence that a missing stylesheet does not stop the HTML from rendering.
- Students should count the same repeated declarations in `refactor-starter.html` (commonly `color: darkgreen;`, `background-color: honeydew;`, and `padding: 10px;`) and notice that each copy must be edited separately if one value changes.

## Completion Check

Students should:

- Identify all three methods.
- Make a visible style change.
- Link a working stylesheet.
- Remove repeated inline styles.
- Repair the broken `<link>` element.
