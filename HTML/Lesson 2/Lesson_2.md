# <span style="color:orange">Lesson-2 Notes</span>

## <span style="color:yellow">HTML Attributes</span>

### <span style="color: pink;"> Key Points About Attributes</span>

1. **Always in Opening Tags:** Attributes are added to the opening tag of an HTML element.
2. **Key-Value Pairs:** Most attributes have a `name="value"` format.
3. **Case Insensitive:** Attribute names are not case-sensitive in HTML, but lowercase is recommended for consistency.
4. **Quotation Marks:** Attribute values should be enclosed in double (`"`) or single (`'`) quotes.

---

### <span style="color: pink;"> Common HTML Attributes</span>

| **Attribute** | **Description**                                            | **Example**                              |
| ------------- | ---------------------------------------------------------- | ---------------------------------------- |
| `id`          | Unique identifier for an element                           | `<div id="main"></div>`                  |
| `class`       | Specifies one or more class names for styling or scripting | `<p class="text"></p>`                   |
| `src`         | Specifies the source of an external resource (e.g., image) | `<img src="image.jpg" alt="Image">`      |
| `href`        | Specifies the URL for a link                               | `<a href="https://example.com">Link</a>` |
| `alt`         | Provides alternative text for images                       | `<img src="image.jpg" alt="Image">`      |
| `style`       | Inline CSS styling                                         | `<p style="color: red;">Text</p>`        |
| `title`       | Tooltip text displayed on hover                            | `<p title="Tooltip text">Hover me!</p>`  |

---

### <span style="color: pink;"> Example of Using Attributes</span>

```html
<a href="https://example.com" target="_blank" title="Visit Example"
  >Click Here</a
>
```

---

## <span style="color:yellow">HTML Case Sensitivity</span>

### <span style="color: pink;"> Case Sensitivity in HTML</span>

1. **Element Names:**

- HTML is not case-sensitive for element names.

- `<Div>` is interpreted the same as `<div>`.

2. **Attribute Names:**

- HTML attributes are also not case-sensitive.
- Both `class` and `CLASS` work the same, but lowercase is preferred.

3. **Attribute Values:**

- Attribute values can be case-sensitive depending on the context.
- For example:
  - URLs in the `href` attribute are case-sensitive on some servers (e.g., Linux-based servers).
  - CSS class names and IDs are case-sensitive.

### <span style="color: pink;"> Best Practices</span>

- Always use lowercase for element names and attribute names for consistency.
- Be mindful of case sensitivity in attribute values (e.g., `href`, `src`, `id`, and `class`).
