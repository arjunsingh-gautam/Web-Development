# <span style="color:orange">**CSS Selectors**</span>

- CSS selectors are the part of CSS rulesets that determine which HTML elements should be styled by the defined properties and values.

1. **ID Selector:**

- Targets an element based on its id attribute. Each ID should be unique within a page.

```css
#header {
  background-color: navy;
  color: white;
}
```

2. **Element Selector:**

- Targets all instances of a particular HTML element.

```css
p {
  margin: 20px;
  line-height: 1.5;
}
```

3. **Class Selector:**

- Targets all elements that have a specific class attribute.

```css
.highlight {
  background-color: yellow;
}
```

4. **Universal Selector:**
   Applies to all elements in the document.
   css

```css
* {
  box-sizing: border-box;
}
```

5. **Group Selector:**

- Allows you to target multiple specific selectors and apply the same styles to all selected elements.

```css
h1,
h2,
h3 {
  font-family: Arial, sans-serif;
}
```

6. **Attribute Selector**
   > Attribute selectors in CSS allow you to target elements based on the presence, value, or partial value of their attributes. They provide a powerful way to apply styles to specific elements without needing to add additional classes or IDs. Let's explore the attribute selectors with a code snippet:

### Syntax:

- `[attribute]:` Selects elements that have the specified attribute.
- `[attribute=value]`: Selects elements with the specified attribute and value.
- `[attribute~=value]`: Selects elements with an attribute value containing a specified word.
- `[attribute|=value]`: Selects elements with an attribute value starting with a specified value, followed by a hyphen.
- `[attribute^=value]`: Selects elements with an attribute value starting with a specified value.
- `[attribute$=value]`: Selects elements with an attribute value ending with a specified value.
- `*[attribute=value]**`: Selects elements with an attribute value containing the specified value.
  Example:
  Suppose we have the following HTML:

```html
<input type="text" id="username" placeholder="Enter your username" />
<input type="password" id="password" placeholder="Enter your password" />
<button data-action="submit">Submit</button>
<a href="#" target="_blank" title="Visit our website">Visit Website</a>
```

Code Snippet:

```css
/* Selects all elements with a 'placeholder' attribute */
input[placeholder] {
  color: #999; /* Changes the text color of inputs with placeholder attribute */
}

/* Selects the input element with id 'username' */
input#username {
  border: 1px solid #ccc; /* Adds a border to the username input */
}

/* Selects the button element with a 'data-action' attribute equal to 'submit' */
button[data-action="submit"] {
  background-color: #007bff; /* Changes the background color of the submit button */
}

/* Selects the anchor element with a 'title' attribute containing the word 'website' */
a[title~="website"] {
  font-weight: bold; /* Makes the text bold for links with title containing 'website' */
}
```

### In this example:

- `input[placeholder]` selects all `<input>` elements that have a placeholder attribute.
- `input#username` selects the `<input>` element with the id of username.
- `button[data-action="submit"]` selects the `<button>` element with a data-action attribute equal to "submit".
- `a[title~="website"]` selects `<a>` elements that have a `title` attribute containing the word `"website"`.

## <span style="coloe:pink">Specificity:</span>

- Specificity is a measure of how precise CSS selectors are—the more specific a selector, the higher priority it has in styling an element if multiple rules match. Specificity is calculated based on the number of ID selectors, class selectors, and element selectors.
- Inline styles (placed directly within an HTML element) always take precedence over styles in external stylesheets.
- IDs have a higher specificity than classes, and classes have higher specificity than type selectors (elements).
  Example:

```css
#header {
  /* Specificity = 100 */
  color: red;
}
.page-header {
  /* Specificity = 10 */
  color: blue;
}
h1 {
  /* Specificity = 1 */
  color: green;
}
```

> In the above example, if `h1` has `id="header"` and `class="page-header"`, it will be `red` because ID selectors have the highest specificity.

## <span style="color:pink">Inheritance:</span>

- In CSS, some properties are inherited by the children of an element if they aren't defined on the children themselves. Common inherited properties include `font-family`, `color`, and `text-align`.
- Some properties, like `border or padding,` do not inherit.

### Where inheritance does not work:

- For properties that do not inherit by default, you can force inheritance using the `inherit` value.
  Example:

```css
body {
  font-family: "Open Sans", sans-serif;
  color: darkblue;
}
.no-inherit {
  color: inherit; /* This will force the element to inherit the color from its parent */
}
```

### Solving inheritance issues:

> If a property isn't naturally inherited but you want it to be, you can explicitly set it to `inherit`. This tells the element to take the same computed value as its parent for that property.

## Parent Element

A parent element in HTML is one that encloses another element. It's directly above another element in the DOM tree. Any element that contains another element inside it is considered a parent to that enclosed element.

For example, in the following HTML snippet, `<div>` is the **parent element**:

```html
<div>
  <!-- Parent -->
  <p>This is a paragraph inside a div.</p>
  <!-- Child -->
</div>
```

## Child Element

A child element is an element that is directly enclosed in another element. It's directly below another element in the DOM hierarchy. In the example above, `<p>` is the child element of `<div>`.

> Children inherit CSS properties from their parents if those properties are **inheritable**.
> For instance, if you set the `font-family or color` on a parent element, the child elements will inherit those styles by default unless they have overridden styles applied directly to them

## Descendant Selector

The descendant selector, represented by a space ( ) in CSS, **targets all elements that are descendants of a specified element, regardless of how deeply nested they are within the DOM tree.** It selects not only direct children but also all subsequent generations of descendants.

```css
/* Descendant selector */
parentElement descendantElement {
  /* Styles */
}
```

Example:

```html
<div class="parent">
  <div>
    <p>This is a descendant paragraph.</p>
    <!-- Selected by .parent p selector -->
  </div>
</div>
```

```css
.parent p {
  color: blue; /* Styles applied to all <p> elements inside .parent */
}
```

## Direct Child Selector

The direct child selector, represented by the > symbol in CSS, targets only those elements that are direct children of a specified parent element. It does not target elements nested deeper in the DOM hierarchy; it only selects the immediate children.

```css
/* Direct child selector */
parentElement > childElement {
  /* Styles */
}
```

Example:

```html
<div class="parent">
  <div>
    <p>This is a descendant paragraph.</p>
    <!-- Not selected by .parent > p selector -->
  </div>
  <p>This is a direct child paragraph.</p>
  <!-- Selected by .parent > p selector -->
</div>
```

```css
.parent > p {
  color: red; /* Styles applied to direct child <p> elements of .parent */
}
```

### Differences and Usage

1. **Scope:**
   - Descendant selectors target elements at any level of nesting within the parent element.
   - Direct child selectors target only elements that are immediate children of the parent element.
2. **Specificity:**
   - Direct child selectors are more specific than descendant selectors because they target a narrower scope.
   - Using direct child selectors can help avoid unintentional styling of deeply nested elements that you may not want to affect.
3. **Performance:**
   - Direct child selectors are generally more efficient in terms of CSS performance since they only target immediate children, reducing the number of elements that need to be checked against the selector.
4. **Use Cases:**
   - Descendent selectors are useful for applying styles to all descendants of a parent element, regardless of their depth in the DOM tree.
   - Direct child selectors are handy when you want to style only the immediate children of a parent element, such as styling specific components in a layout or menu structure.

## `!important`

> In CSS, the `!important keyword` is used to give a declaration higher specificity, overriding any conflicting styles applied to an element, even if those styles have higher specificity or come later in the stylesheet.

Here's how it works:

```css
selector {
  property: value !important;
}
```

- When `!important` is added to a declaration, it tells the browser to prioritize that specific style above all others, regardless of specificity or source order. This can be useful for overriding styles that are difficult to change or for applying critical styles that must not be overridden.

- However, it's generally considered a best practice to use `!important` **sparingly**, as it can make your CSS harder to maintain and debug, especially in larger projects. It can also lead to specificity wars and make it more challenging to predict how styles will cascade.
