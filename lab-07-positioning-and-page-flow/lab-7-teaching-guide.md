# Lab 7: Teaching Guide

## Positioning and Page Flow

## Purpose

Students investigate positioning as a controlled exception to normal flow. The lab explicitly prevents the common beginner misconception that absolute positioning is the standard method for arranging an entire page.

## Preparation

- Verify that the playground page is long enough to test fixed positioning.
- Test the broken badge at several viewport widths.
- Explain that students should restore the resource files after each investigation.
- Keep Flexbox and Grid as the preferred tools for later main layouts.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-position a "Featured" badge with `position: absolute` on a card, predicting aloud before refreshing. First omit `position: relative` on the parent card, show the badge escaping to the wrong part of the page, and think out loud about identifying the missing containing block. This is the exact bug in Part 3's repair challenge — save your real fix for after students attempt it themselves. A quick live float-and-clear demonstration fits well here too.

**Scaffold:** The positioning playground and broken badge challenge are the scaffold — students test and repair inside files you already built.

**Fade:** The Portfolio Checkpoint (one purposeful positioned detail) is the fade step.

## Suggested Timing

| Part | Time |
|---|---:|
| Block and inline flow | 8 minutes |
| Position values | 12 minutes |
| Repair the badge | 10 minutes |
| Float and clear | 7 minutes |
| Portfolio checkpoint | 9 minutes |
| Exit questions | 4 minutes |

## Answer Guidance

### Display

- Block elements usually begin on a new line and take available width.
- Inline elements participate inside a line and do not behave like full boxes for width and height.
- Inline-block elements sit inline while accepting box dimensions.

### Positioning

- Static: normal default flow.
- Relative: remains in flow; offsets from its normal location; can establish the containing block for an absolute child.
- Absolute: removed from normal flow; positioned relative to the nearest positioned ancestor, otherwise an initial containing block.
- Fixed: removed from normal flow and positioned relative to the viewport.

### Badge Repair

```css
.featured-card {
  position: relative;
}

.badge {
  position: absolute;
  top: 12px;
  right: 12px;
}
```

## Facilitation Guidance

Ask students after each test:

- Did surrounding content move into the element’s former space?
- What happens when the page scrolls?
- What containing block controls the offsets?
- Would this approach remain stable if text becomes longer?

## Common Student Difficulties

### Absolute element uses unexpected coordinates

Find the nearest ancestor whose `position` is not `static`.

### Relative element overlaps neighbors

Relative offsets move the visible box but preserve its original space. The offset can therefore create overlap.

### Fixed content covers page controls

Reduce its size, add page space, move it, or remove it. Fixed elements require careful testing.

### Float affects later content

Use `clear`, a flow-root container, or another containment method.

## Completion Check

Students should:

- Explain normal flow.
- Compare all four position values.
- Repair the badge using a positioned ancestor.
- Demonstrate one float and clear.
- Avoid absolute positioning for the main portfolio layout.
