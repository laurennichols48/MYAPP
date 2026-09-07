# Lab 10: Student Materials

## Lab Files

- [Bootstrap component sampler](resources/bootstrap-components.html)
- [Bootstrap portfolio starter](resources/starter-site/index.html)
- [Completed reference site](resources/completed-site/index.html)
- [Portfolio review checklist](resources/portfolio-review-checklist.md)

## Bootstrap and Responsive Website Build

### Guiding Question

How can a framework speed up development without making every website look identical?

### Lab Goals

After completing this lab, you will be able to:

- Explain what Bootstrap provides.
- Decode common Bootstrap class names.
- Build responsive rows and columns.
- Use components and utility classes.
- Customize Bootstrap with a later stylesheet.
- Test a multi-page site at several widths.
- Complete the portfolio website.

> The supplied files use Bootstrap 5.3.8 from a CDN. An internet connection is required for the framework styles and JavaScript to load.

---

## Part 1: Inspect the Component Sampler

Open `bootstrap-components.html`.

Find examples of:

- A container.
- A responsive navigation bar.
- A grid row.
- Columns.
- Cards.
- Buttons.
- Spacing utilities.
- Text utilities.

Choose five class names and infer what they do before checking the rendered result.

| Class | Prediction | Observed result |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

---

## Part 2: Decode Responsive Columns

Examine:

```html
<div class="col-12 col-md-6">
```

Complete:

- At the smallest widths, the column uses ______ of 12 grid units.
- At the `md` breakpoint and above, it uses ______ of 12 grid units.
- Two such columns will usually __________________ on small screens.
- Two such columns will usually __________________ at `md` and above.

Resize the sampler and confirm your predictions.

---

## Part 3: Build a Responsive Section

Open the starter site.

On the homepage, complete the introduction row.

Requirements:

- Use a `.container`.
- Place content inside a `.row`.
- Use one text column and one image column.
- Stack them on small screens.
- Place them side by side at `md` or above.
- Use Bootstrap spacing utilities to prevent crowding.
- Keep the image responsive.

Suggested structure:

```html
<div class="row align-items-center g-4">
  <div class="col-12 col-md-7">
    ...
  </div>
  <div class="col-12 col-md-5">
    ...
  </div>
</div>
```

---

## Part 4: Customize Bootstrap

Bootstrap is the starting layer. Your stylesheet should load after it:

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">
<link rel="stylesheet" href="custom.css">
```

In `custom.css`, change at least:

- The body font.
- The main heading color.
- The navigation or footer treatment.
- Card borders or shadows.
- Link or button appearance.
- One repeated spacing decision.

Do not edit the Bootstrap CDN file.

Record one customization that overrides a framework style.

| Bootstrap/default appearance | Your custom rule | New appearance |
|---|---|---|
|  |  |  |

---

## Part 5: Complete the Multi-Page Website

Choose one path:

### Path A: Finish the Supplied Starter

Replace sample content and complete all three pages.

### Path B: Add Selected Bootstrap Patterns to Your Existing Portfolio

Keep your content and structure, then use Bootstrap only where it improves the build.

Required pages:

- Homepage.
- About page.
- Projects, interests, or experience page.

Required behavior:

- Navigation reaches every page.
- Content remains readable at narrow and wide widths.
- Project cards stack or reorganize responsively.
- Images resize without distortion.
- Custom styles make the site visually distinct.

---

## Part 6: Responsive and Accessibility Review

Use the supplied checklist.

Test approximately:

- Narrow phone width.
- Tablet or small laptop width.
- Wide desktop width.
- Browser zoom at 200%, when available.

Review:

- Page titles.
- Heading order.
- Link descriptions.
- Alternative text.
- Color contrast.
- Keyboard navigation.
- Visible focus.
- Content overflow.
- Navigation behavior.
- Consistency across pages.

Record the most important issue you found and fixed.

Issue: __________________________________________________________

Fix: ____________________________________________________________

---

## Final Deliverable Check

- [ ] Homepage, About page, and Projects/Interests/Experience page exist.
- [ ] Navigation works from every page.
- [ ] HTML is correctly nested and clearly organized.
- [ ] Classes are reused appropriately.
- [ ] IDs are unique and purposeful.
- [ ] Links are descriptive.
- [ ] Meaningful images have useful alternative text.
- [ ] The design is visually coherent.
- [ ] Layout works at narrow and wide widths.
- [ ] The final site reflects the student’s own content and design decisions.
- [ ] No component was copied without understanding and testing it.

---

## Exit Questions

1. What does Bootstrap save you from writing?

   ________________________________________________________________

2. What decisions does Bootstrap not make for you?

   ________________________________________________________________

3. What does `col-12 col-md-6` communicate?

   ________________________________________________________________

4. Why must `custom.css` load after Bootstrap?

   ________________________________________________________________

5. What is the strongest part of your final portfolio?

   ________________________________________________________________

6. What would you improve with more time?

   ________________________________________________________________
