# <span style="color:darkcyan"> **`display` property** </span>

## 1. What is `display` in CSS?

- The **`display` property** defines **how an element is rendered in the document flow** (i.e., how it behaves as a box on the page).
- It controls:

  - Whether the element is **block-level, inline, flex, grid**, etc.
  - How children of the element are **laid out**.

---

## 2. Why do we need `display`?

- By default, HTML elements have their **own display types**:

  - `<div>` = `block`
  - `<span>` = `inline`
  - `<ul>` = `block`
  - `<li>` = `list-item`

- But sometimes you want them to behave differently (e.g., inline menu instead of vertical list). That’s where `display` comes in.

---

## 3. Values of `display` & Their Uses

### 🔹 Common Values

1. **`block`**

   - Starts on a new line, takes full width by default.
   - Eg: `<div>, <p>, <h1>`.
   - Use: For major layout containers.

   ```css
   div {
     display: block;
   }
   ```

2. **`inline`**

   - Flows with text, doesn’t force new line, only takes as much width as content.
   - Eg: `<span>, <a>, <strong>`.
   - Use: For styling words/phrases inside text.

   ```css
   span {
     display: inline;
   }
   ```

3. **`inline-block`**

   - Behaves like inline (sits in a line) but can have width/height.
   - Use: Buttons, nav items.

   ```css
   button {
     display: inline-block;
   }
   ```

4. **`none`**

   - Removes element from document flow (no space taken).
   - Use: Hide/show elements (toggle with JS).

   ```css
   .hidden {
     display: none;
   }
   ```

---

### 🔹 Layout-Specific Values

5. **`flex`**

   - Turns container into a **flexbox**, children are flex items.
   - Use: One-dimensional layouts (row or column).

   ```css
   .container {
     display: flex;
   }
   ```

6. **`inline-flex`**

   - Like `flex` but behaves as inline element in its parent.

7. **`grid`**

   - Turns container into **CSS Grid**.
   - Use: Two-dimensional layouts.

   ```css
   .grid {
     display: grid;
   }
   ```

8. **`inline-grid`**

   - Like `grid`, but inline with text flow.

---

### 🔹 Other Useful Values

9. **`list-item`**

   - Makes element behave like `<li>` with markers.

   ```css
   span {
     display: list-item;
   }
   ```

10. **`table`, `inline-table`**

    - Makes element behave like `<table>`.
    - Use: Rare; mostly replaced by flex/grid.

11. **`contents`**

    - Makes element disappear visually but its children remain.
    - Use: Semantic wrappers that shouldn’t affect layout.

12. **`run-in`** (deprecated, not widely supported).

---

## 4. Use Cases of `display`

- **`block`** → Layout sections (`div`, `header`, `footer`).
- **`inline`** → Styling text parts (`span`, `a`).
- **`inline-block`** → Buttons, nav links, badges.
- **`flex`** → Navbars, card layouts, vertical centering.
- **`grid`** → Dashboards, galleries, page templates.
- **`none`** → Conditional rendering, toggle menus.
- **`list-item`** → Custom bullet points.

---

## 5. Examples

```css
/* Example 1: Block vs Inline */
div {
  display: block; /* Takes full width */
}
span {
  display: inline; /* Flows with text */
}

/* Example 2: Inline-block buttons */
a {
  display: inline-block;
  padding: 10px;
  background: teal;
  color: white;
}

/* Example 3: Flexbox Layout */
nav {
  display: flex;
  justify-content: space-between;
}

/* Example 4: Grid Layout */
section {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

---

## 6. Best Practices

✔ Use `flex` for **1D layouts** (rows/columns).
✔ Use `grid` for **2D layouts** (rows + columns).
✔ Use `inline-block` for small items like nav links/buttons if you don’t want flex.
✔ Avoid using `display: none;` for accessibility-critical elements (screen readers might miss them). Use `visibility: hidden;` if you want them invisible but still occupying space.
✔ Don’t overuse `inline` on block-level elements (can break layout).

---

## 7. General Template

```css
/* Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Block container */
.container {
  display: block;
  width: 80%;
  margin: auto;
}

/* Inline-block nav */
.nav-item {
  display: inline-block;
  margin: 0 10px;
}

/* Flexbox */
.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Grid */
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

/* Hide temporarily */
.hidden {
  display: none;
}
```

---

## <span style="color:orange"> **core difference between block vs inline elements** </span>

### Why Inline Elements Behave Differently

By default:

- **Block elements** (`div`, `p`, `h1`, `ul`, etc.):

  - Occupy the **full available width**.
  - Start on a **new line**.
  - Can have **all box model properties** (`margin`, `padding`, `border`, `width`, `height`) applied normally.

- **Inline elements** (`span`, `a`, `em`, `strong`):

  - Sit **within a line of text**.
  - Width/height are **defined by content only** (you cannot set custom width/height).
  - Box properties behave differently:

    - ✅ Horizontal padding/margin works.
    - ❌ Vertical padding/margin doesn’t push surrounding lines apart (only overlaps).
    - ❌ Width/height ignored.

---

### Why We Need `display` for Inline Elements

When you want inline elements (like `<a>`, `<span>`, `<strong>`) to behave like a **box** (e.g., button or card), you **change their `display`**:

1. **`inline-block`**

   - Keeps element inline with text, **but** allows width, height, padding, margin, border to behave like block elements.

   ```css
   a {
     display: inline-block;
     padding: 10px;
     margin: 5px;
     border: 2px solid teal;
     background: lightblue;
   }
   ```

2. **`block`**

   - Makes inline element behave as a full-width block element.

   ```css
   span {
     display: block;
     width: 200px;
     padding: 10px;
     background: yellow;
   }
   ```

3. **`flex` / `grid`**

   - Allows inline elements to act as **containers for layout**.

   ```css
   a {
     display: flex;
     justify-content: center;
     align-items: center;
     padding: 10px;
   }
   ```

---

### Example: Inline vs Inline-Block vs Block

```html
<a href="#">Link 1</a> <a href="#">Link 2</a>
```

```css
/* Default (inline) */
a {
  padding: 10px; /* horizontal works, vertical overlaps */
  margin: 20px; /* top/bottom ignored */
  border: 2px solid red;
}

/* Change to inline-block */
a {
  display: inline-block;
  padding: 10px;
  margin: 20px; /* now works in all directions */
  border: 2px solid red;
}

/* Change to block */
a {
  display: block;
  width: 200px;
  margin: 10px auto;
  padding: 10px;
  background: lightblue;
}
```

---

# 📌 Why We Cannot Directly Apply Box Properties to Inline Elements

- CSS was originally designed for **text documents**, where inline elements (like `<span>`, `<em>`) are **part of a line of text**.
- Applying full block-level box properties would **break line flow** and spacing.
- That’s why **vertical margins/padding don’t shift lines**, and width/height are ignored.

So, to style them as “boxes” (buttons, nav items, badges), we **switch their display type**.

---

### Best Practices

✔ Keep `<span>` and `<a>` inline when just styling text.
✔ Use `inline-block` for small UI elements like **buttons, menu items, tags**.
✔ Use `block` for full-width clickable sections.
✔ Use `flex`/`grid` when the element should also be a **layout container**.

---
