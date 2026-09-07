# Lab 10: Teaching Guide

## Bootstrap and Responsive Website Build

## Purpose

Students use a framework as a productivity tool while preserving their own content, structure, and design choices. The lab consolidates semantic HTML, external CSS, selectors, the box model, Flexbox, Grid, responsiveness, and accessibility.

## Preparation

- Confirm internet access because the supplied starter uses Bootstrap 5.3.8 CDN files.
- Open the sampler before class and verify the navigation toggler.
- Provide a local fallback or allow students to continue with their existing CSS if the CDN is unavailable.
- Ask students to bring their portfolio folder and Figma mockups.
- Emphasize that Bootstrap is optional for parts already working well.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** Live-load `custom.css` before the Bootstrap CDN link in `<head>`, change a heading color, and show that Bootstrap's own styles still win. Move `custom.css` below the Bootstrap link and narrate why load order determines which rule applies — this is the exact "Custom CSS has no effect" difficulty listed below.

**Scaffold:** The component sampler and starter site are the scaffold — students decode and build inside files you already built.

**Fade:** The completed multi-page portfolio site is the fade step — the most independent build in the sequence.

## Suggested Timing

| Part | Time |
|---|---:|
| Inspect and decode classes | 8 minutes |
| Responsive columns | 6 minutes |
| Build responsive section | 9 minutes |
| Customize Bootstrap | 8 minutes |
| Complete multi-page build | 12 minutes |
| Responsive/accessibility review | 7 minutes |

The final polish may continue as homework. The lab should still end with a working, reviewable site.

## Facilitation Guidance

### Class Names

Teach students to read class names as compact instructions. Examples:

- `p-3`: padding.
- `mb-4`: bottom margin.
- `text-center`: text alignment.
- `col-md-6`: six grid units from the medium breakpoint upward.
- `d-flex`: display flex.

Students do not need to memorize every utility. They should use documentation and inspect examples.

### Responsive Grid

Bootstrap’s grid is mobile-first. Base classes apply at small widths; breakpoint classes apply from that breakpoint upward.

### Customization

The custom stylesheet should load after Bootstrap so later rules can override framework defaults when selectors permit. Students should not paste the entire framework into their project or edit CDN assets.

### Final Review

Require students to navigate the site rather than opening each page separately. Keyboard testing should include the navigation toggler and links.

## Answer Guidance

For `col-12 col-md-6`:

- At the smallest widths, the column uses 12 of 12 grid units.
- At the `md` breakpoint and above, it uses 6 of 12 grid units.
- Two such columns will usually stack on small screens.
- Two such columns will usually sit side by side at `md` and above.

## Common Student Difficulties

### Bootstrap does not appear

Check internet access, CDN links, integrity attributes, and whether the link appears in the head.

### Navbar toggler does not open

Verify that the JavaScript bundle is loaded before `</body>` and that target IDs match.

### Custom CSS has no effect

Check load order, selector matching, spelling, and whether a more specific framework rule is winning.

### Site looks identical to the sample

Require students to replace content, revise the visual system, and justify at least three design decisions from their mockup.

### Too many utility classes reduce readability

Move a repeated visual pattern into `custom.css` or a reusable class.

## Completion Check

Students should:

- Decode common classes.
- Build one responsive row.
- Customize at least five visual decisions.
- Complete the required pages.
- Test at several widths.
- Repair at least one accessibility or responsiveness issue.
