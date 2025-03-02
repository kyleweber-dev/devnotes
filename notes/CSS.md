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
