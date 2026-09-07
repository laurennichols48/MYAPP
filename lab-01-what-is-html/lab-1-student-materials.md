# Lab 1: Student Materials

## Lab Files

- [Completed example HTML](resources/completed-example.html)
- [Broken HTML practice file](resources/broken-example.html)
- [Corrected HTML answer key](resources/corrected-example.html)
- [Student starter HTML](resources/starter.html)

## What Is HTML?

### Guiding Question

How does a browser turn plain text into a structured webpage?

### Lab Goals

After completing this lab, you will be able to:

- Identify the components of an HTML element.
- Explain the purpose of angle brackets and closing tags.
- Distinguish among an element, tag, attribute, attribute value, and content.
- Correctly nest HTML elements.
- Create a basic HTML document.
- Use headings, paragraphs, lists, links, and an image.
- Open an HTML file in a browser and inspect the result.

---

## Part 1: Examine an HTML Document

Open the provided completed HTML file in:

1. Your code editor.
2. Your web browser.

Compare the source code with the webpage displayed in the browser.

Answer the following questions:

1. Which line of code creates the largest text on the page?

   ***

2. Which parts of the code appear as visible text?

   ***

3. Which parts of the code do not appear directly on the page?

   ***

4. What patterns do you notice in the use of `<` and `>`?

   ***

5. Why do you think some tags contain a `/`?

   ***

6. How can you tell where one section of content begins and ends?

   ***

---

## Part 2: Change, Predict, and Observe

For each change:

1. Predict what will happen.
2. Make the change in the HTML file.
3. Save the file.
4. Refresh the browser.
5. Record the actual result.

| Change                                     | Prediction | Actual Result |
| ------------------------------------------ | ---------- | ------------- |
| Change the text inside the `<h1>` element. |            |               |
| Change both the opening `<h1>` tag and closing `</h1>` tag to `<h2>` and `</h2>`. |            |               |
| Change a `<p>` tag to an `<h3>` tag.       |            |               |
| Remove a closing tag.                      |            |               |
| Place one element inside another element.  |            |               |
| Change the visible text of a link.         |            |               |
| Change the value inside `href`.            |            |               |

After completing the table, restore the file to its original working form.

---

## Part 3: Identify the Parts of HTML

### Example 1: A Paragraph

Examine this HTML:

```html
<p>Welcome to my website.</p>
```

Use the word bank to label each part.

**Word bank:** opening tag, closing tag, content, complete element

| Part of the HTML                | Name |
| ------------------------------- | ---- |
| `<p>`                           |      |
| `Welcome to my website.`        |      |
| `</p>`                          |      |
| `<p>Welcome to my website.</p>` |      |

### Example 2: A Link

Examine this HTML:

```html
<a href="about.html">Learn more about us</a>
```

Use the word bank to label each part.

**Word bank:** opening tag, closing tag, attribute, attribute value, visible content, complete element

| Part of the HTML                               | Name |
| ---------------------------------------------- | ---- |
| `<a href="about.html">`                        |      |
| `href`                                         |      |
| `"about.html"`                                 |      |
| `Learn more about us`                          |      |
| `</a>`                                         |      |
| `<a href="about.html">Learn more about us</a>` |      |

Answer the following questions:

1. Which part of the link will appear as text on the webpage?

   ***

2. Which part tells the browser where the link should go?

   ***

3. Is `<a href="about.html">` an opening tag or a complete element?

   ***

### Try One More

Examine this HTML:

```html
<a href="schedule.html">View the class schedule</a>
```

Identify each component.

| Component        | Answer                               |
| ---------------- | ------------------------------------ |
| Opening tag      | ******\*\*******\_\_******\*\******* |
| Closing tag      | ******\*\*******\_\_******\*\******* |
| Attribute        | ******\*\*******\_\_******\*\******* |
| Attribute value  | ******\*\*******\_\_******\*\******* |
| Visible content  | ******\*\*******\_\_******\*\******* |
| Complete element | ******\*\*******\_\_******\*\******* |

Before opening the page in your browser, predict:

1. What text will appear on the webpage?

   ***

2. Where will the link try to take the user?

   ***

---

## Part 4: Repair Broken HTML

Open the provided broken HTML file.

The document contains several errors. Correct each error and refresh the page after making a change.

Look for:

- Missing closing tags.
- Incorrectly nested elements.
- Missing quotation marks.
- Misspelled tags.
- Broken links.
- List items that are not inside a list.

Record your corrections.

| Error | Correction | Why the Correction Was Necessary |
| ----- | ---------- | -------------------------------- |
|       |            |                                  |
|       |            |                                  |
|       |            |                                  |
|       |            |                                  |
|       |            |                                  |
|       |            |                                  |
|       |            |                                  |

Answer the following questions:

1. Did the browser display any content before all the errors were corrected?

   ***

2. What does this suggest about how browsers handle incorrect HTML?

   ***

3. Why is it still important to write correctly structured HTML?

   ***

---

## Part 5: Create Your First Webpage

Create a new file named:

```text
index.html
```

Your page may be about yourself, a hobby, a place, an organization, or another topic approved by your instructor.

Your webpage must include:

- One main heading using `<h1>`.
- At least one smaller heading.
- At least two paragraphs.
- One ordered or unordered list.
- At least one link.
- One image using `<img src="..." alt="...">`.
- Correctly nested elements.

Use the following structure as a starting point:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Webpage</title>
  </head>

  <body>
    <!-- Add your visible webpage content here -->
  </body>
</html>
```

Save the file and open it in a browser.

### Final Check

- [ ] All intended text appears.
- [ ] The heading sizes are different.
- [ ] The list displays correctly.
- [ ] The image appears on the page.
- [ ] The link works.
- [ ] All elements are correctly nested.
- [ ] The file is saved as `index.html`.

---

## Exit Questions

Answer each question in one or two sentences.

1. What is the difference between a tag and an element?

   ***

2. What is the purpose of a closing tag?

   ***

3. What does it mean for elements to be nested?

   ***

4. What is an attribute?

   ***

5. What does the `href` attribute control?

   ***

6. Identify one error you encountered and explain how you corrected it.

   ***

7. What is one question you still have about HTML?

   ***

---
