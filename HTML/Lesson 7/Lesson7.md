## <span style="color:orange">Semantic Tags</span>

- Semantic HTML tags _provide meaning to the web content beyond just how they appear on the page._
- They help browsers, search engines, and assistive technologies understand the structure and significance of web content. Here’s a detailed explanation of the semantic tags you mentioned, along with examples:

### <span style="color:violet">header Tag `<header>`</span>

The `<header>` tag represents a container for introductory content or a set of navigational links. A `<header>` element typically contains one or more heading elements `(<h1> - <h6>)`, logo, and navigation elements. It can be used in different sections of a document, not just at the top.

```html
<header>
  <h1>My Website</h1>
  <nav>
    <!-- Navigation links -->
  </nav>
</header>
```

### <span style="color:violet">footer Tag `<footer>`</span>

The `<footer>` tag defines a footer for a document or a section. It often contains information about the author, copyright information, contact links, and sitemap.

```html
<footer>
  <p>Copyright © 2024. All rights reserved.</p>
</footer>
```

### <span style="color:violet">nav Tag `<nav>`</span>

The `<nav>` element represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.

```html
<nav>
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#news">News</a></li>
  </ul>
</nav>
```

### <span style="color:violet">main Tag `<main>`</span>

The `<main>` element represents the main content of the body of a document or application. The content should be unique to the document and not repeated across documents (e.g., site-wide navigation links).

```html
<main>
  <article>
    <!-- Main content -->
  </article>
</main>
```

### <span style="color:violet">article Tag `<article>`</span>

The `<article>` element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication).

```html
<article>
  <h2>Article Title</h2>
  <p>Article content...</p>
</article>
```

### <span style="color:violet">section Tag `<section>`</span>

The `<section>` tag represents a standalone section of content within a document, typically with a heading. It should be used for thematic grouping of content.

```html
<section>
  <h2>Section Heading</h2>
  <p>Section content...</p>
</section>
```

### <span style="color:violet">aside Tag `<aside>`</span>aside

The `<aside>` element represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes.

```html
<aside>
  <p>This is an aside.</p>
</aside>
```

### <span style="color:violet">details Tag `<details>`</span>

The `<details>` tag specifies additional details that the user can view or hide on demand. It’s often used to create an interactive widget that the user can open and close.

```html
<details>
  <summary>More Details</summary>
  <p>Hidden details go here.</p>
</details>
```

### <span style="color:violet">summary Tag `<summary>`</span>

The `<summary>` element specifies a summary, caption, or legend for a `<details>` element's content. It’s used as a heading for the content that can be shown or hidden.

```html
<details>
  <summary>Summary Title</summary>
  <p>Details content...</p>
</details>
```

### <span style="color:violet">mark Tag `<mark>`</span>

The `<mark>` tag defines text that should be marked or highlighted for reference or notation purposes, due to its relevance in another context.

```html
<p>Do not forget to buy <mark>milk</mark> today.</p>
```

### <span style="color:violet">time Tag `<time>`</span>

The `<time>` element represents a specific period in time or a date on the calendar. It can also include a time zone. This tag helps search engines and other services understand dates and times in a standardized format.

```html
<p>The concert is on <time datetime="2024-09-14">September 14</time>.</p>
```

#### Attribute `datetime`

- Attribute Name: datetime
- Purpose: Specifies the date and/or time in a machine-readable format. This can include dates, times, or both.
- Value Format:
  - For dates: **YYYY-MM-DD** (e.g., 2024-01-01 for January 1, 2024).
  - For times: **HH:MM (optionally HH:MM:SS or HH:MM:SS.sss)**, with a 24-hour clock (e.g., 14:30 for 2:30 PM).
  - For combined date and time: **YYYY-MM-DDTHH:MM (optionally YYYY-MM-DDTHH:MM:SS or YYYY-MM-DDTHH:MM:SSZ for UTC times)** (e.g., 2024-01-01T14:30 for January 1, 2024, at 2:30 PM).
  - For time zones: The ISO 8601 format is used, with a Z indicating UTC time or a +/-HH:MM offset for other time zones (e.g., 2024-01-01T14:30-05:00 for Eastern Standard Time).
  - For duration:
    1. Representing Hours, Minutes, and Seconds:
       - **PT2H30M:** Represents a duration of 2 hours and 30 minutes.
    2. Representing Days, Hours, and Minutes:
       - **P1DT1H:** Represents a duration of 1 day and 1 hour.
    3. Representing Weeks:
       - **P2W:** Represents a duration of 2 weeks.
    4. Representing Years and Months:
       - **P1Y2M:** Represents a duration of 1 year and 2 months.

### <span style="color:violet">div Tag `<div>`</span>

The `<div>` tag is a generic container for flow content, which does not inherently represent anything. It can be used to group elements for styling purposes (using the class or id attributes), or because they share attribute values, such as lang.

```html
<div class="container">
  <!-- Content -->
</div>
```

### <span style="color:violet">span Tag `<span>`</span>

The `<span>` element is a generic inline container for phrasing content, which does not inherently represent anything. It can be used to style parts of text, or for marking up a part of a text, or a part of a document with a class or id attribute.

```html
<p>This is an example of <span class="highlight">highlighted text</span>.</p>
```
