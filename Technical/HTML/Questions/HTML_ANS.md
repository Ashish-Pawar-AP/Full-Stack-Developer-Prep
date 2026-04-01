# HTML & HTML5 Interview Questions

---

## 1. Basic HTML Questions

---

### 1. What is HTML?

**Answer:**

HTML (HyperText Markup Language) is the standard language used to create and structure content on the web. It defines the layout of web pages using elements like headings, paragraphs, images, links, etc.

- It is **not a programming language**, but a **markup language**
- It uses **tags** to structure content

**Example:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

---

### 2. What is the difference between HTML and HTML5?

**Answer:**

| Feature    | HTML (Older)          | HTML5 (Latest)                |
| ---------- | --------------------- | ----------------------------- |
| Doctype    | Long declaration      | Simple (`<!DOCTYPE html>`)    |
| Multimedia | Requires plugins      | Native audio & video support  |
| Semantics  | Limited               | New semantic tags added       |
| Graphics   | No canvas/SVG support | Supports Canvas & SVG         |
| Storage    | Cookies only          | LocalStorage & SessionStorage |

**Example (HTML5 features):**

```html
<video controls>
  <source src="video.mp4" type="video/mp4" />
</video>

<canvas id="myCanvas"></canvas>
```

---

### 3. What are tags in HTML?

**Answer:**

Tags are predefined keywords used to define elements in HTML. They are enclosed in angle brackets `< >`.

- Most tags come in pairs: opening and closing
- Some are self-closing

**Examples:**

```html
<p>This is a paragraph</p>
<br />
<img src="image.jpg" />
```

---

### 4. What is an element?

**Answer:**

An HTML element consists of:

- Opening tag
- Content
- Closing tag

**Structure:**

```html
<tagname>Content</tagname>
```

**Example:**

```html
<h1>Hello</h1>
```

Here:

- `<h1>` = opening tag
- `Hello` = content
- `</h1>` = closing tag

---

### 5. What is the difference between tags and attributes?

**Answer:**

| Tags                 | Attributes                     |
| -------------------- | ------------------------------ |
| Define structure     | Provide additional information |
| Written inside `< >` | Written inside opening tag     |
| Example: `<p>`       | Example: `class="text"`        |

**Example:**

```html
<p class="text">Hello</p>
```

- `<p>` = tag
- `class="text"` = attribute

---

### 6. What are global attributes?

**Answer:**

Global attributes are attributes that can be used on **any HTML element**.

**Common Global Attributes:**

- `id`
- `class`
- `style`
- `title`
- `data-*`

**Example:**

```html
<p id="para1" class="text" style="color:red;" title="info">Hello World</p>
```

---

### 7. What is the basic structure of an HTML document?

**Answer:**

Every HTML document follows a standard structure.

**Structure:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    Content goes here
  </body>
</html>
```

**Explanation:**

- `<!DOCTYPE html>` → Defines HTML5
- `<html>` → Root element
- `<head>` → Metadata
- `<body>` → Visible content

---

### 8. What is `<!DOCTYPE html>`?

**Answer:**

`<!DOCTYPE html>` is a declaration that tells the browser the document type and version of HTML.

- It ensures the page is rendered in **standard mode**
- Required at the top of every HTML5 document

**Example:**

```html
<!DOCTYPE html>
```

---

### 9. What is the difference between `<head>` and `<body>`?

**Answer:**

| `<head>`                    | `<body>`                       |
| --------------------------- | ------------------------------ |
| Contains metadata           | Contains visible content       |
| Not displayed on page       | Displayed to users             |
| Includes title, meta, links | Includes text, images, buttons |

**Example:**

```html
<head>
  <title>My Website</title>
</head>

<body>
  <h1>Welcome</h1>
</body>
```

---

### 10. What is a meta tag?

**Answer:**

Meta tags provide information about the HTML document to the browser and search engines.

- Placed inside `<head>`
- Not visible on the webpage

**Common Uses:**

- Character encoding
- SEO
- Viewport settings

**Example:**

```html
<meta charset="UTF-8" />
<meta name="description" content="This is a website" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

---

## 2. HTML Document Structure

---

### 11. What are semantic and non-semantic tags?

**Answer:**

HTML tags are categorized into **semantic** and **non-semantic** based on whether they describe the meaning of the content.

#### ✅ Semantic Tags:

Semantic tags clearly describe the purpose of the content to both **developers and browsers**.

**Examples:**

- `<header>`
- `<footer>`
- `<article>`
- `<section>`
- `<nav>`
- `<main>`

These tags improve:

- SEO
- Accessibility
- Code readability

#### ❌ Non-Semantic Tags:

These tags do not describe the content meaning.

**Examples:**

- `<div>`
- `<span>`

They are mainly used for styling and layout.

**Example:**

```html id="sem1"
<header>
  <h1>Website Title</h1>
</header>

<div>
  <p>This is a non-semantic container</p>
</div>
```

---

### 12. What are block-level elements?

**Answer:**

Block-level elements take up the **full width available** and always start on a **new line**.

#### Key Features:

- Occupy full width
- Start on a new line
- Can contain block and inline elements

**Common Block Elements:**

- `<div>`
- `<p>`
- `<h1>` to `<h6>`
- `<section>`
- `<article>`

**Example:**

```html id="block1"
<div>This is a block element</div>
<p>This is another block element</p>
```

---

### 13. What are inline elements?

**Answer:**

Inline elements only take up as much width as needed and do **not start on a new line**.

#### Key Features:

- Stay in the same line
- Only take required width
- Cannot contain block elements

**Common Inline Elements:**

- `<span>`
- `<a>`
- `<strong>`
- `<img>`
- `<em>`

**Example:**

```html id="inline1"
<p>This is <span>inline</span> text.</p>
```

---

### 14. What is the difference between `<div>` and `<span>`?

**Answer:**

| Feature    | `<div>` (Block)   | `<span>` (Inline)   |
| ---------- | ----------------- | ------------------- |
| Type       | Block-level       | Inline              |
| Line Break | Starts new line   | No line break       |
| Usage      | Layout / sections | Styling small parts |
| Width      | Full width        | Content width       |

**Example:**

```html id="divspan1"
<div>This is a block container</div>

<p>This is <span style="color:red;">important</span> text.</p>
```

---

### 15. What is the difference between `<section>` and `<div>`?

**Answer:**

| Feature | `<section>`                     | `<div>`           |
| ------- | ------------------------------- | ----------------- |
| Type    | Semantic                        | Non-semantic      |
| Meaning | Represents a section of content | Generic container |
| SEO     | Better for SEO                  | No SEO value      |
| Usage   | Thematic grouping               | Styling/layout    |

#### When to use `<section>`:

- When content has a **clear heading or purpose**

#### When to use `<div>`:

- For styling or grouping without meaning

**Example:**

```html id="section1"
<section>
  <h2>About Us</h2>
  <p>We are a company...</p>
</section>

<div class="box">Styled container</div>
```

---

### 16. What is the `<article>` tag?

**Answer:**

The `<article>` tag represents **independent, self-contained content** that can be reused or distributed.

#### Examples:

- Blog posts
- News articles
- Comments
- Product cards

#### Key Feature:

- Makes sense even if removed from the page

**Example:**

```html id="article1"
<article>
  <h2>Blog Title</h2>
  <p>This is a blog post.</p>
</article>
```

---

### 17. What is the `<aside>` tag?

**Answer:**

The `<aside>` tag represents content that is **related but not part of the main content**.

#### Examples:

- Sidebar
- Ads
- Related links
- Author bio

**Example:**

```html id="aside1"
<aside>
  <h3>Related Links</h3>
  <ul>
    <li>Article 1</li>
    <li>Article 2</li>
  </ul>
</aside>
```

---

### 18. What is `<header>` and `<footer>`?

**Answer:**

#### `<header>`:

Represents introductory content.

**Contains:**

- Logo
- Navigation
- Title

#### `<footer>`:

Represents ending content.

**Contains:**

- Copyright
- Contact info
- Links

**Example:**

```html id="headerfooter1"
<header>
  <h1>My Website</h1>
</header>

<footer>
  <p>© 2026 My Website</p>
</footer>
```

---

### 19. What is the `<main>` tag?

**Answer:**

The `<main>` tag represents the **main content of the webpage**.

#### Rules:

- Should be **unique**
- Should not include repeated elements like header/footer/nav

**Purpose:**

- Helps screen readers
- Improves accessibility

**Example:**

```html id="main1"
<main>
  <h2>Welcome</h2>
  <p>This is the main content.</p>
</main>
```

---

### 20. Why is semantic HTML important?

**Answer:**

Semantic HTML is important because it improves:

#### 1. SEO (Search Engine Optimization)

Search engines understand content better.

#### 2. Accessibility

Screen readers can interpret the structure correctly.

#### 3. Readability

Code becomes easier to understand and maintain.

#### 4. Maintainability

Developers can easily navigate and update code.

#### 5. Better Structure

Clear separation of content sections.

**Example (Non-semantic vs Semantic):**

❌ Non-semantic:

```html id="nonsem"
<div class="header">Header</div>
<div class="content">Content</div>
<div class="footer">Footer</div>
```

✅ Semantic:

```html id="sem2"
<header>Header</header>
<main>Content</main>
<footer>Footer</footer>
```

---

## 3. Text & Formatting Tags

---

### 21. What is the difference between `<b>` and `<strong>`?

**Answer:**

Both `<b>` and `<strong>` make text appear bold, but they serve different purposes.

| Feature       | `<b>`                | `<strong>`                  |
| ------------- | -------------------- | --------------------------- |
| Type          | Non-semantic         | Semantic                    |
| Purpose       | Just makes text bold | Indicates importance        |
| SEO           | No impact            | Helps SEO                   |
| Accessibility | No special meaning   | Screen readers emphasize it |

#### Key Point:

- `<strong>` conveys meaning (importance)
- `<b>` is purely visual

**Example:**

```html
<p>This is <b>bold</b> text.</p>
<p>This is <strong>important</strong> text.</p>
```

---

### 22. What is the difference between `<i>` and `<em>`?

**Answer:**

Both `<i>` and `<em>` italicize text, but their meaning differs.

| Feature       | `<i>`         | `<em>`                   |
| ------------- | ------------- | ------------------------ |
| Type          | Non-semantic  | Semantic                 |
| Purpose       | Visual italic | Emphasis (importance)    |
| Accessibility | No effect     | Screen readers stress it |

#### Key Point:

- `<em>` adds emphasis (semantic)
- `<i>` is just styling

**Example:**

```html
<p>This is <i>italic</i> text.</p>
<p>This is <em>emphasized</em> text.</p>
```

---

### 23. What is the `<mark>` tag?

**Answer:**

The `<mark>` tag is used to **highlight text**.

#### Use Cases:

- Search results highlighting
- Important notes

**Default Behavior:**

- Background color becomes yellow

**Example:**

```html
<p>This is <mark>highlighted</mark> text.</p>
```

---

### 24. What is the `<small>` tag?

**Answer:**

The `<small>` tag is used to display **smaller text**.

#### Common Uses:

- Copyright text
- Legal disclaimers
- Notes

**Example:**

```html
<p>This is normal text.</p>
<p><small>This is small text.</small></p>
```

---

### 25. What are `<sup>` and `<sub>` tags?

**Answer:**

These tags are used for superscript and subscript text.

| Tag     | Meaning     | Position       |
| ------- | ----------- | -------------- |
| `<sup>` | Superscript | Above baseline |
| `<sub>` | Subscript   | Below baseline |

#### Use Cases:

- Mathematical formulas
- Chemical formulas

**Example:**

```html
<p>2<sup>3</sup> = 8</p>
<p>H<sub>2</sub>O</p>
```

---

### 26. What is the `<pre>` tag?

**Answer:**

The `<pre>` tag displays text in a **preformatted way**, preserving:

- Spaces
- Line breaks
- Formatting

#### Key Feature:

- Uses monospace font

**Example:**

```html
<pre>
Hello     World
This is preformatted text
</pre>
```

---

### 27. What is the `<code>` tag?

**Answer:**

The `<code>` tag is used to display **programming code**.

#### Features:

- Displays text in monospace font
- Used inside `<pre>` for better formatting

**Example:**

```html
<p>Inline code: <code>console.log("Hello")</code></p>

<pre>
<code>
function test() {
  return true;
}
</code>
</pre>
```

---

### 28. What is the `<blockquote>` tag?

**Answer:**

The `<blockquote>` tag is used for **long quotations** from another source.

#### Features:

- Indented by default
- Can include `cite` attribute for source

**Example:**

```html
<blockquote cite="https://example.com">
  This is a quoted text from another source.
</blockquote>
```

---

### 29. What is the `<abbr>` tag?

**Answer:**

The `<abbr>` tag is used to define **abbreviations or acronyms**.

#### Feature:

- Shows full form on hover using `title` attribute

**Example:**

```html
<p><abbr title="HyperText Markup Language">HTML</abbr> is a markup language.</p>
```

---

### 30. What is the `<cite>` tag?

**Answer:**

The `<cite>` tag is used to reference the **title of a work**.

#### Examples of Work:

- Books
- Movies
- Articles
- Research papers

**Default Style:**

- Italic text

**Example:**

```html
<p>I recently read <cite>Atomic Habits</cite>.</p>
```

---

## 4. Links & Media

---

### 31. How do you create a hyperlink in HTML?

**Answer:**

A hyperlink is created using the `<a>` (anchor) tag. It allows users to navigate from one page to another.

#### Syntax:

```html
<a href="URL">Link Text</a>
```

#### Key Attribute:

- `href` → Specifies the destination URL

**Example:**

```html id="link1"
<a href="https://www.google.com">Visit Google</a>
```

#### Linking to internal page:

```html id="link2"
<a href="about.html">Go to About Page</a>
```

---

### 32. What is the difference between absolute and relative URLs?

**Answer:**

| Feature    | Absolute URL                    | Relative URL                       |
| ---------- | ------------------------------- | ---------------------------------- |
| Definition | Full path including domain      | Path relative to current file      |
| Usage      | External links                  | Internal links                     |
| Example    | `https://example.com/page.html` | `page.html` or `/folder/page.html` |

#### Example:

```html id="url1"
<!-- Absolute URL -->
<a href="https://example.com">External Site</a>

<!-- Relative URL -->
<a href="contact.html">Contact Page</a>
```

---

### 33. What does `target="_blank"` do?

**Answer:**

The `target="_blank"` attribute opens the link in a **new browser tab or window**.

#### Example:

```html id="target1"
<a href="https://example.com" target="_blank">Open in new tab</a>
```

#### ⚠️ Best Practice (Security):

Use `rel="noopener noreferrer"` to prevent security risks.

```html id="target2"
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
  Secure Link
</a>
```

---

### 34. What is the `alt` attribute in the `<img>` tag?

**Answer:**

The `alt` attribute provides **alternative text** for an image.

#### Purpose:

- Displayed if image fails to load
- Improves accessibility (screen readers)
- Helps SEO

**Example:**

```html id="img1"
<img src="image.jpg" alt="A beautiful sunset" />
```

---

### 35. What are `<figure>` and `<figcaption>` tags?

**Answer:**

These are semantic tags used to group media content with a caption.

#### `<figure>`:

- Wraps media like images, charts, diagrams

#### `<figcaption>`:

- Provides a caption for the content

**Example:**

```html id="figure1"
<figure>
  <img src="image.jpg" alt="Nature" />
  <figcaption>This is a nature image</figcaption>
</figure>
```

---

### 36. What is the difference between `<audio>` and `<video>`?

**Answer:**

| Feature | `<audio>`        | `<video>`           |
| ------- | ---------------- | ------------------- |
| Purpose | Plays sound      | Plays video + audio |
| Visual  | No visual output | Displays video      |
| Formats | MP3, WAV, OGG    | MP4, WebM, OGG      |

**Example:**

```html id="media1"
<audio controls>
  <source src="audio.mp3" type="audio/mpeg" />
</audio>

<video controls width="300">
  <source src="video.mp4" type="video/mp4" />
</video>
```

---

### 37. What is the `controls` attribute?

**Answer:**

The `controls` attribute adds **default media controls** like:

- Play
- Pause
- Volume
- Seek bar

#### Used in:

- `<audio>`
- `<video>`

**Example:**

```html id="controls1"
<video controls>
  <source src="video.mp4" />
</video>
```

---

### 38. What is the `poster` attribute in `<video>`?

**Answer:**

The `poster` attribute specifies an **image to display before the video plays**.

#### Purpose:

- Acts like a thumbnail

**Example:**

```html id="poster1"
<video controls poster="thumbnail.jpg">
  <source src="video.mp4" />
</video>
```

---

### 39. What is the `<source>` tag?

**Answer:**

The `<source>` tag is used inside media elements (`<audio>`, `<video>`) to define multiple media files.

#### Purpose:

- Allows browser to choose supported format

**Example:**

```html id="source1"
<video controls>
  <source src="video.mp4" type="video/mp4" />
  <source src="video.webm" type="video/webm" />
</video>
```

---

### 40. What is an `<iframe>`?

**Answer:**

An `<iframe>` (Inline Frame) is used to **embed another webpage inside the current page**.

#### Use Cases:

- Embedding YouTube videos
- Google Maps
- External websites

**Example:**

```html id="iframe1"
<iframe src="https://www.example.com" width="600" height="400"> </iframe>
```

#### Example (YouTube embed):

```html id="iframe2"
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  allowfullscreen
>
</iframe>
```

---

Here is your **detailed, clean, copy-paste ready Markdown file** 👇

---

## 5. Lists

---

### 41. What are the types of lists in HTML?

**Answer:**

HTML provides **three types of lists** to organize content:

#### 1. Unordered List (`<ul>`)

- Displays items with **bullets**
- Order does not matter

#### 2. Ordered List (`<ol>`)

- Displays items with **numbers or letters**
- Order matters

#### 3. Description List (`<dl>`)

- Used for **terms and descriptions**

**Example:**

```html id="list1"
<!-- Unordered List -->
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>

<!-- Ordered List -->
<ol>
  <li>Step 1</li>
  <li>Step 2</li>
</ol>

<!-- Description List -->
<dl>
  <dt>HTML</dt>
  <dd>Markup language for web pages</dd>
</dl>
```

---

### 42. What is the difference between `<ul>` and `<ol>`?

**Answer:**

| Feature  | `<ul>` (Unordered List) | `<ol>` (Ordered List) |
| -------- | ----------------------- | --------------------- |
| Order    | Not important           | Important             |
| Marker   | Bullets                 | Numbers / Letters     |
| Use Case | Items without sequence  | Steps / rankings      |

**Example:**

```html id="ulol1"
<ul>
  <li>Milk</li>
  <li>Bread</li>
</ul>

<ol>
  <li>Login</li>
  <li>Dashboard</li>
</ol>
```

---

### 43. What is the `<li>` tag?

**Answer:**

The `<li>` (List Item) tag is used to define **individual items** inside lists.

#### Used Inside:

- `<ul>`
- `<ol>`

**Example:**

```html id="li1"
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

#### Nested List Example:

```html id="li2"
<ul>
  <li>
    Fruits
    <ul>
      <li>Apple</li>
      <li>Banana</li>
    </ul>
  </li>
</ul>
```

---

### 44. What is the `<dl>` tag?

**Answer:**

The `<dl>` (Description List) tag is used to create a list of **terms and their descriptions**.

#### Structure:

- `<dl>` → container
- `<dt>` → term
- `<dd>` → description

**Use Cases:**

- Glossary
- FAQs
- Definitions

**Example:**

```html id="dl1"
<dl>
  <dt>CSS</dt>
  <dd>Used for styling web pages</dd>

  <dt>JavaScript</dt>
  <dd>Used for interactivity</dd>
</dl>
```

---

### 45. What are `<dt>` and `<dd>` tags?

**Answer:**

These tags are used inside a `<dl>` (Description List).

#### `<dt>` (Description Term):

- Represents the **term or title**

#### `<dd>` (Description Definition):

- Represents the **description of the term**

**Example:**

```html id="dtdd1"
<dl>
  <dt>HTML</dt>
  <dd>Structure of web pages</dd>

  <dt>CSS</dt>
  <dd>Design and styling</dd>
</dl>
```

#### Multiple Descriptions Example:

```html id="dtdd2"
<dl>
  <dt>JavaScript</dt>
  <dd>Client-side scripting language</dd>
  <dd>Used for dynamic behavior</dd>
</dl>
```

---

## 6. Tables

---

### 46. How do you create a table in HTML?

**Answer:**

A table in HTML is created using the `<table>` tag along with rows (`<tr>`) and cells (`<td>` or `<th>`).

#### Basic Structure:

```html id="table1"
<table border="1">
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Ashish</td>
    <td>22</td>
  </tr>
</table>
```

#### Explanation:

- `<table>` → Table container
- `<tr>` → Table row
- `<th>` → Table header cell
- `<td>` → Table data cell

---

### 47. What are `<table>`, `<tr>`, `<td>`, and `<th>`?

**Answer:**

These are the core tags used to build tables:

| Tag       | Full Form    | Purpose               |
| --------- | ------------ | --------------------- |
| `<table>` | Table        | Defines the table     |
| `<tr>`    | Table Row    | Defines a row         |
| `<td>`    | Table Data   | Defines a normal cell |
| `<th>`    | Table Header | Defines a header cell |

#### Example:

```html id="table2"
<table border="1">
  <tr>
    <th>Subject</th>
    <th>Marks</th>
  </tr>
  <tr>
    <td>Math</td>
    <td>90</td>
  </tr>
</table>
```

---

### 48. What is the difference between `<td>` and `<th>`?

**Answer:**

| Feature       | `<td>` (Table Data) | `<th>` (Table Header)    |
| ------------- | ------------------- | ------------------------ |
| Purpose       | Normal cell         | Header cell              |
| Text Style    | Normal              | Bold (default)           |
| Alignment     | Left-aligned        | Center-aligned (default) |
| Semantic Role | Data                | Heading                  |

**Example:**

```html id="tdth1"
<tr>
  <th>Name</th>
  <th>Age</th>
</tr>
<tr>
  <td>Ashish</td>
  <td>22</td>
</tr>
```

---

### 49. What is colspan and rowspan?

**Answer:**

These attributes are used to **merge table cells**.

#### `colspan`:

- Merges cells **horizontally (columns)**

#### `rowspan`:

- Merges cells **vertically (rows)**

**Example:**

```html id="span1"
<table border="1">
  <tr>
    <th colspan="2">Student Info</th>
  </tr>
  <tr>
    <td>Name</td>
    <td>Age</td>
  </tr>
  <tr>
    <td rowspan="2">Ashish</td>
    <td>22</td>
  </tr>
  <tr>
    <td>23</td>
  </tr>
</table>
```

---

### 50. What are `<thead>`, `<tbody>`, and `<tfoot>`?

**Answer:**

These tags are used to **structure a table logically**.

| Tag       | Purpose                      |
| --------- | ---------------------------- |
| `<thead>` | Groups the header content    |
| `<tbody>` | Groups the main body content |
| `<tfoot>` | Groups the footer content    |

#### Benefits:

- Improves readability
- Helps styling with CSS
- Better accessibility

**Example:**

```html id="table3"
<table border="1">
  <thead>
    <tr>
      <th>Name</th>
      <th>Marks</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Ashish</td>
      <td>90</td>
    </tr>
    <tr>
      <td>Rahul</td>
      <td>85</td>
    </tr>
  </tbody>

  <tfoot>
    <tr>
      <td>Total</td>
      <td>175</td>
    </tr>
  </tfoot>
</table>
```

---

## 7. Forms

---

### 51. How do you create a form in HTML?

**Answer:**

A form is created using the `<form>` tag, which contains input elements like text fields, buttons, checkboxes, etc., to collect user data.

#### Basic Structure:

```html id="form1"
<form action="/submit" method="POST">
  <label>Name:</label>
  <input type="text" name="name" />

  <button type="submit">Submit</button>
</form>
```

#### Key Points:

- Used for user input
- Data is sent to a server for processing
- Contains form controls like `<input>`, `<textarea>`, `<select>`

---

### 52. What is the `<form>` tag?

**Answer:**

The `<form>` tag is used to **define a form** that collects user input and sends it to a server.

#### Important Attributes:

- `action` → URL where data is sent
- `method` → HTTP method (GET or POST)

**Example:**

```html id="form2"
<form action="/login" method="POST">
  <input type="text" name="username" />
  <input type="password" name="password" />
  <button type="submit">Login</button>
</form>
```

---

### 53. What are form attributes (action, method)?

**Answer:**

#### 1. `action`:

- Specifies where form data is sent

#### 2. `method`:

- Specifies how data is sent

| Attribute | Description              |
| --------- | ------------------------ |
| action    | URL to send data         |
| method    | HTTP method (GET / POST) |

**Example:**

```html id="form3"
<form action="/submit-data" method="POST">
  <input type="text" name="username" />
  <button type="submit">Submit</button>
</form>
```

---

### 54. What is the difference between GET and POST?

**Answer:**

| Feature       | GET            | POST                |
| ------------- | -------------- | ------------------- |
| Data Location | URL            | Request body        |
| Security      | Less secure    | More secure         |
| Data Limit    | Limited        | Large data allowed  |
| Use Case      | Fetch data     | Send sensitive data |
| Visibility    | Visible in URL | Not visible         |

#### Example:

```html id="getpost1"
<!-- GET -->
<form method="GET" action="/search">
  <input name="query" />
</form>

<!-- POST -->
<form method="POST" action="/login">
  <input name="password" />
</form>
```

---

### 55. What is the `<input>` tag?

**Answer:**

The `<input>` tag is used to create **input fields** in forms.

#### Key Attribute:

- `type` → Defines input type

**Example:**

```html id="input1"
<input type="text" placeholder="Enter name" />
<input type="password" placeholder="Enter password" />
```

---

### 56. What are different input types in HTML5?

**Answer:**

HTML5 introduced many input types for better validation and UX.

#### Common Input Types:

- `text`
- `password`
- `email`
- `number`
- `date`
- `checkbox`
- `radio`
- `file`
- `submit`
- `reset`
- `range`
- `color`

**Example:**

```html id="input2"
<input type="email" placeholder="Enter email" />
<input type="date" />
<input type="checkbox" /> Accept Terms <input type="range" min="0" max="100" />
```

---

### 57. What is the `<label>` tag?

**Answer:**

The `<label>` tag is used to define a **label for an input field**.

#### Benefits:

- Improves accessibility
- Clicking label focuses input

#### Using `for` attribute:

```html id="label1"
<label for="name">Name:</label> <input type="text" id="name" />
```

---

### 58. What is the `<textarea>` tag?

**Answer:**

The `<textarea>` tag is used to create a **multi-line text input field**.

#### Attributes:

- `rows`
- `cols`

**Example:**

```html id="textarea1"
<textarea rows="4" cols="30">
Enter your message
</textarea>
```

---

### 59. What is the `<select>` and `<option>` tag?

**Answer:**

Used to create a **dropdown list**.

#### `<select>`:

- Container for dropdown

#### `<option>`:

- Individual options

**Example:**

```html id="select1"
<select>
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
</select>
```

---

### 60. What is the `<fieldset>` and `<legend>` tag?

**Answer:**

These tags are used to **group related form elements**.

#### `<fieldset>`:

- Groups inputs

#### `<legend>`:

- Title of the group

**Example:**

```html id="fieldset1"
<fieldset>
  <legend>Personal Info</legend>

  <label>Name:</label>
  <input type="text" />

  <label>Age:</label>
  <input type="number" />
</fieldset>
```

---

## 8. HTML5 Features

---

### 61. What are new features introduced in HTML5?

**Answer:**

HTML5 introduced many powerful features to improve web development, performance, and user experience.

#### Key Features:

1. **Semantic Elements**
   - `<header>`, `<footer>`, `<article>`, `<section>`, `<main>`

2. **Multimedia Support**
   - `<audio>` and `<video>` without plugins

3. **Graphics**
   - `<canvas>` and SVG

4. **Form Enhancements**
   - New input types (`email`, `date`, `range`, etc.)
   - Built-in validation

5. **Web Storage**
   - `localStorage`, `sessionStorage`

6. **APIs**
   - Geolocation API
   - Drag and Drop API

**Example:**

```html id="html5features1"
<video controls>
  <source src="video.mp4" />
</video>

<input type="email" placeholder="Enter email" />
```

---

### 62. What are semantic elements in HTML5?

**Answer:**

Semantic elements clearly describe the meaning and structure of content.

#### Examples:

- `<header>` → Top section
- `<footer>` → Bottom section
- `<article>` → Independent content
- `<section>` → Section of page
- `<nav>` → Navigation links
- `<main>` → Main content

#### Benefits:

- Better SEO
- Improved accessibility
- Cleaner code structure

**Example:**

```html id="semantic1"
<header>
  <h1>My Website</h1>
</header>

<main>
  <section>
    <article>
      <h2>Blog Post</h2>
      <p>Content here...</p>
    </article>
  </section>
</main>

<footer>
  <p>© 2026</p>
</footer>
```

---

### 63. What is localStorage?

**Answer:**

`localStorage` is used to store data in the browser with **no expiration time**.

#### Key Features:

- Data persists even after browser is closed
- Stored as key-value pairs
- Capacity ~5MB

**Example:**

```html id="local1"
<script>
  localStorage.setItem("name", "Ashish");
  let value = localStorage.getItem("name");
  console.log(value);
</script>
```

---

### 64. What is sessionStorage?

**Answer:**

`sessionStorage` stores data for **one browser session only**.

#### Key Features:

- Data is deleted when tab/browser is closed
- Similar API as localStorage

**Example:**

```html id="session1"
<script>
  sessionStorage.setItem("user", "Ashish");
  let user = sessionStorage.getItem("user");
  console.log(user);
</script>
```

---

### 65. What is the difference between localStorage and sessionStorage?

**Answer:**

| Feature       | localStorage       | sessionStorage          |
| ------------- | ------------------ | ----------------------- |
| Expiry        | No expiration      | Expires when tab closes |
| Scope         | Shared across tabs | Per tab                 |
| Storage Limit | ~5MB               | ~5MB                    |
| Use Case      | Persistent data    | Temporary session data  |

---

### 66. What is the canvas element?

**Answer:**

The `<canvas>` element is used to draw **graphics dynamically using JavaScript**.

#### Use Cases:

- Games
- Charts
- Animations

**Example:**

```html id="canvas1"
<canvas id="myCanvas" width="200" height="100"></canvas>

<script>
  const canvas = document.getElementById("myCanvas");
  const ctx = canvas.getContext("2d");

  ctx.fillStyle = "blue";
  ctx.fillRect(10, 10, 150, 75);
</script>
```

---

### 67. What is SVG?

**Answer:**

SVG (Scalable Vector Graphics) is used to create **vector-based graphics** in XML format.

#### Key Features:

- Scalable without losing quality
- Lightweight
- Can be styled with CSS

**Example:**

```html id="svg1"
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="black" fill="red" />
</svg>
```

---

### 68. What is drag and drop API?

**Answer:**

The Drag and Drop API allows users to **drag elements and drop them** into a target area.

#### Common Events:

- `dragstart`
- `dragover`
- `drop`

**Example:**

```html id="drag1"
<div draggable="true" ondragstart="drag(event)">Drag me</div>

<div ondrop="drop(event)" ondragover="allowDrop(event)">Drop here</div>

<script>
  function allowDrop(ev) {
    ev.preventDefault();
  }

  function drag(ev) {
    ev.dataTransfer.setData("text", ev.target.innerText);
  }

  function drop(ev) {
    ev.preventDefault();
    let data = ev.dataTransfer.getData("text");
    ev.target.innerHTML = data;
  }
</script>
```

---

### 69. What is Geolocation API?

**Answer:**

The Geolocation API is used to get the **user's current location** (latitude & longitude).

#### Requires:

- User permission

**Example:**

```html id="geo1"
<script>
  navigator.geolocation.getCurrentPosition(function (position) {
    console.log(position.coords.latitude);
    console.log(position.coords.longitude);
  });
</script>
```

---

### 70. What is Web Storage API?

**Answer:**

The Web Storage API allows storing data in the browser using:

- `localStorage`
- `sessionStorage`

#### Features:

- Key-value storage
- Faster than cookies
- No server interaction required

**Example:**

```html id="storage1"
<script>
  localStorage.setItem("theme", "dark");
  let theme = localStorage.getItem("theme");
</script>
```

---

## 9. SEO & Performance

---

### 71. What is SEO?

**Answer:**

SEO (Search Engine Optimization) is the process of improving a website’s visibility on search engines like Google.

#### Goals of SEO:

- Rank higher in search results
- Increase organic (free) traffic
- Improve user experience

#### Types of SEO:

- **On-page SEO** → Content, HTML structure, tags
- **Off-page SEO** → Backlinks, social signals
- **Technical SEO** → Performance, mobile-friendliness

---

### 72. How does HTML help in SEO?

**Answer:**

HTML plays a major role in SEO by providing structure and meaning to web content.

#### Key Ways HTML Helps SEO:

1. **Semantic Tags**
   - `<header>`, `<article>`, `<section>` improve content understanding

2. **Heading Tags (`<h1>`–`<h6>`)**
   - Define content hierarchy

3. **Meta Tags**
   - Provide information to search engines

4. **Alt Attributes**
   - Help search engines understand images

5. **Proper Structure**
   - Clean and well-structured HTML improves crawlability

**Example:**

```html id="seo1"
<h1>Main Title</h1>
<h2>Subheading</h2>

<img src="image.jpg" alt="SEO optimized image" />
```

---

### 73. What are meta description and keywords?

**Answer:**

Meta tags provide information about a webpage.

#### Meta Description:

- A short summary of the page
- Displayed in search results

```html id="meta1"
<meta name="description" content="Learn HTML basics and advanced concepts" />
```

#### Meta Keywords:

- Previously used for keywords
- Now mostly ignored by modern search engines

```html id="meta2"
<meta name="keywords" content="HTML, CSS, JavaScript" />
```

---

### 74. What is the viewport meta tag?

**Answer:**

The viewport meta tag controls how a webpage is displayed on different screen sizes (responsive design).

#### Importance:

- Makes websites mobile-friendly
- Essential for responsive layouts

**Example:**

```html id="viewport1"
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

---

### 75. What is lazy loading?

**Answer:**

Lazy loading is a technique where images or resources are loaded **only when they are needed (on scroll)**.

#### Benefits:

- Faster page load time
- Reduced bandwidth usage
- Improved performance

**Example:**

```html id="lazy1"
<img src="image.jpg" loading="lazy" alt="Lazy loaded image" />
```

---

### 76. What is the importance of alt attribute?

**Answer:**

The `alt` attribute provides alternative text for images.

#### Importance:

1. **Accessibility**
   - Screen readers use it for visually impaired users

2. **SEO**
   - Helps search engines understand images

3. **Fallback**
   - Displays text if image fails to load

**Example:**

```html id="alt1"
<img src="logo.png" alt="Company Logo" />
```

---

### 77. What are Open Graph meta tags?

**Answer:**

Open Graph (OG) meta tags control how content appears when shared on social media platforms.

#### Used By:

- Facebook
- LinkedIn
- WhatsApp

#### Common OG Tags:

- `og:title`
- `og:description`
- `og:image`
- `og:url`

**Example:**

```html id="og1"
<meta property="og:title" content="My Website" />
<meta property="og:description" content="Best website for learning" />
<meta property="og:image" content="image.jpg" />
<meta property="og:url" content="https://example.com" />
```

---

### 78. What is favicon?

**Answer:**

A favicon is a small icon displayed in the browser tab next to the website title.

#### Importance:

- Improves branding
- Helps users identify your site

**Example:**

```html id="favicon1"
<link rel="icon" href="favicon.ico" type="image/x-icon" />
```

---

## 10. Advanced HTML Questions

### 79. What is the difference between `id` and `class`?

**Answer:**

Both `id` and `class` are attributes used to identify HTML elements, but they serve different purposes.

| Feature      | `id`               | `class`                    |
| ------------ | ------------------ | -------------------------- |
| Uniqueness   | Must be unique     | Can be reused              |
| Usage        | Single element     | Multiple elements          |
| CSS Selector | `#id`              | `.class`                   |
| JavaScript   | `getElementById()` | `getElementsByClassName()` |

**Example:**

```html id="idclass1"
<div id="header">Header</div>
<p class="text">Paragraph 1</p>
<p class="text">Paragraph 2</p>
```

---

### 80. Can multiple elements have the same `id`?

**Answer:**

❌ No, multiple elements should **not** have the same `id`.

#### Why?

- Violates HTML standards
- Causes issues in JavaScript and CSS
- Leads to unpredictable behavior

#### Correct Approach:

Use `class` for multiple elements.

**Example:**

```html id="idclass2"
<!-- Wrong -->
<div id="box"></div>
<div id="box"></div>

<!-- Correct -->
<div class="box"></div>
<div class="box"></div>
```

---

### 81. What is `data-*` attribute?

**Answer:**

The `data-*` attribute is used to store **custom data** in HTML elements.

#### Features:

- Starts with `data-`
- Accessible via JavaScript

**Example:**

```html id="data1"
<div data-user-id="123" id="user"></div>

<script>
  const user = document.getElementById("user");
  console.log(user.dataset.userId);
</script>
```

---

### 82. What is `contenteditable` attribute?

**Answer:**

The `contenteditable` attribute makes an element **editable by the user directly in the browser**.

#### Values:

- `true`
- `false`

**Example:**

```html id="editable1"
<p contenteditable="true">You can edit this text</p>
```

---

### 83. What is `tabindex`?

**Answer:**

The `tabindex` attribute controls the **tab order** of elements when navigating using the keyboard.

#### Values:

- `0` → Default tab order
- `-1` → Not focusable via tab
- `1+` → Custom order (not recommended)

**Example:**

```html id="tab1"
<input type="text" tabindex="1" /> <input type="text" tabindex="2" />
```

---

### 84. What is ARIA?

**Answer:**

ARIA (Accessible Rich Internet Applications) is a set of attributes that improve **accessibility** for users with disabilities.

#### Purpose:

- Helps screen readers understand UI components

#### Common ARIA Attributes:

- `aria-label`
- `aria-hidden`
- `aria-role`

**Example:**

```html id="aria1"
<button aria-label="Close menu">X</button>
```

---

### 85. What is accessibility in HTML?

**Answer:**

Accessibility means making websites usable for **all users**, including people with disabilities.

#### Key Practices:

- Use semantic HTML
- Add `alt` text to images
- Use proper labels
- Ensure keyboard navigation
- Use ARIA when needed

**Example:**

```html id="access1"
<label for="email">Email:</label> <input id="email" type="email" />
```

---

### 86. What is the difference between `defer` and `async`?

**Answer:**

Both are used in `<script>` to load JavaScript efficiently.

| Feature   | `async`                | `defer`            |
| --------- | ---------------------- | ------------------ |
| Execution | Immediately after load | After HTML parsing |
| Order     | Not guaranteed         | Maintains order    |
| Use Case  | Independent scripts    | Dependent scripts  |

**Example:**

```html id="script1"
<script src="app.js" async></script>
<script src="main.js" defer></script>
```

---

### 87. What is progressive enhancement?

**Answer:**

Progressive enhancement is a strategy where the basic functionality works for all users, and advanced features are added for modern browsers.

#### Approach:

1. Start with basic HTML
2. Add CSS
3. Add JavaScript enhancements

#### Benefit:

- Works on all devices and browsers

---

### 88. What is graceful degradation?

**Answer:**

Graceful degradation means building a fully featured application first and then ensuring it still works on older browsers.

#### Difference from Progressive Enhancement:

- Progressive → build basic → enhance
- Graceful → build advanced → fallback

---

### 89. How do browsers render HTML?

**Answer:**

Browser rendering process:

1. **Parse HTML** → Create DOM (Document Object Model)
2. **Parse CSS** → Create CSSOM
3. **Render Tree** → Combine DOM + CSSOM
4. **Layout** → Calculate positions
5. **Painting** → Draw pixels on screen

#### Flow:

```
HTML → DOM → CSS → CSSOM → Render Tree → Layout → Paint
```

---

### 90. What is DOM?

**Answer:**

DOM (Document Object Model) is a **tree-like structure** representing HTML elements.

#### Key Points:

- Allows JavaScript to interact with HTML
- Each element is a node

**Example:**

```html id="dom1"
<p id="text">Hello</p>

<script>
  document.getElementById("text").innerText = "Hi";
</script>
```

---

## 11. Scenario-Based Questions

### 91. How would you improve website accessibility?

**Answer:**

To improve accessibility, ensure your website is usable by all users, including those with disabilities.

#### Best Practices:

1. **Use Semantic HTML**
   - `<header>`, `<nav>`, `<main>`, `<footer>`

2. **Add Alt Text to Images**

```html
<img src="image.jpg" alt="Description of image" />
```

3. **Use Labels for Inputs**

```html
<label for="email">Email:</label> <input id="email" type="email" />
```

4. **Keyboard Navigation**

- Ensure all elements are accessible via keyboard (`tabindex`)

5. **ARIA Attributes**

```html
<button aria-label="Close">X</button>
```

6. **Proper Heading Structure**

- Use `<h1>` → `<h6>` in order

---

### 92. How would you optimize HTML for performance?

**Answer:**

#### Techniques:

1. **Minimize HTML Size**

- Remove unnecessary tags/comments

2. **Use Lazy Loading**

```html
<img src="image.jpg" loading="lazy" alt="image" />
```

3. **Optimize Images**

- Use compressed formats (WebP, JPEG)

4. **Reduce DOM Size**

- Avoid deeply nested elements

5. **Use Async/Defer for Scripts**

```html
<script src="app.js" defer></script>
```

6. **Avoid Inline Styles**

- Use external CSS

---

### 93. How would you structure a blog page using semantic tags?

**Answer:**

Use semantic elements to organize content properly.

**Example:**

```html
<header>
  <h1>My Blog</h1>
</header>

<main>
  <article>
    <h2>Blog Title</h2>
    <p>Blog content...</p>
  </article>

  <aside>
    <h3>Related Posts</h3>
  </aside>
</main>

<footer>
  <p>© 2026 Blog</p>
</footer>
```

---

### 94. How do you create a responsive HTML layout?

**Answer:**

#### Steps:

1. **Viewport Meta Tag**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

2. **Use Flexible Layouts**

- Use percentages instead of fixed widths

3. **Use CSS Media Queries**

```css
@media (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
```

4. **Responsive Images**

```html
<img src="image.jpg" style="max-width:100%;" />
```

---

### 95. How do you validate HTML code?

**Answer:**

HTML validation ensures your code follows proper standards.

#### Methods:

1. **Online Validator**

- Use W3C Validator

2. **Browser DevTools**

- Check console for errors

3. **Code Editors**

- VS Code extensions for linting

---

### 96. How do you embed a YouTube video?

**Answer:**

Use `<iframe>` to embed videos.

**Example:**

```html
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  allowfullscreen
>
</iframe>
```

---

### 97. How do you open a link in a new tab safely?

**Answer:**

Use `target="_blank"` with security attributes.

**Example:**

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
  Open Link
</a>
```

#### Why?

- Prevents security issues like tabnabbing

---

### 98. How do you create a downloadable link?

**Answer:**

Use the `download` attribute.

**Example:**

```html
<a href="file.pdf" download>Download PDF</a>
```

#### Optional:

```html
<a href="file.pdf" download="myfile.pdf">Download File</a>
```

---

### 99. How do you prevent form submission default behavior?

**Answer:**

Use JavaScript to prevent default form behavior.

**Example:**

```html
<form id="myForm">
  <button type="submit">Submit</button>
</form>

<script>
  document.getElementById("myForm").addEventListener("submit", function (e) {
    e.preventDefault();
    console.log("Form submission prevented");
  });
</script>
```

---

### 100. How would you design a login form using HTML?

**Answer:**

A login form includes input fields for username and password.

**Example:**

```html
<form action="/login" method="POST">
  <fieldset>
    <legend>Login</legend>

    <label for="username">Username:</label>
    <input id="username" type="text" name="username" required />

    <label for="password">Password:</label>
    <input id="password" type="password" name="password" required />

    <button type="submit">Login</button>
  </fieldset>
</form>
```

#### Best Practices:

- Use `required` for validation
- Use proper labels
- Use semantic structure

---
