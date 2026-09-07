# Lab 4: Teaching Guide

## CSS Selectors and the Cascade

## Preparation

- Keep each HTML file beside its matching stylesheet.
- Verify the initial results before class.
- Encourage students to change one rule at a time.
- Do not begin with a full specificity formula. Let students first observe patterns.
- Confirm `selector-practice.html` shows the `<div class="notice">` and the footer link outside `<main>` — Part 3 depends on both.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-write a class selector and an ID selector that both target the same element, and predict aloud which one will win before refreshing. Then write `a[target=blank]` without quotes or the leading underscore, show that it silently does nothing, and think out loud about noticing a selector that "should" work but doesn't — the same kind of error in Part 7.

**Scaffold:** The selector-practice and cascade-investigation files are the scaffold — students test and predict inside files you already built.

**Fade:** Lab 4 has no portfolio checkpoint of its own; the fade continues into Lab 5's checkpoint.

## Suggested Timing

| Part | Time |
|---|---:|
| Selector matching | 8 minutes |
| Write selectors | 10 minutes |
| Combine selectors | 9 minutes |
| Source order investigation | 8 minutes |
| Specificity and inheritance | 10 minutes |
| Repair broken selectors | 8 minutes |
| Exit questions | 4 minutes |

## Selector Guidance

### Element Selector

```css
p {
  color: navy;
}
```

Affects every matching `<p>` element.

### Class Selector

```css
.notice {
  background-color: lightyellow;
}
```

A class can be reused.

### ID Selector

```css
#featured {
  border: 2px solid black;
}
```

An ID should be unique on a page. It is more specific than a class.

### Attribute Selector

```css
a[target="_blank"] {
  font-weight: bold;
}
```

Selects elements based on an attribute.

### Combining Selectors

Part 3 is discovery-first: students see `h1, .notice { color: blue; }` and `main a { color: blue; }` already working, predict and observe what each affects, then deliberately break the punctuation before you confirm anything. Don't front-load the comma/space definitions — let the "it stopped working" moment from the punctuation swap do the teaching.

What the swap should produce:

- `h1, .notice` → `h1 .notice` (comma removed, space added): this silently matches nothing, since no `.notice` element is nested inside `<h1>`. The rule stops affecting anything, which is the point — the meaning didn't degrade gracefully, it changed entirely.
- `main a` → `maina` (space removed): this selects a nonexistent `<maina>` element, so it also silently matches nothing.

Confirm only after students have written their own comma/space rule in their own words:

- A comma groups separate selectors so they receive the same styles.
- A space targets an element located inside another element.

This lab intentionally stops at grouped and descendant selectors. Compound selectors (`p.notice`, no space) are out of scope here — introduce them only if a later lab specifically needs that combination.

## Cascade Guidance

When two rules have equal specificity, the later rule wins.

When specificity differs, the more specific selector usually wins even if it appears earlier.

For this introductory lab, use the hierarchy:

1. ID selector
2. Class or attribute selector
3. Element selector

Inline styles are even more specific, but avoid adding them to this investigation unless students ask.

### Where Internal and External CSS Fit

Lab 3 introduced inline, internal, and external CSS as three locations. It's tempting to teach a clean three-step ladder (inline beats internal beats external), but that overstates it:

- Inline styles do have a real, elevated specificity and beat ordinary selector-based rules almost always.
- Internal and external stylesheets are not ordered relative to each other by type. When a rule in each targets the same element with equal specificity, whichever one appears later in the rendered HTML wins — the exact same source-order rule Part 4 investigates with two `p` rules in one file.

If a student asks "so which wins, internal or external?", the answer is "neither, by default — check which one loads later," not a fixed rule.

## Inheritance

Some properties, such as `color` and `font-family`, are commonly inherited by children. Others, such as `border`, usually are not.

## Reflection Guidance

Part 4's reflection ("what should you check first") is looking for: check whether another rule targets the same element with equal specificity and appears later in the file — not just whether the selector itself is "correct."

Part 5's reflection (does moving `p` to the bottom change the winner) is looking for: no, it wouldn't — `#featured` still wins because specificity is compared before source order is ever considered. Source order only breaks ties between rules of equal specificity.

## Answer Guidance

`broken-selectors.css` contains five errors:

| Broken selector | Intended target | Correction |
|---|---|---|
| `card { ... }` | Elements with class `card` | `.card { ... }` (missing the class dot selects a nonexistent `<card>` element) |
| `.featured-card { ... }` | Element with ID `featured-card` | `#featured-card { ... }` |
| `a[target=blank] { ... }` | Links opening in a new tab | `a[target="_blank"] { ... }` (missing quotes and the leading underscore) |
| `.h2 { ... }` | All `<h2>` elements | `h2 { ... }` (a class selector was used for an element selector) |
| `p .card { ... }` | Paragraphs inside `.card` sections | `.card p { ... }` (the descendant order is reversed — `p .card` looks for a `.card` element nested inside a `<p>`, which doesn't exist, so it silently matches nothing) |

## Completion Check

Students should:

- Write all four selector types.
- Combine selectors correctly (descendant and grouped) and explain the difference in their own words.
- Correctly predict at least two cascade outcomes.
- Explain one example of inheritance.
- Repair the challenge stylesheet, including the reversed descendant selector.
