# <span style="color:orange">HTML Basics</span>

- HTML is **not case-sensitive**

## <span style="color:orange">`<!DOCTYPE html>`</span>

- The <!DOCTYPE html> declaration is used to inform the browser about the version of HTML the page is written in. This declaration must be the very first thing in an HTML document, before the <html> tag. It tells the browser to interpret the document as HTML5.

## `<html>`

- The `<html>` element is the root element of an HTML page. It encapsulates the entire content of the document.

### <span style="color:orange">Attributes:</span>

- lang: Specifies the language of the document.

## 1. `<head>`

- The `<head>` element contains meta-information about the document, such as the title, links to stylesheets, scripts, and other meta tags.

- Common tags and attributes inside `<head>`:

### 1. `<meta>`: Defines meta-information about the document.

- charset: Specifies the character encoding for the document (e.g., UTF-8).
- name: Defines a name/value pair for meta-information.
- content: Specifies the value of the meta-information.

Example:

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### 2. `<title>`: Defines the title of the document, which appears in the browser's title bar or tab.

Example:

```html
<title>Title of the Document</title>
```

### `<meta name="author">`

- This meta tag specifies the author of the document.

```html
<meta name="author" content="John Doe" />
```

### `<meta name="description">`

- The description meta tag provides a brief summary of the content of the page. Search engines often use this information to display a snippet about the page in search results.

```html
<meta name="description" content="This is a description of the web page." />
```

### `<meta name="keywords">`

- The keywords meta tag was traditionally used to specify keywords relevant to the content of the page. However, most search engines no longer use this meta tag for ranking purposes.

```html
<meta name="keywords" content="HTML, CSS, JavaScript" />
```

### `<meta name="viewport">`

- The viewport meta tag controls the layout on mobile browsers. It ensures that the page is rendered correctly on various devices and screen sizes.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### 3. `<link>` tag attributes

- The `<link>` tag is used to link external resources, such as stylesheets, to an HTML document. Below are some common attributes used with the `<link>` tag:

  - `rel`: Specifies the relationship between the current document and the linked resource.
  - `href`: Specifies the URL of the linked resource.
  - `type`: Specifies the MIME type of the linked resource. For stylesheets, it is typically set to `"text/css"`.

  ***

  ***

> <span style="color: orange;">**The MIME Type of a Linked Resource**</span>
> The **MIME type** (Multipurpose Internet Mail Extensions type) of a linked resource refers to the type of content that a file or resource linked to a webpage represents. It is a way for servers and browsers to understand the type of data being sent or requested.
> For example, if a webpage links to a CSS file, the MIME type of that file would be `text/css`. Similarly, if it links to an image, the MIME type might be `image/png`, `image/jpeg`, or another image type.<br> <span style="color: pink;">**Why MIME Types Matter**</span></br><br>**Content Interpretation:** MIME types help the browser determine how to handle the linked resource. For instance:
>
> - A `text/html` MIME type tells the browser to interpret the file as an HTML document.
> - A `text/css` MIME type tells the browser the file contains stylesheets.
> - An `application/javascript` MIME type tells the browser it contains JavaScript.</br><br> **Security:** Incorrect MIME types can lead to vulnerabilities. For example:</br>
> - If a file intended to be downloaded as plain text (`text/plain`) is mistakenly interpreted as executable code (`application/javascript`), it could lead to a security risk.
>   **Performance and Behavior:** Proper MIME types ensure that resources like images, fonts, and scripts load and function correctly.

---

### `<link rel="icon"> or <link rel="shortcut icon">`

These meta tags are used to specify the favicon (short for "favorite icon") for the website, which is the small icon displayed in the browser tab next to the page title.

```html
<link rel="icon" href="favicon.ico" type="image/x-icon" />
or html

<link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
```

### `<meta http-equiv="refresh">`

- This meta tag is used to automatically refresh or redirect the page after a specified number of seconds.

```html
<meta http-equiv="refresh" content="5;url=https://www.example.com" />
```

> In the example above, the page will refresh after 5 seconds and redirect to https://www.example.com.

### 3. `title` Tag:Used to describe the title of Webpage in tab bar of brower

- Eg.

```html
<title>Chatgpt</title>
```

![title_bar](img/title.png)

---

---

## 2. `<body>`

- The `<body>` element **contains the content of the HTML document**, such as text, images, links, and other elements that are visible to the user.

### Common tags and attributes inside `<body>`:

- `<h1>` to `<h6>`: Defines headings of different levels.

Example:

```html
<h1>This is a Heading level 1</h1>
<h2>This is a Heading level 2</h2>
```

- `<p>`: Defines a paragraph.
  Example:

```html
<p>This is a paragraph.</p>
```

- `<a>`: Defines a hyperlink. - href: Specifies the URL to which the link points.
  Example:

```html
<a href="https://www.example.com">Visit Example.com</a>
```

- `<img>`: Inserts an image into the document. - src: Specifies the URL of the image. - alt: Provides a text description of the image.
  Example:

```html
<img src="image.jpg" alt="Description of the image" />
```
