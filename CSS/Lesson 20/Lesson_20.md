

# <span style="color:purple">**CSS Variables**</span>

* CSS Variables (also called **Custom Properties**) let you store values (like colors, fonts, sizes) and reuse them across your stylesheet.
* Declared using `--` (double dash).
* Accessed using `var()` function.

👉 They make CSS **dynamic, maintainable, and scalable**.

---

## 2. Syntax

### Declaring:

```css
:root {
  --main-color: #3498db;
  --padding-lg: 20px;
}
```

### Using:

```css
button {
  background-color: var(--main-color);
  padding: var(--padding-lg);
}
```

---

## 3. Naming Rules

✅ Must start with `--`
✅ Can contain letters, numbers, hyphens
✅ Case-sensitive (`--MainColor` ≠ `--maincolor`)
✅ You can’t use reserved CSS property names

👉 Good names:

* `--primary-color`, `--font-size-sm`, `--gap-large`
  👉 Bad names:
* `--123color`, `--background color` (spaces not allowed)

---

## 4. Scope Rules

* CSS variables follow **normal CSS cascading rules**.

### Global Scope:

Declared inside `:root` (the top-level element):

```css
:root {
  --text-color: black;
}
p {
  color: var(--text-color);
}
```

### Local Scope:

Declared inside a selector → only available within that element & its children:

```css
.card {
  --card-bg: lightgray;
  background: var(--card-bg);
}
```

👉 Analogy:

* `:root` variables = **global settings** (like app-wide theme).
* Local variables = **private settings** for a component.

---

## 5. Use Cases

1. **Theme Management** (light/dark mode):

```css
:root {
  --bg: white;
  --text: black;
}
.dark-mode {
  --bg: black;
  --text: white;
}
body {
  background: var(--bg);
  color: var(--text);
}
```

2. **Consistent Spacing & Sizing**

```css
:root {
  --gap: 10px;
}
.container {
  padding: var(--gap);
  margin: var(--gap);
}
```

3. **Dynamic Changes (with JS)**

```js
document.documentElement.style.setProperty('--main-color', 'red');
```

---

## 6. Why Variables are Important in CSS

* ✅ Avoid **repetition** (change once, update everywhere).
* ✅ Enable **themes and design systems**.
* ✅ Follow **DRY principle** (Don’t Repeat Yourself).
* ✅ Can be **changed at runtime** (e.g., with JS).
* ✅ Make code **readable and maintainable**.

---

## 7. Best Practices

* Define **global theme variables** in `:root`.
* Use **semantic names** (`--primary-color`, not `--blue`).
* Use **fallback values** in `var()` for safety:

```css
color: var(--not-defined, black);
```

* Keep variables organized (colors, spacing, typography).
* Override locally only when necessary.

---

## 8. Template

```css
/* Global variables */
:root {
  --primary-color: #4caf50;
  --secondary-color: #ff9800;
  --font-size-base: 16px;
  --spacing: 1rem;
}

/* Usage */
body {
  font-size: var(--font-size-base);
  background: var(--primary-color);
}

button {
  padding: var(--spacing);
  background: var(--secondary-color);
  color: white;
}
```

---

👉 **Analogy**:
Think of CSS variables like **containers of paint in a workshop**.

* Instead of painting each wall with a new mix, you **label buckets** (`--blue-paint`) and reuse them.
* If you change the paint in the bucket, **all walls painted with it automatically update**. 🎨

---


# 🔹 1. `:root` Pseudo-class in CSS

* `:root` is a **pseudo-class** that represents the **highest-level element** in the DOM.
* In HTML documents, `:root` = `<html>` element.
* Similar to `html`, but with **higher specificity** (because it’s a pseudo-class).

👉 Example:

```css
html {
  --color: blue;
}
:root {
  --color: red;
}
p {
  color: var(--color);
}
```

➡️ The text will be **red**, because `:root` has higher specificity than `html`.

---

### ✅ Use Cases of `:root`

1. **CSS Variables (Custom Properties)**

   * Declaring global theme variables:

   ```css
   :root {
     --primary-color: #4caf50;
     --font-size: 16px;
   }
   ```
2. **Theme Switching** (light/dark mode overrides):

   ```css
   :root {
     --bg: white;
     --text: black;
   }
   .dark-mode {
     --bg: black;
     --text: white;
   }
   ```

👉 Think of `:root` as the **master stylesheet hub**.

---

# <span style="color:yellow">**🔹 2. `box-shadow` Property in CSS**</span>

The **`box-shadow`** property adds shadow effects to elements.

### ✅ Syntax

```css
box-shadow: offset-x offset-y blur-radius spread-radius color inset;
```

### Parameters:

1. **offset-x** → horizontal shadow position

   * `+ve` = right, `-ve` = left
2. **offset-y** → vertical shadow position

   * `+ve` = down, `-ve` = up
3. **blur-radius** *(optional)*

   * Bigger value = more blurred (default = 0 = sharp edge).
4. **spread-radius** *(optional)*

   * Positive = shadow expands outward
   * Negative = shadow shrinks inward
5. **color** *(optional, default = current text color)*
6. **inset** *(optional keyword)*

   * Makes shadow **inside** the element instead of outside.

---

### ✅ Examples

```css
/* Simple shadow */
box-shadow: 5px 5px 10px gray;

/* With spread */
box-shadow: 5px 5px 15px 5px rgba(0,0,0,0.3);

/* Inner shadow */
box-shadow: inset 0 0 10px rgba(0,0,0,0.5);

/* Multiple shadows */
box-shadow: 2px 2px 5px red, -2px -2px 5px blue;
```

---

### ✅ Visualization

* `offset-x` → moves shadow left/right
* `offset-y` → moves shadow up/down
* `blur-radius` → controls softness
* `spread-radius` → controls size

👉 Example with annotation:

```css
box-shadow: 10px 10px 20px 5px rgba(0,0,0,0.25);
/*
10px → right
10px → down
20px → blur softness
5px  → spread
rgba(0,0,0,0.25) → shadow color
*/
```

---

### ✅ Use Cases

1. **Elevated Cards (Material Design style)**

   ```css
   .card {
     box-shadow: 0 4px 6px rgba(0,0,0,0.1);
   }
   ```
2. **Button Hover Effect**

   ```css
   button:hover {
     box-shadow: 0 0 10px rgba(0, 150, 255, 0.7);
   }
   ```
3. **Neumorphism (soft UI style)**

   ```css
   .box {
     box-shadow: 5px 5px 10px #aaa, -5px -5px 10px #fff;
   }
   ```

---

# 🔹 3. Best Practices for `box-shadow`

* Use **RGBA colors** for realistic shadows (opacity < 0.3).
* Keep shadows **subtle** (big blur, light opacity).
* Use multiple shadows for **depth** (inner + outer).
* Avoid overusing → can slow rendering if applied to many elements.

---

✅ **Summary**

* `:root` = highest-level element (like `html`), best for global **CSS variables**.
* `box-shadow` = property for **outer/inner shadows**, with 6 main parameters.
* Used for **UI depth, hover effects, neumorphism, and theming**.

---


