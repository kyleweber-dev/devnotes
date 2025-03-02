# CSS Dev Notes and Tips

## CSS Selectors Cheat Sheet

### ID and Class Selectors

```css
#idName {
  /* Styles for an element with a specific ID */
}

.className {
  /* Styles for elements with this class */
}
```

### Attribute Selectors

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

### Using Attribute Selectors on Different Elements

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

/* Select all buttons with a class that contains 'primary' */
button[class*="primary"] {
  background-color: green;
  color: white;
}

/* Select paragraphs that contain a specific word */
p[class~="highlight"] {
  background-color: yellow;
}

/* Select divs with an ID that starts with 'section-' */
div[id^="section-"] {
  padding: 10px;
  border: 2px solid gray;
}

/* Select all forms that have a method attribute */
form[method] {
  border: 1px solid red;
}

/* Select all labels associated with a specific input */
label[for] {
  font-weight: bold;
}
```

## Element Selection Techniques

### Selecting Child and Descendant Elements

```css
/* Selects all <p> inside #id or .class, regardless of depth */
#id p {
  color: blue;
}

.class p {
  color: blue;
}

/* Selects only direct child <p> inside #id or .class*/
#id > p {
  font-weight: bold;
}

.class > p {
  font-weight: bold;
}
```

### Selecting Adjacent and Sibling Elements

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

/* Selects every third <div> */
div:nth-child(3n) {
  border: 2px solid black;
}
```

### First and Last of Type

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

### Only Child and Only-of-Type

```css
/* Selects elements that are the only child of their parent */
p:only-child {
  font-weight: bold;
}

/* Selects elements that are the only one of their type within a parent */
p:only-of-type {
  text-transform: uppercase;
}
```
