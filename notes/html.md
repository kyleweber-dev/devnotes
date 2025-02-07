# HTML Notes

## Introduction

> This page contains my detailed notes about HTML. I'll use this as a reference to document everything I learn while working with HTML, including tags, attributes, best practices, and more.

---

## Table of Contents

- [Introduction](#introduction)
- [Basic Tags](#basic-tags)
- [Attributes](#attributes)
- [HTML Structure](#html-structure)
- [Forms and Inputs](#forms-and-inputs)
- [Semantic Elements](#semantic-elements)
- [Best Practices](#best-practices)

---

## Basic Tags

### What are Tags?

Tags are the building blocks of HTML. They define the structure and content of a webpage. Most tags come in pairs with an opening tag (`<tag>`) and a closing tag (`</tag>`).

### Common Tags

- `<html>`: Defines the root of an HTML document.
- `<head>`: Contains metadata and links (e.g., stylesheets, scripts).
- `<body>`: Contains the content displayed on the webpage.
- `<Main>`: This is fot the main content of the page. (`<body>` goes here)
- `<Header>`: The head of the document (`<Nav>` would go here)
- `<Footer>`: This is the footer of the document.
- `<h1>` to `<h6>`: Heading tags for different levels of importance.
- `<p>`: Paragraph tag for text.
- `<a>`: Anchor tag for links.
- `<img>`: Image tag to display pictures.
- `<!-- -->`: Comment tag for leaving notes in the code.
- `<Section>`: Tag for grouping similiter content.
- `<Div>`: Tag for grouping content
- `<Form>`: Used to group an input
- `<Lable>`: Used to add text to inputs (Lable needs a `<p>` inside of it to show text)
- `<Button>`: Used to make a button (Can )

---

## Attributes

### What are Attributes?

Attributes provide additional information about an element. They are written inside the opening tag and follow a `name="value"` format.

### Common Attributes

- `id`: Specifies a unique identifier for an element.
- `class`: Defines one or more classes for CSS or JavaScript targeting.
- `src`: Specifies the source file for images or scripts.
- `alt`: Provides alternative text for images.
- `href`: Specifies the URL for links.
- `style`: Adds inline CSS styles.

---

## Simple Start of HTML Webpage

```md
<!DOCTYPE html>
<html lang="en"> <!-- This sets the page language -->
<head>
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hello World</h1>
</body>
</html>
```

# HTML Input Best Practices Cheat Sheet

## 1. **Basic Input Structure**

Each input should:

- Be inside a `<form>` for proper submission.
- Have a `<label>` linked to it using the `for` attribute.
- Have a `name` attribute for data submission.
- Have an `id` that matches the `for` in the label.

```html
<form>
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required />
</form>
```

## 2. **Types of Inputs**

Text Input (Single Line)

```html
<label for="name">Full Name:</label>
<input
  type="text"
  id="name"
  name="name"
  placeholder="Enter your full name"
  required
/>
```

✅ Use `placeholder` for hints but always use a `<label>`. ✅ Use `required` to ensure input is filled.
