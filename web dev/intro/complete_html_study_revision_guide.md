# HTML Master Study & Revision Guide
> A complete, pedagogy-focused reference guide designed for students.

---

## Table of Contents
1. [Module 1: Introduction to HTML & Web Fundamentals](#module-1-introduction-to-html--web-fundamentals)
2. [Module 2: HTML Text Formatting, Hierarchy & Comments](#module-2-html-text-formatting-hierarchy--comments)
3. [Module 3: Lists & Hierarchical Data](#module-3-lists--hierarchical-data)
4. [Module 4: File Paths, Hyperlinks & HTML Attributes](#module-4-file-paths-hyperlinks--html-attributes)
5. [Module 5: Self-Closing Tags & Media (Images & SVGs)](#module-5-self-closing-tags--media-images--svgs)
6. [Module 6: HTML Forms & User Input](#module-6-html-forms--user-input)
7. [Module 7: Containers & Semantic HTML Layouts](#module-7-containers--semantic-html-layouts)
8. [Module 8: HTML Tables](#module-8-html-tables)
9. [Module 9: Scientific, Academic & Media Notation](#module-9-scientific-academic--media-notation)
10. [Quick-Reference Syntax Cheatsheet](#quick-reference-syntax-cheatsheet)

---

# Module 1: Introduction to HTML & Web Fundamentals

## 1.1 What is HTML?
**HTML** stands for **HyperText Markup Language**:
* **HyperText**: Text that links to other pieces of text or other web documents (both internal and external pages).
* **Markup**: A standardized syntax of tags used to define and annotate page structure, formatting, and layout.
* **Language**: A formal system of rules and tags interpreted by web browsers.

### The Core Web Triad
A webpage is assembled from three core technologies:
```
+-------------------------------------------------------------+
|                          WEBPAGE                            |
|                                                             |
|  +--------------------+  +------------------+  +---------+  |
|  |     HTML (5)       |  |     CSS (3)      |  | JS (ES) |  |
|  |--------------------|  |------------------|  |---------|  |
|  | • Structure        |  | • Styling        |  | • Logic |  |
|  | • Content skeleton |  | • Colors, fonts  |  | • Events|  |
|  | • Semantic markup  |  | • Visual layout  |  | • APIs  |  |
|  +--------------------+  +------------------+  +---------+  |
+-------------------------------------------------------------+
```

---

## 1.2 Anatomy of an HTML Element

An HTML element typically consists of an **opening tag**, the **content**, and a **closing tag**.

```
       Opening Tag                  Content                  Closing Tag
   +-----------------+        +------------------+        +---------------+
   |   <p class="...">        |  I am a paragraph|        |     </p>      |
   +-----------------+        +------------------+        +---------------+
    |   |           |                                       |   |   |
    |   |           +-- Attribute                           |   |   +-- Right Angle Bracket
    |   +-------------- Tag Name                            |   +------ Tag Name
    +------------------ Left Angle Bracket                  +---------- Forward Slash (indicates close)
   
   |<--------------------------- FULL HTML ELEMENT ---------------------->|
```

* **Left & Right Angle Brackets (`<`, `>`):** Enclose tag identifiers.
* **Tag Name:** Informs the browser what type of content is being wrapped (e.g., `p`, `h1`, `div`).
* **Forward Slash (`/`):** Signals the closure of an element.
* **Element:** The combined entity of opening tag, attributes, content, and closing tag.

---

## 1.3 HTML Files & Best Practices

### File Extensions
Every digital asset has a file extension defining how data is encoded and interpreted:
* **Documents:** `.txt`, `.pdf`, `.doc`
* **Images:** `.jpg`, `.png`, `.svg`, `.webp`
* **Audio / Video:** `.mp3`, `.wav`, `.mp4`, `.mov`
* **Web:** `.html` (or `.htm`)

### Editing vs. Viewing
* **Code Editor (Authoring):** Tools like VS Code, Sublime Text, or WebStorm are used to write and edit raw source code.
* **Browser (Rendering):** Browsers (Google Chrome, Firefox, Safari, Edge) parse the HTML tags and paint the visual interface.

### File Naming Conventions
* **Always use lowercase letters:** Prevents case-sensitivity bugs across Unix, Linux, and Windows servers.
* **Hyphen-separated words (kebab-case):** Use `about-us.html` or `user-profile.html` instead of `AboutUs.html` or `about_us.html`.
* **No spaces or special characters:** Spaces become `%20` in URLs and can cause broken links.

---

## 1.4 The HTML5 Boilerplate Structure

Browsers require a foundational scaffolding to parse and render documents reliably without entering "quirks mode".

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
  </head>
  <body>
    <h1>Welcome to My Website</h1>
    <p>This is visible page content.</p>
  </body>
</html>
```

### Breakdown of Boilerplate Elements:
1. `<!DOCTYPE html>`:
   * **Declaration, not an element.**
   * Informs the browser that this is an **HTML5** document.
   * *Historical comparison:* HTML 4.01 required a long DTD (Document Type Definition) string:
     `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`.
2. `<html lang="en">`:
   * The **root element** enclosing all page content.
   * `lang="en"` indicates English as the primary document language (essential for search engine indexing and screen reader pronunciation).
3. `<head>`:
   * Contains **metadata**—configuration data *about* the document that is not visually rendered in the viewport.
   * Analogy: File properties/metadata in PowerPoint or Word (Author, Created Date, Subject).
4. `<meta charset="UTF-8">`:
   * Specifies character encoding. UTF-8 supports virtually all human languages, numbers, punctuation, and emojis.
5. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`:
   * Sets viewport rules for responsive design across mobile, tablet, and desktop devices.
6. `<title>`:
   * Defines the text displayed on browser tabs, bookmarks, and search engine results.
7. `<body>`:
   * Contains **all visible elements** displayed directly on the screen (headings, text, buttons, graphics, forms).

---

## 1.5 Hierarchy, Nesting, and Indentation

HTML uses a parent-child hierarchical tree structure (similar to Russian Matryoshka nesting dolls):

```
       [html]                  <-- Grandparent / Root
       /    \
   [head]  [body]              <-- Siblings (Children of html)
     |       |
  [title]   [p]                <-- Children of head and body
```

### Indentation Rules
Indentation does not affect how the browser renders HTML, but it is **mandatory for human readability and maintainability**:
* Always indent child elements inside their parent container (typically 2 spaces or 4 spaces).
* Keep opening and closing parent tags at the identical column level.

---

# Module 2: HTML Text Formatting, Hierarchy & Comments

## 2.1 Headings (`<h1>` to `<h6>`)
Headings communicate semantic structure and document hierarchy. They are not merely for making text larger or bolder.

```html
<h1>Level 1: Main Page Topic</h1>
<h2>Level 2: Major Section Heading</h2>
<h3>Level 3: Sub-section Heading</h3>
<h4>Level 4: Grouping Sub-heading</h4>
<h5>Level 5: Minor Sub-heading</h5>
<h6>Level 6: Lowest Level Heading</h6>
```

### Heading Hierarchy Rules:
1. **The Single `<h1>` Rule:** Each page must contain exactly **one** `<h1>` tag representing the overarching topic/title (crucial for SEO and screen readers).
2. **Never skip levels:** Do not jump directly from an `<h1>` to an `<h3>`. Descend step-by-step (`<h1>` $\rightarrow$ `<h2>` $\rightarrow$ `<h3>`).
3. **Use for structure, not styling:** Never choose a heading level simply because you want text to appear large or bold; use CSS for appearance.

---

## 2.2 Paragraphs (`<p>`)
Paragraphs are block-level structural text blocks used to organize continuous reading material.

```html
<p>
  Unlock the simplicity of online journaling. Say goodbye to the hassle
  of pen and paper and hello to effortless productivity.
</p>
```
* Can hold a single sentence or multiple sentences.
* Browsers automatically append default top and bottom margins to separate paragraphs visually.

---

## 2.3 HTML Comments
Comments are developer notes stored directly inside the code that are completely ignored by the browser renderer.

### Syntax
```html
<!-- This is a single-line comment -->

<!--
  Multi-line Comment:
  TODO: Replace this mock section with API call.
  Author: Dev Team
-->
```

* **Opening delimiter:** `<!--`
* **Closing delimiter:** `-->`
* **Keyboard Shortcuts:**
  * macOS: `Cmd + /`
  * Windows / Linux: `Ctrl + /`

### Primary Use Cases:
1. **Notes to Self / To-Do Items:** Reminders for future code improvements (e.g., `<!-- TODO: Add validation here -->`).
2. **Section Demarcation:** Outlining large code files (e.g., `<!-- ============ HERO SECTION ============ -->`).
3. **Code Debugging / Toggling:** Disabling code lines without deleting them.

---

## 2.4 Chrome Developer Tools (DevTools)
Built-in developer software inside Google Chrome used to test, debug, and optimize web applications:
* **Elements Tab:** Live inspection and real-time editing of the DOM (Document Object Model) and CSS styles.
* **Console Tab:** Log errors, check output, execute JavaScript snippets.
* **Network Tab:** Inspect incoming/outgoing HTTP requests, images, scripts, latency, and status codes.

---

# Module 3: Lists & Hierarchical Data

Lists organize items in concise, structured formats. HTML supports two primary list types plus nested combinations.

## 3.1 Ordered Lists (`<ol>`)
Used when the sequence of items is critical (rankings, recipes, step-by-step guides, formal reference notes).

```html
<ol>
  <li>Open the project directory</li>
  <li>Install dependencies via terminal</li>
  <li>Start the development server</li>
</ol>
```
* Rendered by default with numerical decimal markers (`1.`, `2.`, `3.`).

---

## 3.2 Unordered Lists (`<ul>`)
Used when the sequence of items does not change the core meaning (features, bullet points, navigation menus).

```html
<ul>
  <li>Instant Data Sync</li>
  <li>End-to-End Encryption</li>
  <li>Offline Availability</li>
</ul>
```
* Rendered by default with circular bullets (`•`).

---

## 3.3 Nested Lists
Lists placed inside other lists to represent multi-tiered menus, categories, or subtasks.

```html
<ol>
  <li>
    Planning Phase
    <ul>
      <li>Determine budget</li>
      <li>Establish target launch dates</li>
    </ul>
  </li>
  <li>
    Design Phase
    <ul>
      <li>Create wireframes</li>
      <li>Assemble UI design system</li>
    </ul>
  </li>
</ol>
```

### Nesting Matrix
| Outer Type | Inner Type | Example Visual Output | Typical Use Case |
| :--- | :--- | :--- | :--- |
| **Ordered** | **Ordered** | 1. Step 1<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Sub-step A<br>2. Step 2 | Legal clauses, algorithmic steps |
| **Ordered** | **Unordered** | 1. Phase 1<br>&nbsp;&nbsp;&nbsp;&nbsp;• Note item<br>2. Phase 2 | Phased timelines with bullet points |
| **Unordered** | **Ordered** | • Category A<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Rank 1<br>• Category B | Categories with ranked sub-items |
| **Unordered** | **Unordered** | • Main Topic<br>&nbsp;&nbsp;&nbsp;&nbsp;• Subtopic<br>• Next Topic | Multi-level site navigation / menus |

> **Critical Rule:** The nested `<ul>` or `<ol>` **must** sit directly inside a parent `<li>` tag, never directly between `<li>` tags.

---

# Module 4: File Paths, Hyperlinks & HTML Attributes

## 4.1 Directory Structures & File Paths
Understanding file systems is essential for linking files, images, scripts, and stylesheets.

```
[Project Root]
 ├── index.html
 ├── register.html
 └── images/
      ├── logo.png
      └── banner.jpg
```

### Absolute vs. Relative Paths
* **Absolute File Paths:** State the entire path starting from the machine's root drive:
  * Example: `/Users/username/Desktop/Project/images/logo.png`
  * *Disadvantage:* Breaks as soon as you upload the project to a web server or share it with another developer.
* **Relative File Paths:** State the location relative to the file where the code is written:
  * Same folder: `register.html`
  * Subfolder: `images/logo.png`
  * Up one directory: `../index.html`
  * *Advantage:* Highly portable; functions identically across local machines and cloud servers.

---

## 4.2 Hyperlinks (`<a>` Tag)
Hyperlinks navigate users across documents, pages, or sections.

```html
<a href="https://www.example.com" target="_blank" rel="noopener noreferrer">Visit Example</a>
```

### Anatomy of an Attribute
Attributes provide supplemental instructions or data to an HTML tag.
```
         Tag Name   Attribute Name      Attribute Value           Anchor Text
            |              |                   |                       |
            v              v                   v                       v
          < a             href = "https://example.com" >       Click Here      </a>
```

### Link Variations:
1. **External Absolute Link:**
   `<a href="https://google.com">Google</a>`
2. **Internal Relative Link:**
   `<a href="about.html">About Us</a>`
3. **List Navigation Pattern:**
   ```html
   <ul>
     <li><a href="index.html">Home</a></li>
     <li><a href="login.html">Login</a></li>
     <li><a href="register.html">Register</a></li>
   </ul>
   ```

---

## 4.3 The `id` Attribute & In-Page Anchor Links
The `id` attribute assign an identifier to an element.

### Strict Rules for IDs:
* **Must be unique:** An `id` name can only appear **once** per HTML document.
* Case-sensitive, lowercase recommended, no spaces.

### Tri-Purpose of `id`:
1. **In-Page Anchor Linking (HTML):** Directs the browser viewport to a specific section on the page.
2. **CSS Styling Hook:** Targets a unique element (`#main-header { color: blue; }`).
3. **JavaScript DOM Hook:** Retrieves elements (`document.getElementById('target')`).

### Anchor Linking Syntax:
```html
<!-- Trigger Link -->
<a href="#pricing-section">Jump to Pricing</a>

<!-- Long Content ... -->

<!-- Target Destination -->
<section id="pricing-section">
  <h2>Our Pricing Plans</h2>
</section>
```

---

# Module 5: Self-Closing Tags & Media (Images & SVGs)

## 5.1 Self-Closing (Void) Tags
Normal tags wrap content (`<p>Content</p>`). **Void elements** cannot contain content or child nodes. Therefore, they do not have a closing tag.

### Common Void Elements:
* `<meta>`: Document metadata.
* `<link>`: External resources (e.g., CSS stylesheets).
* `<img>`: Visual image embeds.
* `<input>`: Form user input fields.
* `<br>`: Single line break.
* `<hr>`: Thematic divider / horizontal rule.
* `<source>`, `<track>`, `<wbr>`, `<area>`, `<base>`, `<col>`, `<embed>`, `<param>`.

> **Syntax Note:** Both `<br>` (HTML5 standard) and `<br />` (XHTML legacy) are valid and recognized by modern browsers.

---

## 5.2 The Image Element (`<img>`)
Images are embedded using the self-closing `<img>` tag:

```html
<!-- External Source -->
<img src="https://images.com/sample.jpg" alt="A golden retriever running on grass">

<!-- Local Relative Path -->
<img src="images/logo.png" alt="Company Official Logo">
```

### Crucial Attributes:
* **`src` (Source):** The URL or relative path locating the image file.
* **`alt` (Alternative Text):**
  * Read aloud by screen readers for visually impaired users.
  * Rendered inside the viewport if the network fails to load the image.
  * Essential for search engine image indexing (SEO).

---

## 5.3 Raster vs. Vector Graphic Formats

| Attribute | Raster Graphics (`.jpg`, `.png`, `.webp`) | Vector Graphics (`.svg`) |
| :--- | :--- | :--- |
| **Composition** | Made of fixed grids of pixels. | Made of mathematical lines, curves, and shapes. |
| **Scalability** | Pixelates and blurs when scaled up. | Scales infinitely without quality degradation. |
| **File Sizes** | Heavy for complex high-res graphics. | Tiny file size for logos, icons, and illustrations. |
| **Best Used For** | Photographs, complex scenic artwork. | Logos, UI icons, line graphs, geometric art. |

### Working with SVGs in HTML:
1. **As an external image:**
   ```html
   <img src="images/icon.svg" alt="Search Icon">
   ```
2. **Inline `<svg>` (direct DOM manipulation & CSS styling):**
   ```html
   <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
     <path d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
   </svg>
   ```

---

# Module 6: HTML Forms & User Input

Forms allow web applications to collect information from users and transmit it to web servers for processing.

```
       USER BROWSER                                      BACKEND SERVER
+------------------------+                             +-----------------+
|  [Name: ____________]  |   HTTP GET/POST Request     |                 |
|  [Email: ___________]  | --------------------------> |  Database / API |
|  [ Submit Button ]     | <-------------------------- |                 |
+------------------------+      JSON / HTML Response   +-----------------+
```

## 6.1 The `<form>` Element & Transport Methods

```html
<form action="/api/v1/journals" method="POST">
  <!-- Form input controls go here -->
</form>
```

### Core Attributes:
* **`action`:** The destination URL/endpoint that will process the submitted payload.
* **`method`:** The HTTP verb defining how data is sent:

| HTTP Method | Data Placement | Security | URL Display | Caching / Bookmarking |
| :--- | :--- | :--- | :--- | :--- |
| **`GET`** | Attached to URL (Query String): `?key=val` | Low (Never use for passwords) | Visible in address bar | Can be bookmarked & cached |
| **`POST`** | Encapsulated in the HTTP Request Body | High | Hidden from URL | Cannot be bookmarked directly |

---

## 6.2 The Accessible `<label>` and `<input>` Pair

Every input field must be paired with a `<label>` to ensure usability and accessibility.

```html
<label for="user-email">Email Address</label>
<input 
  type="email" 
  id="user-email" 
  name="email" 
  placeholder="name@example.com" 
  required
>
```

### Critical Pairing Rule:
* The `for` attribute on the `<label>` **must exactly match** the `id` value on the `<input>`.
* **Benefit:** Clicking the text of the `<label>` automatically focuses the corresponding input field (vital for checkboxes/radio buttons on mobile).

---

## 6.3 Input Types & Attributes

### Common `type` Values:
* `type="text"`: Standard single-line text input.
* `type="password"`: Masked text input (characters hidden with dots).
* `type="email"`: Verifies basic email syntax automatically.
* `type="date"`: Built-in calendar picker.
* `type="checkbox"`: Independent multi-select toggles.
* `type="radio"`: Mutually exclusive single-choice selections.
* `type="submit"`: Triggers form submission.

### Input Control Attributes:
* `name`: **Mandatory for backend submission.** Defines the key in the transmitted key-value pair (`email=user@test.com`).
* `placeholder`: Temporary ghost text suggesting expected format.
* `value`: Predefined or current programmatic value.
* `required`: Prevents form submission if empty.
* `disabled`: Grayed out, uneditable, ignored on submission.
* `maxlength` / `minlength`: Text length restrictions.
* `max` / `min`: Numerical or date bounds.

---

## 6.4 Specialized Form Controls

### Multi-line Text: `<textarea>`
Used for long-form comments, blog entries, or messages. Requires a closing tag.

```html
<label for="entry-content">Journal Entry</label>
<textarea 
  id="entry-content" 
  name="entry" 
  rows="6" 
  cols="40" 
  placeholder="Write your thoughts..."
></textarea>
```

### Dropdown Menu: `<select>` and `<option>`
Presents a compact list of selectable choices.

```html
<label for="category">Category</label>
<select id="category" name="category">
  <option value="task">Task Item</option>
  <option value="note">Reference Note</option>
  <option value="idea" selected>Creative Idea</option>
</select>
```

### Checkboxes vs. Radio Buttons:
```html
<!-- Checkboxes (Multiple Selections Allowed) -->
<fieldset>
  <legend>Select Toppings</legend>
  <input type="checkbox" id="top-cheese" name="cheese" value="yes">
  <label for="top-cheese">Extra Cheese</label>
  
  <input type="checkbox" id="top-olives" name="olives" value="yes">
  <label for="top-olives">Olives</label>
</fieldset>

<!-- Radio Buttons (Single Selection Only: Shared `name`) -->
<fieldset>
  <legend>Select Pizza Size</legend>
  <input type="radio" id="size-sm" name="size" value="s">
  <label for="size-sm">Small</label>

  <input type="radio" id="size-md" name="size" value="m" checked>
  <label for="size-md">Medium</label>

  <input type="radio" id="size-lg" name="size" value="l">
  <label for="size-lg">Large</label>
</fieldset>
```
> **Radio Button Rule:** Radio buttons belong to the same group if and only if they share an identical `name` attribute.

---

## 6.5 Buttons: `<button>` vs. Anchor Links `<a>`

* **`<a href="...">`:** Used for **navigation** (taking the user to another page or section).
* **`<button type="submit">`:** Used to perform an **action** (submitting form data, triggering UI actions).

```html
<!-- Complete Accessible Form Pattern -->
<form action="/submit-feedback" method="POST">
  <label for="client-name">Full Name</label>
  <input type="text" id="client-name" name="name" required>

  <label for="client-feedback">Your Thoughts</label>
  <textarea id="client-feedback" name="feedback" rows="4"></textarea>

  <button type="submit">Send Feedback</button>
</form>
```

---

# Module 7: Containers & Semantic HTML Layouts

## 7.1 Block-Level vs. Inline Elements

```
Block Elements: Take 100% of available line width, start on a new line.
+-------------------------------------------------------------+
| <div>, <p>, <h1>-<h6>, <section>, <header>, <article>        |
+-------------------------------------------------------------+

Inline Elements: Take only the width of their content, stay in-line.
+-------------------------------------------------------------+
| <span>Word</span>, <a href="#">Link</a>, <strong>Bold</strong>|
+-------------------------------------------------------------+
```

### Generic Containers:
* **`<div>` (Division):** Generic block container. Provides zero inherent semantic meaning. Used solely for CSS grouping, layout grids, and wrappers.
* **`<span>`:** Generic inline container used to style or manipulate a specific slice of text inside a paragraph or heading.

```html
<!-- Generic Container Usage -->
<div class="user-card">
  <h2>John Doe</h2>
  <p>Status: <span class="active-badge">Online</span></p>
</div>
```

---

## 7.2 Semantic HTML Architecture
**Semantic HTML** means using tags that describe their human and machine-readable **meaning**, rather than just how they look.

### Why Semantics Matter:
1. **Accessibility (a11y):** Assistive technologies (screen readers) rely on semantic landmarks to help visually impaired users navigate quickly.
2. **SEO Optimization:** Search engines prioritize content housed within proper semantic tags (`<article>`, `<main>`) over generic `<div>` soup.
3. **Developer Maintainability:** Clean structure makes onboarding, refactoring, and code comprehension much faster.

---

## 7.3 Semantic Layout Blueprint

```
+-------------------------------------------------------------+
|                          <header>                           |
|  +--------------------+  +-------------------------------+  |
|  |     [Logo]         |  |             <nav>             |  |
|  +--------------------+  +-------------------------------+  |
+-------------------------------------------------------------+
|                           <main>                            |
|  +-------------------------------------+  +---------------+ |
|  |             <section>               |  |    <aside>    | |
|  |  +-------------------------------+  |  |               | |
|  |  |           <article>           |  |  | • Sidebar     | |
|  |  |  <h1>Title</h1>               |  |  | • Ads         | |
|  |  |  <p>Content text...</p>       |  |  | • Related     | |
|  |  +-------------------------------+  |  |   Links       | |
|  +-------------------------------------+  +---------------+ |
+-------------------------------------------------------------+
|                          <footer>                           |
|  • Copyright Notice  • Privacy Policy  • Contact Information|
+-------------------------------------------------------------+
```

### Semantic Tag Definitions:
* `<header>`: Introductory section of a page or individual `<article>`; typically holds logos, headings, and global navigation.
* `<nav>`: Block of major navigational links.
* `<main>`: The unique, primary content of the document. **Only one `<main>` per page.**
* `<section>`: A thematic grouping of content, almost always accompanied by its own heading (`<h2>`-`<h6>`).
* `<article>`: A self-contained, independent composition reusable in syndication (e.g., blog post, news story, product card, user review).
* `<aside>`: Content indirectly related to the main content (sidebars, callouts, author bios, ad units).
* `<footer>`: The concluding section containing copyright info, contact details, sitemaps, and legal links.

---

# Module 8: HTML Tables

Tables display structured, tabular, multi-dimensional dataset values (e.g., financial spreadsheets, schedules, event scorecards).

```html
<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Fight</th>
      <th>Venue</th>
      <th>City</th>
      <th>PPV Buys</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>UFC 189</td>
      <td>Mendes vs. McGregor</td>
      <td rowspan="3">MGM Grand</td>
      <td rowspan="4">Las Vegas</td>
      <td>825,000</td>
    </tr>
    <tr>
      <td>UFC 194</td>
      <td>Aldo vs. McGregor</td>
      <td>1,200,000</td>
    </tr>
    <tr>
      <td>UFC 196</td>
      <td>McGregor vs. Diaz</td>
      <td>1,317,000</td>
    </tr>
    <tr>
      <td>UFC 202</td>
      <td>Diaz vs. McGregor 2</td>
      <td>T-Mobile Arena</td>
      <td>1,650,000</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="4">Total PPV Sales</td>
      <td>4,992,000</td>
    </tr>
  </tfoot>
</table>
```

## 8.1 Table Elements:
* `<table>`: The wrapper for all tabular data.
* `<thead>`: Groups header content; ensures column titles remain visible during scrolling or printing.
* `<tbody>`: Encloses the primary body data rows.
* `<tfoot>`: Houses summary rows (e.g., totals, averages).
* `<tr>` (Table Row): Defines an individual horizontal row.
* `<th>` (Table Header): Defines a heading cell (bold and centered by default, accessible to screen readers).
* `<td>` (Table Data): Defines a standard data cell.

## 8.2 Cell Spanning (`colspan` & `rowspan`)
* **`colspan="n"` (Column Span):** Merges a cell across $n$ horizontal columns.
  * Example: `<td colspan="4">Total PPV Sales</td>` stretches across 4 columns.
* **`rowspan="n"` (Row Span):** Merges a cell downwards across $n$ vertical rows.
  * Example: `<td rowspan="3">MGM Grand</td>` merges across 3 rows, preventing repeated cell text.

---

# Module 9: Scientific, Academic & Media Notation

## 9.1 Superscript (`<sup>`) & Subscript (`<sub>`)

Used for formulas, math exponents, chemical equations, and footnote annotations:

```html
<!-- Mathematical Powers -->
<p>The Pythagorean equation: a<sup>2</sup> + b<sup>2</sup> = c<sup>2</sup></p>

<!-- Chemical Formulas -->
<p>Water formula: H<sub>2</sub>O</p>
<p>Glucose formula: C<sub>6</sub>H<sub>12</sub>O<sub>6</sub></p>

<!-- Footnote and Citation References -->
<p>According to recent publications<sup>[8]</sup>, global temperatures rose.</p>
```

* **`<sup>` (Superscript):** Raises text above the baseline (exponents $x^2$, ordinal indicators $1^{\text{st}}$, citations $^{[1]}$).
* **`<sub>` (Subscript):** Lowers text below the baseline (chemical notation $\text{CO}_2$, math indices $x_i$).

---

## 9.2 Figures & Captions (`<figure>` and `<figcaption>`)
Used to encapsulate self-contained media (charts, diagrams, code blocks, photos) along with an explicit caption:

```html
<figure>
  <img src="images/potassium.jpg" alt="Soft silvery-white chunk of potassium stored in mineral oil">
  <figcaption>Figure 1.1: Freshly cut pieces of potassium metal under controlled laboratory conditions.</figcaption>
</figure>
```
* **`<figure>`:** Semantically wraps the visual or illustrative asset.
* **`<figcaption>`:** Provides an accessible, direct text caption tied directly to the figure element.

---

# Quick-Reference Syntax Cheatsheet

```html
<!-- 1. BOILERPLATE -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
</head>
<body>

  <!-- 2. HEADINGS & TEXT -->
  <h1>Single Main Title</h1>
  <p>Standard paragraph with <strong>bold</strong>, <em>italic</em>, and <span class="custom">inline span</span>.</p>

  <!-- 3. LISTS -->
  <ol>
    <li>Numbered Item</li>
  </ol>
  <ul>
    <li>Bullet Item</li>
  </ul>

  <!-- 4. MEDIA & LINKS -->
  <a href="https://site.com" target="_blank" rel="noopener">External Link</a>
  <a href="#section-id">In-page Link</a>
  <img src="path/image.png" alt="Accessible description">

  <!-- 5. SEMANTIC WRAPPERS -->
  <header><nav></nav></header>
  <main>
    <section id="section-id">
      <article></article>
      <aside></aside>
    </section>
  </main>
  <footer></footer>

  <!-- 6. FORMS -->
  <form action="/target" method="POST">
    <label for="fname">First Name</label>
    <input type="text" id="fname" name="firstname" required>

    <label for="notes">Notes</label>
    <textarea id="notes" name="notes"></textarea>

    <button type="submit">Submit Form</button>
  </form>

  <!-- 7. TABLES -->
  <table>
    <thead><tr><th>Col 1</th><th>Col 2</th></tr></thead>
    <tbody><tr><td>Data 1</td><td>Data 2</td></tr></tbody>
    <tfoot><tr><td colspan="2">Summary</td></tr></tfoot>
  </table>

  <!-- 8. SCIENTIFIC & FIGURES -->
  <p>E = mc<sup>2</sup> | H<sub>2</sub>O</p>
  <figure>
    <img src="chart.svg" alt="Bar chart">
    <figcaption>Figure 1: Performance metrics</figcaption>
  </figure>

</body>
</html>
```