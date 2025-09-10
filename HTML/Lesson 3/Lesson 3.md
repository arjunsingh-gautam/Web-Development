# <span style="color:orange">HTML Tags and Elements</span>

## <span style="color:pink">Block vs Inline elements</span>

### <span style="color:violet">Block-level Elements</span>

Block-level elements occupy the entire space of their parent container (width-wise), creating a "block". They start on a new line and stretch out as far as they can, effectively breaking the flow of content. Block-level elements can contain other block-level elements, inline elements, and text.

#### Characteristics:

- Start on a new line.
- Take up the full width available (stretches out to the left and right as far as it can).
- Respect all CSS box model properties, including width, height, margin, and padding.
- Can contain inline elements and other block-level elements.

#### Examples:

- **div:** The most common block-level element, used for grouping other elements.
- **p:** Represents a paragraph.
- **h1, h2, ..., h6:** Heading elements.
- **ul, ol:** Unordered and ordered list containers.
- **li:** List item, which is considered block-level in the context of lists.

### <span style="color:violet">Inline Elements</span>

Inline elements do not start on a new line; they appear on the same line as the preceding content, assuming there's enough space. They only take up as much width as necessary. Inline elements are typically used to style a part of a text block without disrupting the flow of content.

#### Characteristics:

- Do not start on a new line; they appear in line with the surrounding content.
- Take up only as much width as necessary (not the full width of the container).
- Do not respect the top and bottom margin and padding settings (they do respect left and right margins and paddings).
- Cannot contain block-level elements.

#### Examples:

- **span:** Used for styling or targeting inline portions of text or elements without introducing a line break.
- **a:** Represents a hyperlink, allowing in-line links within text.
  strong: Makes text bold, indicating that it's of strong importance.
- **em:** Emphasizes text, usually styled as italic.
- **img:** Embeds an image in the document inline with the text.

#### Comparison in Practice

Consider this HTML snippet:

```html
<div>
  <p>This is a block-level element, a paragraph.</p>
  <span>This is an inline <em>element</em> within a block-level element.</span>
</div>
```

### <span style="color:violet">Whitespace Collapsing</span>

Whitespace collapsing is a fundamental behavior in HTML and CSS that involves the browser automatically reducing sequences of whitespace characters (spaces, tabs, and newlines) to a single space when rendering HTML documents. This behavior is crucial for making HTML more forgiving to write and read, but it can sometimes interfere with the intended layout or presentation of content.

---

### <span style="color:violet"> heading element:</span>

- In HTML, heading elements are used to define headings or titles for sections of content on a webpage. Headings range from `<h1>` (the highest level) to `<h6>` (the lowest level), indicating different levels of importance and hierarchy.
  > The `<h1>` element represents the **main heading** or title of the entire page, while the `<h6>` element represents a **lower-level heading**.

---

### <span style="color:violet"> paragraph element:</span>

- In HTML, the paragraph element is represented by the `<p>` tag.
- It is used to define paragraphs of text on a webpage.
- The `<p>` element is a **block-level element**, meaning it starts on a new line and takes up the full width available.

#### Common Attributes for Many HTML Elements:

- `id` Attribute:

  - Specifies a unique identifier for an HTML element. This is often used for linking to a specific section of a page.

```html
<h1 id="main-heading">Main Heading</h1>
<p id="intro-paragraph">This is the introduction.</p>
```

- `class` Attribute:

  - Specifies one or more class names for an HTML element. Classes are commonly used for styling multiple elements with CSS.

```html
<h2 class="subheading">Subheading</h2>
<p class="content">This is some content.</p>
```

#### Specific Attributes for Anchors within Headings:

- For headings, if you want to create a hyperlink to a specific heading, you can use the **id attribute** along with the `<a>` (anchor) element:

```html
<h3 id="section-heading">Section Heading</h3>
<a href="#section-heading">Jump to Section Heading</a>
```

---

### <span style="color:violet">Abbreviation Tag: `<abbr>` </span>

The `<abbr>` tag is used to denote an abbreviation or acronym. The title attribute is important because it provides the full description or meaning of the abbreviation/acronym. This is particularly useful for accessibility, as screen readers will utilize the title attribute to help users understand the abbreviation.

Example:

```html
<p>
  The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.
</p>
```

In this example, hovering over "WHO" in a browser will display the full form "World Health Organization" as a tooltip.

### <span style="color:violet">Address Tag: `<address>` </span>

- The `<address>` tag is used to contain contact information for the author/owner of a document or article. This tag semantically indicates that the enclosed text is contact information.
- **Block level element**

Example:

```html
<address>
  Contact us at <a href="mailto:example@example.com">example@example.com</a>.
</address>
```

In this example, the `<address>` tag encloses an email link, clearly indicating that this is contact information.

### <span style="color:violet">Line Break Tag: `<br>` </span>

The `<br>` tag is used to insert a line break in the text. It's a self-closing tag, meaning it doesn't need an end tag. The `<br>` tag is particularly useful for formatting text like addresses or poems where the line breaks are significant.

Example:

```html
<p>This is a line.<br />This is another line.</p>
```

This example shows how to use `<br>` to break lines within a paragraph.

### <span style="color:violet">Emphasis Tag: `<em>` </span>

The `<em>` tag is used to emphasize text, which is typically displayed as italic by browsers. The semantic importance of the `<em>` tag is that it denotes stressed emphasis on the enclosed text, which can affect the way screen readers interpret it.

Example:

```html
<p>The <em>quick</em> brown fox jumps over the lazy dog.</p>
```

Here, "quick" is emphasized (italicized), indicating a stress on that word.

### <span style="color:violet">Strong Tag: `<strong>` </span>

- The `<strong>` tag in HTML is used to indicate that its contents should be <u>strongly emphasized</u> or given importance compared to the surrounding text. When rendered by a web browser, text enclosed within a `<strong>` tag is typically displayed in <u>**bold** </u> by default.

```html
<p>
  This is a normal sentence, but
  <strong>this part is especially important</strong>.
</p>
```

### <span style="color:violet">Horizontal Rule Tag: `<hr>` </span>

The `<hr>` tag is used to insert a thematic break between paragraphs of text, often displayed as a horizontal line by browsers. It can be used to denote a change in topic or a significant shift in content.

Example:

```html
<p>Here is a paragraph.</p>
<hr />
<p>Here is another paragraph after a thematic break.</p>
```

### <span style="color:violet">Comments: `<!-- -->` </span>

- In HTML, comments are used to insert notes, explanations, or to temporarily disable code that should not be executed or rendered by the browser. **Comments are not displayed in the browser when the HTML document is rendered**.

```html
<!-- This is a comment -->
```

---

## <span style="color: yellow;"> HTML Entities </span>

- These are HTML entities, which are used to represent special characters that may otherwise be interpreted incorrectly by the HTML parser.
- Each entity begins with an ampersand (&) and ends with a semicolon (;). Entities are especially useful for characters that have a specific meaning in HTML (like `<`, `>`, `&`) or for inserting characters that are not readily available on a standard keyboard.

### <span style="color: pink;">Here's a breakdown of each of these entities:</span>

1. **&lt; - Less Than Symbol (`<`)**

   - **Entity**: `&lt;`
   - **Purpose**: Represents the less-than sign (`<`).
   - **Use Case**: Since `<` is used in HTML to denote the start of a tag (like `<div>` or `<p>`), writing it directly in content could confuse the HTML parser. So, `&lt;` is used to display a literal `<` in text.
   - **Example**:
     ```html
     <p>Use &lt; and &gt; for comparison in HTML.</p>
     ```
     **Output**:
     ```css
     Use < and > for comparison in HTML.
     ```

2. **&copy; - Copyright Symbol (`©`)**

   - **Entity**: `&copy;`
   - **Purpose**: Represents the copyright symbol (`©`).
   - **Use Case**: This is often used in footer sections or anywhere you want to denote copyrighted material in an HTML document.
   - **Example**:
     ```html
     <p>&copy; 2024 MyWebsite. All rights reserved.</p>
     ```
     **Output**:
     ```css
     © 2024 MyWebsite. All rights reserved.
     ```

3. **&nbsp; - Non-Breaking Space**
   - **Entity**: `&nbsp;`
   - **Purpose**: Inserts a non-breaking space in the text.
   - **Use Case**: It’s useful when you want to add extra spaces without the browser collapsing them. HTML collapses consecutive spaces by default, but `&nbsp;` prevents this. It’s also used to keep words together on the same line.
   - **Example**:
     ```html
     <p>Line&nbsp;with&nbsp;non-breaking&nbsp;spaces.</p>
     ```
     **Output**:
     ```csharp
     Line with non-breaking spaces.
     ```

### <span style="color: pink;">Why HTML Entities Are Used</span>

HTML entities are essential when you need to display characters that are part of the HTML language (like `<` or `&`), or when you need special symbols (like © or ®). They help prevent the HTML parser from misinterpreting content as tags or attributes, ensuring the text renders correctly in the browser.

### <span style="color: pink;">Common HTML Entities</span>

Some additional frequently used HTML entities include:

- `&gt;` for `>` (greater-than symbol)
- `&amp;` for `&` (ampersand symbol)
- `&quot;` for `"` (quotation mark)
- `&apos;` for `'` (apostrophe)

HTML entities improve readability and ensure proper rendering across all browsers and devices.

---

## <span style="color:#33ff00">HTML Text Formatting Tags and Elements</span>

HTML provides several tags and elements for formatting text. These tags allow you to emphasize, style, or structure text in various ways.

### <span style="color: pink;"> 1. `<b>` - Bold Text</span>

- **Purpose:** Makes the text bold without adding extra importance.
- **Attributes:** None.
- **Example:**
  ```html
  <b>This text is bold</b>
  ```
- **Use Case:** Highlighting specific text for visual purposes.

### <span style="color: pink;"> 2. `<strong>` - Strong Emphasis</span>

- **Purpose:** Indicates strong importance, typically displayed as **bold** and add semantic meaning
- **Attributes:** None.
- **Example:**

```html
<strong>Important text</strong>
```

- **Use Case:** Use for important or emphasized content.

### <span style="color: pink;"> 3. `<i>` - Italic Text</span>

- **Purpose:** Makes text italic without adding extra importance..
- **Attributes:** None.
- **Example:**

```html
<i>This text is italic</i>
```

- **Use Case:** For stylistic changes, like book titles or foreign words.

### <span style="color: pink;"> 4. `<em>` - Emphasized Text</span>

- **Purpose:** Adds emphasis to text, usually displayed in _italics_ add semantic meaning.
- **Attributes:** None.
- **Example:**

```html
<em>Emphasized text</em>
```

- **Use Case:** Highlighting text with semantic emphasis.

### <span style="color: pink;"> 5. `<mark>` - Highlighted Text</span>

- **Purpose:** Highlights text with a yellow background by default.
- **Attributes:** None.
- **Example:**

```html
<mark>Highlighted text</mark>
```

- **Use Case:** To draw attention to specific words or phrases.

### <span style="color: pink;"> 6. `<small>` - Smaller Text</span>

- **Purpose:** Reduces the font size of the enclosed text.
- **Attributes:** None
- **Semantic Meaning:** The `<small>` tag is used to indicate fine print, disclaimers, legal text, or secondary information. It tells screen readers that the enclosed text is less important or a note related to the main content.
- **Example:**

```html
<small>This is small text</small>
```

- **Use Case:** For fine print or less important information

### <span style="color: pink;"> 7. `<del>` - Deleted Text</span>

- **Purpose:** Shows text as deleted, usually with a strikethrough with semantic meaning.
- **Attributes:** None.
- **Example:**

```html
<del>This text is deleted</del>
```

- **Use Case:** Indicating corrections or outdated content.

### <span style="color: pink;"> 8. `<ins>` - Inserted Text</span>

- **Purpose:**Highlights inserted text, usually with an underline.
- **Attributes:**
  - `cite:` A URL that explains the change.
  - `datetime:` Date and time of the change.
- **Example:**

```html
<ins datetime="2024-12-20">Inserted text</ins>
```

- **Use Case:** Tracking edits or additions to content

### <span style="color: pink;"> 9. `<sub>` - Subscript Text</span>

- **Purpose:** Displays text as subscript and have semantic meaning.
- **Attributes:** None
- **Example:**

```html
H<sub>2</sub>O
```

- **Use Case:** For chemical formulas or mathematical indices

### <span style="color: pink;">10. `<sup>` - Superscript Text</span>

- **Purpose:** Displays text as superscript and have semantic meaning.
- **Attributes:** None
- **Example:**

```html
x<sup>2</sup>
```

- **Use Case:** For mathematical exponents or footnotes

### <span style="color: pink;">11. `<u>` - Underlined Text</span>

- **Purpose:** Underlines the text.
- **Attributes:** None
- **Example:**

```html
<u>This text is underlined</u>
```

- **Use Case:**To emphasize text visually

### <span style="color: pink;">12. `<s>` - Strikethrough Text</span>

- **Purpose:** Indicates text that is no longer relevant
- **Attributes:** None
- **Example:**

```html
<s>Old price</s> New price
```

- **Use Case:** For marking content as outdated

### <span style="color: pink;">13. `<abbr>` - Abbreviation</span>

- **Purpose:** Defines an abbreviation or acronym, providing a tooltip with the full form.
- **Attributes:**
  - `title:` Specifies the full form of the abbreviation.
- **Example:**

```html
<abbr title="World Health Organization">WHO</abbr>
```

- **Use Case:**To explain abbreviations

### <span style="color: pink;">14. `<cite>` - Citation</span>

- **Purpose:** Refers to a title of a work, like a book or a website..
- **Attributes:** None
- **Example:**

```html
<cite>To Kill a Mockingbird</cite>
```

- **Use Case:** To provide citations or references

### <span style="color: pink;">15. `<code>` - Inline Code</span>

- **Purpose:** Represents a fragment of computer code
- **Attributes:** None
- **Example:**

```html
<code>print("Hello, World!")</code>
```

- **Use Case:** For code snippets in documentation.

### <span style="color: pink;">16. `<pre>` - Preformatted Text</span>

- **Purpose:** Preserves whitespace, line breaks, and formatting.
- **Attributes:** None
- **Example:**

```html
<pre>
Line 1
Line 2
Line 3
</pre>
```

- **Use Case:** Displaying code blocks or formatted text.

### <span style="color: pink;">17. `<kbd>` - Keyboard Input</span>

- **Purpose:** Represents user keyboard input and has semantic meaning.
- **Attributes:** None
- **Example:**

```html
<kbd>Ctrl + C</kbd>
```

- **Use Case:** Documenting keyboard shortcuts.

### <span style="color: pink;">18. `<span>` - Inline Container</span>

- **Purpose:** A generic inline container for styling.
- **Attributes:** Any global attribute like `class`, `id`, or `style`.
- **Example:**

```html
<span style="color: red;">Red Text</span>
```

- **Use Case:** Applying custom styles or classes to inline content.

### <span style="color: pink;">19. `<bdo>` - Bi-Directional Override</span>

- **Purpose:**

1. **Overriding Text Direction:** Useful for correcting or changing the direction of text in multilingual documents.
2. **Handling RTL and LTR Content:** Helps in displaying text properly when mixing languages with different writing directions.

- **Attributes:**
  | Attribute | Description | Example Value |
  |-----------|-------------|---------------|
  | `dir` | Specifies the text direction. | `ltr` (left-to-right), `rtl` (right-to-left) |
- **Example:**

```html
<p>Default text direction: Hello World!</p>
<p>Reversed using <bdo dir="rtl">Hello World!</bdo></p>
```

- **Use Case:**Suppose you are writing a document in English but need to include a snippet in Arabic. You can use <bdo> to ensure the Arabic snippet is displayed correctly:

### <span style="color: pink;"> 20. `<address>` - Contact Information</span>

- **Purpose:** The `<address>` tag is used to provide contact information for its nearest enclosing article or document. This tag is **semantically meaningful** and typically renders text in italics by default in most browsers.
- **Attributes:** Any global attribute like `class`, `id`, or `style`.
- **Example:**

```html
<address>
  Written by <a href="mailto:author@example.com">Author Name</a>.<br />
  Visit us at:<br />
  123 Web Dev Lane,<br />
  Tech City, TC 45678<br />
</address>
```

- **Use Case:** Author/organization details

---

## <span style="color:#33ff00;"> HTML Tags Related to Quotations</span>

HTML provides specific tags for quoting text or referencing external sources. These tags help differentiate quoted or cited text visually and semantically.

### <span style="color: pink;"> 1. `<q>` - Inline Quotation</span>

- The `<q>` tag is used for short inline quotations. It generally renders text with quotation marks around it.

#### **Attributes**

| Attribute | Description                            | Example Value                 |
| --------- | -------------------------------------- | ----------------------------- |
| `cite`    | Specifies the source of the quotation. | `https://example.com/article` |

#### **Example**

```html
<p>He said, <q cite="https://example.com">HTML is easy to learn!</q></p>
```

### <span style="color: pink;"> 2. `<blockquote>` - Block Quotation</span>

- The `<blockquote>` tag is used for longer quotations that typically span multiple lines. It often renders with indentation to distinguish the quoted content.

#### Attributes

| Attribute | Description                            | Example Value               |
| --------- | -------------------------------------- | --------------------------- |
| `cite`    | Specifies the source of the quotation. | https://example.com/article |

#### Example

```html
<blockquote cite="https://example.com">
  The world of programming is vast and ever-evolving. Stay curious!
</blockquote>
```

#### Purpose

- For quoting long passages or blocks of text.
- Can optionally include the source using the cite attribute.
