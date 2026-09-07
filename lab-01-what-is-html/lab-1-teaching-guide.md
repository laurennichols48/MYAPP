# Lab 1: Teaching Guide

## Lab Files

- [Completed example HTML](resources/completed-example.html)
- [Broken HTML practice file](resources/broken-example.html)
- [Corrected HTML answer key](resources/corrected-example.html)
- [Student starter HTML](resources/starter.html)

## Purpose

This guided-discovery lab introduces HTML by allowing students to examine, modify, repair, and create HTML before receiving a formal lecture on the topic.

The instructor or teaching assistant should encourage students to make predictions, test their ideas, and explain what they observe rather than immediately giving them definitions.

## Materials and Preparation

Before the lab, prepare:

- A completed example HTML file.
- A broken HTML file containing common syntax and nesting errors.
- A blank or partially completed starter file.
- A computer with access to a web browser.
- A text editor or code editor, when available.
- Instructions for locating, opening, saving, and refreshing files on student computers.
- A backup browser-based HTML editor or other workaround if local code editors are unavailable.

Suggested files are included at the end of this document.

## Live Demonstration (Model → Scaffold → Fade)

**Placement recommendation:** Perform the short, procedural live demonstration after Parts 1 and 2 (after students have examined and made small changes to files). This prevents pre-teaching formal terms and preserves the guided-discovery flow.

**Model (procedural only):** Spend 2–3 minutes demonstrating the teacher workflow without explaining HTML concepts. Show how to open an HTML file, make a tiny change (one heading, one paragraph, one link), save the file, and refresh the browser so students see the result. Type at a natural pace without naming or defining tags, attributes, or elements. Ask students what they notice about the relationship between the code and the rendered page and invite brief observations.

**Scaffold:** The provided completed, broken, and starter files are the scaffold for the rest of the lab — students predict, test, and repair inside files you already built rather than starting from a blank page.

**Fade:** Part 5's original webpage is the fade step: no starter file, only the goals checklist.

## Suggested Pacing

| Section                              | Suggested Time |
| ------------------------------------ | -------------: |
| Introduction and file setup          |    3–5 minutes |
| Part 1: Examine an HTML Document     |    5–7 minutes |
| Part 2: Change, Predict, and Observe |   8–10 minutes |
| Part 3: Identify the Parts of HTML   |    7–8 minutes |
| Part 4: Repair Broken HTML           |   8–10 minutes |
| Part 5: Create Your First Webpage    |  10–12 minutes |
| Exit Questions                       |    3–5 minutes |

If students need more time, the final webpage or exit questions may be completed after the lab.

## Facilitation Guidance

### Opening the Lab

Begin with the central question:

> How does a browser turn plain text into a structured webpage?

Tell students that they do not need to understand every line of the document yet. Their goal is to notice patterns and test how changes affect the page. Avoid giving formal names or explanations of tags and attributes at this stage — those come after students have made observations in Parts 1 and 2.

### Part 1: Examine an HTML Document

Encourage students to compare individual lines in the source file with the corresponding content in the browser.

Prompt students with questions such as:

- Which parts of the file become visible text?
- Which parts give the browser instructions?
- What symbols appear repeatedly?
- What appears to mark the beginning and end of content?

Avoid formally defining every term before students have had time to observe the file.

### Part 2: Change, Predict, and Observe

Students should make one change at a time.

Remind them to:

1. Predict the result.
2. Make the change.
3. Save the file.
4. Refresh the browser.
5. Record what happened.

Expected results for common Part 2 changes:

- Change the text inside the `<h1>` element: the page displays new heading text in the same large style.
- Change `<h1>` to `<h2>`: the heading becomes visually smaller, showing how different tags affect appearance.
- Change a `<p>` tag to an `<h3>` tag: the paragraph text becomes a subheading style instead of normal paragraph text.
- Remove a closing tag: the browser may merge content, display the page differently, or show unexpected layout changes.
- Place one element inside another element: the content is nested and may appear inside the outer element, often changing structure or formatting.
- Change the visible text of a link: the text shown for the link changes, while the destination stays the same.
- Change the value inside `href`: the visible link text stays the same, but the link points to a new destination or may break if the target does not exist.

If a student changes several things at once, ask them to undo the changes and test one modification at a time.

### Part 3: Identify the Parts of HTML

Use the paragraph example before the link example.

The link example adds two new ideas:

- An opening tag can contain additional information.
- Some information affects how an element behaves without appearing as visible text.

Emphasize that:

- A **tag** is one part of the code, such as `<p>` or `</p>`.
- An **element** includes the opening tag, content, and closing tag.
- An **attribute** provides additional information inside an opening tag.
- An **attribute value** is the setting assigned to the attribute.

### Part 4: Repair Broken HTML

Students may notice that browsers still display content even when the HTML contains errors. Use this observation to explain that browsers often attempt to interpret imperfect HTML.

Do not suggest that browser error correction makes correct syntax unnecessary. Incorrect HTML can produce inconsistent results, make code difficult to understand, and create accessibility or maintenance problems.

Possible guiding questions:

- Where does the opening tag begin?
- Is there a matching closing tag?
- Are quotation marks paired?
- Is an element closed before its parent element closes?
- Is every list item inside a list?
- Does the link point to an existing or appropriate location?

### Part 5: Create Your First Webpage

Students may choose a simple topic such as:

- A personal introduction.
- A favorite hobby.
- A place they would like to visit.
- A school organization.
- A favorite book, movie, game, or activity.

The focus should remain on correct structure rather than visual appearance.

## Common Student Difficulties

### The browser does not show the latest changes

Ask the student to confirm that they:

- Saved the file.
- Refreshed the browser.
- Opened the correct copy of the file.

### The webpage displays code as text

Check for missing angle brackets or incorrectly typed tags.

### A link does not work

Check:

- Whether the `href` value is inside quotation marks.
- Whether the destination is spelled correctly.
- Whether a local file actually exists in the expected folder.

### Elements are incorrectly nested

Ask students to identify the outer element and make sure the inner element closes first.

Correct:

```html
<p>This is <strong>important</strong>.</p>
```

Incorrect:

```html
<p>This is <strong>important.</p></strong>
```

## Teaching Guide Answer Key

### Part 1: Possible Observations

- The `<h1>` line creates the largest heading.
- Text placed between opening and closing tags usually appears on the page.
- Tags, attributes, and document structure do not normally appear as visible text.
- Angle brackets mark HTML tags.
- A slash usually marks a closing tag.
- Opening and closing tags help show where an element begins and ends.

### Part 3: Example 1

| Part of the HTML                | Name             |
| ------------------------------- | ---------------- |
| `<p>`                           | Opening tag      |
| `Welcome to my website.`        | Content          |
| `</p>`                          | Closing tag      |
| `<p>Welcome to my website.</p>` | Complete element |

### Part 3: Example 2

| Part of the HTML                               | Name             |
| ---------------------------------------------- | ---------------- |
| `<a href="about.html">`                        | Opening tag      |
| `href`                                         | Attribute        |
| `"about.html"`                                 | Attribute value  |
| `Learn more about us`                          | Visible content  |
| `</a>`                                         | Closing tag      |
| `<a href="about.html">Learn more about us</a>` | Complete element |

Questions:

- **Which part appears as text?** `Learn more about us`
- **Which part tells the browser where the link should go?** The `href` attribute and its value.
- **Is `<a href="about.html">` an opening tag or complete element?** An opening tag.

### Try One More

| Component        | Answer                                                |
| ---------------- | ----------------------------------------------------- |
| Opening tag      | `<a href="schedule.html">`                            |
| Closing tag      | `</a>`                                                |
| Attribute        | `href`                                                |
| Attribute value  | `"schedule.html"`                                     |
| Visible content  | `View the class schedule`                             |
| Complete element | `<a href="schedule.html">View the class schedule</a>` |

Prediction:

- The webpage will display `View the class schedule`.
- The link will try to open `schedule.html`.

### Part 4: Broken File Corrections

The provided broken file includes examples of:

- A missing `</h1>` closing tag.
- A misspelled paragraph tag.
- Incorrectly nested emphasis tags.
- A missing quotation mark in a link.
- A broken or incomplete link destination.
- List items placed outside a `<ul>` or `<ol>` element.
- A missing paragraph closing tag.

Exact corrections are shown in the prepared resource section.

## Assessment Guidance

Students have met the lab goals when they can:

- Correctly label the parts of a paragraph and link element.
- Explain the role of a closing tag.
- Repair basic syntax and nesting errors.
- Create a browser-readable HTML page with all required elements, including an image.
- Explain at least one difference between source code and rendered output.

---
