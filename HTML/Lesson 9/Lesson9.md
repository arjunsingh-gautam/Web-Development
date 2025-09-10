## <span style="color:orange">Form Tags:</span>

- The `<form>` tag in HTML is used to create a web form for user input.
- A form can contain a variety of elements like text fields, checkboxes, radio buttons, submit buttons, etc., to collect user data.
- Forms are essential for interactive websites, allowing users to register, fill out surveys, log in, and more.

### <span style="color:violet">`<form>` Tag Attributes:</span>

- `action`: Specifies where to send the form data when the form is submitted. Usually, it's a URL to a server-side script.
- `method`: Defines the HTTP method for sending data: get (default, data is appended to the URL) or post (data is sent in the request body).
- `enctype`: Specifies how the form data should be encoded when submitting it to the server (used with method="post"). Common values include application/x-www-form-urlencoded (default), multipart/form-data (for uploading files), and text/plain.
- `name`: Specifies the name of the form.
- `novalidate`: Indicates the form should not be validated on submission.
- `autocomplete`: Specifies whether a form should have autocomplete on or off.

### <span style="color:violet">Form Elements:</span>

- `<input>`: The most versatile form element, with a variety of types to handle different inputs like text, password, submit button, radio buttons, checkboxes, etc.
- `<label>`: Provides a label for an `<input>` element, improving accessibility and user experience.
- `<textarea>`: Allows for multi-line text input.
- `<button>`: Represents a clickable button, which can be configured for various purposes like submitting the form, resetting its fields, or custom JavaScript actions.
- `<select>` and `<option>`: Create a drop-down list.
- `<fieldset>`: Groups related elements in a form.
- `<legend>`: Defines a caption for the `<fieldset>` element.
- `<output>`: Represents the result of a calculation or user action.

### <span style="color:violet">Input Types:</span>

- `text`: A single-line text field.
- `password`: A single-line text field that masks the input.
- `submit`: A button that submits the form.
- `reset`: A button that resets all form controls to their initial values.
- `radio`: A radio button, allowing a single choice among multiple options.
- `checkbox`: A checkbox, allowing single or multiple selections.
- `button`: A clickable button with no default behavior.
- `file`: A file select control, with a button to browse files.
- `hidden`: An invisible field that carries data.
- `image`: An image-based submit button.
- `date`, `time`, `datetime-local`: For date and time input.
- `month`, `week`: For selecting a month or a week.
- `number`: For numeric input.
- `range`: A slider for selecting a value within a range.
- `email`: For email addresses, with built-in validation.
- `url`: For URLs, with built-in validation.
- `search`: For search queries, may include a "clear" button on some browsers.
- `color`: For color selection.
- `tel`: For telephone numbers, with minimal validation.

### Example Form:

```html
<form action="/submit-form" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="user_name" />

  <label for="email">Email:</label>
  <input type="email" id="email" name="user_email" />

  <input type="submit" value="Submit" />
</form>
```
