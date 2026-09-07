# Lab 6: Teaching Guide

## Designing Before Coding

## Purpose

Students pause before adding more CSS and make deliberate content and design decisions. The lab treats design as communication, not decoration. Figma is used for low-cost experimentation before students commit to code.

## Preparation

- Verify both website examples at wide and narrow browser widths.
- Confirm students can access Figma or provide paper as a backup.
- Keep the mockup low fidelity.
- Ask students to bring the content they created in Labs 2–5.
- Pair students before the peer-review section.

## Live Demonstration (Model → Scaffold → Fade)

**Model:** This lab has no code to demonstrate, so model the design-critique skill instead: live-critique the ineffective example in front of the class, pointing at specific evidence (the all-caps heading, "CLICK HERE" link text) rather than saying it "looks bad." This models the evidence-based observation Part 1 and the Peer Design Check ask students to produce themselves.

**Scaffold:** The content-inventory and mockup-checklist files are the scaffold — students plan inside a structure you already built rather than a blank page.

**Fade:** The desktop and mobile Figma mockups are the fade step — no starter file at all, the most independent point in the sequence so far.

## Suggested Timing

| Part | Time |
|---|---:|
| Warm-up: what is visual hierarchy? | 3 minutes |
| Compare two websites | 10 minutes |
| Prioritize content | 6 minutes |
| Content inventory | 8 minutes |
| Figma mockup | 17 minutes |
| Peer design check | 6 minutes |
| Exit questions | 3 minutes |

## Facilitation Guidance

### Warm-Up

Don't skip this even with an experienced group — the menu/sign/poster example exists so "visual hierarchy" isn't a brand-new term the first time it's applied to a website. Take answers from a couple of students before moving on; there's no wrong answer here, the goal is just naming the experience they already have.

### Part 1

Avoid asking only which page students “like.” Require evidence connected to:

- Hierarchy.
- Contrast.
- Alignment.
- Repetition.
- Whitespace.
- Readability.
- Link clarity.

The ineffective page is intentionally exaggerated, but students should still explain the consequence of each choice.

### Part 2

If every item is priority one, ask what a visitor must know before deciding whether to continue. Encourage students to reduce competing calls to action.

### Part 3

Students often design empty rectangles without knowing what content belongs inside them. The inventory should come before the detailed mockup.

### Part 4

Recommended Figma scope:

- One homepage desktop frame.
- One homepage mobile frame.
- Labeled regions.
- Approximate hierarchy and spacing.
- No component library or complex prototype required.

Paper wireframes are an acceptable backup when Figma access fails. The learning goal is planning, not tool mastery.

### Part 5

Feedback must name a visible issue and a plausible revision. Reject comments such as “make it better” or “I like it.”

## Answer Guidance

Concrete evidence students should be able to find in the two examples:

| Principle | Ineffective example | Effective example |
|---|---|---|
| Visual hierarchy | All-caps headings and body text compete for attention; nothing stands out as most important | A large hero heading and an eyebrow label establish a clear reading order |
| Contrast | Emphasis relies only on capitalization, which is applied everywhere and stops meaning anything | Size, weight, and color are reserved for genuinely important elements |
| Alignment | Content is not visually grouped into a consistent column | A shared `.page-width` container aligns every section |
| Repetition | Each section header uses a different exaggerated style | Section headings, eyebrow labels, and spacing repeat predictably |
| Whitespace | Content is dense with little breathing room | Padding and spacing separate sections clearly |
| Link clarity | "CLICK HERE," "MORE," and "GO" do not describe the destination | "About," "Projects," and "Contact" state exactly where the link goes |

## Common Student Difficulties

### Students spend the entire lab choosing colors

Return them to grayscale or a limited palette. Ask them to solve order, grouping, and spacing first.

### Mockup contains placeholder text only

Require enough real content to estimate text length and section size.

### Mobile design is a scaled-down screenshot

Ask which sections should stack, move, simplify, or change spacing.

### Students design features they cannot build

Encourage ambition, but identify a minimum version that can be completed with HTML and CSS.

## Completion Check

Students should have:

- A completed content inventory.
- A desktop homepage mockup.
- A mobile homepage mockup.
- A documented peer recommendation.
- One visible revision based on feedback.
