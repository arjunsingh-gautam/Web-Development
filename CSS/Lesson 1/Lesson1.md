# <span style="color:orange">CSS Basics</span>

## <span style="color:pink">How CSS works?</span>

- CSS works by selecting HTML elements and applying styles to them. These styles can be defined directly within an HTML document, in a separate CSS file, or even applied directly to individual HTML elements using inline styles
- CSS follows a **cascade model**, meaning that multiple style rules can apply to the same element, and the most specific rule takes precedence.

## <span style="color:pink">CSS Ruleset</span>

- A CSS ruleset, also known as a style rule, is a fundamental building block of CSS (Cascading Style Sheets).
- It consists of a selector and one or more declarations.
- A ruleset defines how HTML elements that match the selector should be styled.

```css
selector {
  property1: value1;
  property2: value2;
  /* Additional properties and values */
}
```

1. **Selector:** The selector determines which HTML elements the CSS rules should apply to. Selectors can target elements based on various criteria, such as their tag name, class, ID, attributes, or their relationship to other elements.Examples of selectors:

   - Element selector: `p `targets all `<p>` elements.
   - Class selector: `.highlight` targets all elements with the highlight class.
   - ID selector: `#header` targets the element with the header ID.
   - Descendant selector: `div p` targets all `<p>` elements that are descendants of `<div>` elements.
   - Attribute selector: `input[type="text"]` targets all `<input> `elements with type="text" attribute.

2. **Declaration Block:** The declaration block is enclosed within curly braces `{}` and contains one or more declarations. Each declaration consists of a property and its corresponding value, separated by a colon `:`. Multiple declarations are separated by semicolons `;`

3.

- **Property:** Specifies the aspect of the element's appearance that you want to style, such as `color, font-size, background-color`, etc.
- **Value:** Specifies the value of the property, such as `blue, 14px, #FFFFFF,` etc.

## <span style="color:pink">Types of Styling</span>

- **Inline CSS:** Styles applied directly to individual HTML elements using the style attribute. For example:

```html
<h1 style="color: red;">Hello, world!</h1>
```

- **Internal CSS:** Styles defined within the `<style>` element in the `<head> `section of an HTML document. For example:

```html
<style>
  h1 {
    color: blue;
    font-size: 24px;
  }
</style>
```

- **External CSS:** Styles defined in a separate CSS file and linked to an HTML document using the `<link>` element. For example:

```html
<!-- In the <head> section of HTML -->
<link rel="stylesheet" type="text/css" href="styles.css" />
```

## Best practices:

- **Use External CSS:** It's generally recommended to use external CSS files to separate styles from content and improve maintainability.
- **Keep it Organized:** Group related styles together and use comments to document sections of your CSS code.
- **Be Specific but Concise:** Write selectors that are specific enough to target desired elements but not overly verbose.
- **Optimize for Performance:** Minify CSS files for faster loading times and consider using CSS frameworks or preprocessors for easier development.
