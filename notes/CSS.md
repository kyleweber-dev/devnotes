# CSS Dev Notes and Tips

## CSS Selectors Cheat Sheet

### ID and Class Selectors

**Definition:** Used to style elements based on their unique ID or shared class name.

**Use Cases:**

- Use `#idName` when you need to target a unique element on the page.
- Use `.className` to apply styles to multiple elements that share the same class.

```css
#idName {
  /* Styles for an element with a specific ID */
}

.className {
  /* Styles for elements with this class */
}
```

### Attribute Selectors

**Definition:** Allows selection of elements based on their attributes and attribute values.

**Use Cases:**

- Useful for styling elements dynamically based on attribute values (e.g., links, form inputs, images).
- Great for targeting elements without relying on classes or IDs.

```css
/* Attribute Exists */
[attribute] {
  /* Selects elements that have the attribute */
}

/* Attribute Equals */
[attribute="value"] {
  /* Selects elements where the attribute matches exactly */
}

/* Attribute Starts With */
[attribute^="value"] {
  /* Selects elements where the attribute starts with the given value */
}

/* Attribute Ends With */
[attribute$="value"] {
  /* Selects elements where the attribute ends with the given value */
}

/* Attribute Contains */
[attribute*="value"] {
  /* Selects elements where the attribute contains the given value */
}

/* Attribute Contains Word */
[attribute~="value"] {
  /* Selects elements where the attribute contains a whole word (space-separated) */
}

/* Attribute Contains Substring */
[attribute|="value"] {
  /* Selects elements where the attribute is exactly 'value' or starts with 'value-' */
}
```

### Pseudo-Classes and Pseudo-Elements

**Definition:**

- **Pseudo-classes** select elements based on their state, position, or interaction.
- **Pseudo-elements** style specific parts of an element, like the first letter or first line.

**Use Cases:**

- Styling interactive elements like buttons when hovered or clicked.
- Applying styles to the first letter, first line, or placeholder text.

#### Pseudo-Classes

```css
/* Change link color when hovered */
a:hover {
  color: red;
}

/* Style visited links differently */
a:visited {
  color: purple;
}

/* Change button appearance when active (clicked) */
button:active {
  background-color: darkblue;
}

/* Style input fields when focused */
input:focus {
  border-color: blue;
}

/* Selects the first child of a parent */
p:first-child {
  font-style: italic;
}

/* Selects the last child of a parent */
p:last-child {
  text-decoration: underline;
}
```

#### Pseudo-Elements

```css
/* Style the first letter of a paragraph */
p::first-letter {
  font-size: 140%;
  font-weight: bold;
}

/* Style the first line of a paragraph */
p::first-line {
  font-style: italic;
}

/* Change the color of placeholder text in inputs */
input::placeholder {
  color: gray;
}

/* Add content before an element */
p::before {
  content: "📌 ";
  color: red;
}

/* Add content after an element */
p::after {
  content: " ✅";
  color: green;
}
```

### Using Attribute Selectors on Different Elements

**Definition:** Demonstrates how to apply attribute selectors to specific HTML elements.

**Use Cases:**

- Styling links that start with `https`.
- Changing the appearance of checkboxes, buttons, and input elements.
- Targeting form elements based on attributes like `type` or `method`.

```css
/* Select all links that start with https */
a[href^="https"] {
  color: blue;
}

/* Select all images with a specific file extension */
img[src$=".png"] {
  border: 1px solid black;
}

/* Select all input elements of type checkbox */
input[type="checkbox"] {
  width: 20px;
  height: 20px;
}
```

## Element Selection Techniques

### Selecting Child and Descendant Elements

**Definition:** Allows targeting of nested elements inside a parent container.

**Use Cases:**

- Use `#id p` to select all `<p>` elements inside an ID container.
- Use `#id > p` to select only **direct children**.

```css
/* Selects all <p> inside #id, regardless of depth */
#id p {
  color: blue;
}

/* Selects only direct child <p> inside #id */
#id > p {
  font-weight: bold;
}
```

### Selecting Adjacent and Sibling Elements

**Definition:** Targets elements based on their placement relative to other elements.

**Use Cases:**

- Use `div + p` to select only the **next** `<p>` after a `<div>`.
- Use `div ~ p` to select **all** `<p>` elements that are siblings of a `<div>`.

```css
/* Selects the immediate <p> following a <div> */
div + p {
  color: red;
}

/* Selects all <p> that are siblings of a <div> */
div ~ p {
  background: lightgray;
}
```

### First, Last, and Nth Child Selectors

**Definition:** Selects elements based on their position among siblings.

**Use Cases:**

- Styling the first or last child in a list.
- Applying alternating styles using `nth-child(even)`.

```css
/* Selects the first child <p> of a parent */
p:first-child {
  font-style: italic;
}

/* Selects the last child <p> of a parent */
p:last-child {
  text-decoration: underline;
}

/* Selects every even-numbered <li> in a list */
li:nth-child(even) {
  background-color: lightblue;
}
```

### First and Last of Type

**Definition:** Selects the first or last element of a specific type within a parent.

**Use Cases:**

- Highlighting the first `<p>` in an article.
- Styling the last list item differently.

```css
/* Selects the first <p> of its type within a parent */
p:first-of-type {
  color: purple;
}

/* Selects the last <p> of its type within a parent */
p:last-of-type {
  color: green;
}
```
