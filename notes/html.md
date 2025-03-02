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

### Semantic Elements

- `<article>`: **Definition:** Represents a self-contained, independent piece of content, such as a blog post or news article. **Best Use Case:** Blog posts, news articles, or forum posts.
- `<section>`: **Definition:** Defines a section of content that typically has a heading. **Best Use Case:** Grouping related content within a webpage, such as different sections of an article.

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

## 1. **Basic Form Structure**

Each input should:

- Be inside a `<form>` to allow submission.

- Have a `<label>` linked using the for attribute.

- Have a name attribute for data submission.

- Have an id matching the for in the label.

- Have class attributes for easy styling.

```html
<form action="submit.php" method="POST" class="form-container">
  <fieldset class="form-group">
    <legend class="form-title">User Information</legend>

    <label for="username" class="form-label">Username:</label>
    <input
      type="text"
      id="username"
      name="username"
      class="form-input"
      required
    />

    <label for="email" class="form-label">Email:</label>
    <input type="email" id="email" name="email" class="form-input" required />

    <label for="password" class="form-label">Password:</label>
    <input
      type="password"
      id="password"
      name="password"
      class="form-input"
      required
    />
  </fieldset>

  <button type="submit" class="form-button">Submit</button>
</form>
```

## 2. Types of Inputs with Classes

**Text Input (Single Line)**

```html
<label for="name" class="form-label">Full Name:</label>
<input
  type="text"
  id="name"
  name="name"
  class="form-input"
  placeholder="Enter your full name"
  required
/>
```

**Multiline Text (Textarea)**

```html
<label for="message" class="form-label">Message:</label>
<textarea
  id="message"
  name="message"
  class="form-textarea"
  rows="4"
  placeholder="Type your message here..."
></textarea>
```

**Email Input**

```html
<label for="email" class="form-label">Email:</label>
<input type="email" id="email" name="email" class="form-input" required />
```

**Password Input**

```html
<label for="password" class="form-label">Password:</label>
<input
  type="password"
  id="password"
  name="password"
  class="form-input"
  required
/>
```

**Number Input**

```html
<label for="age" class="form-label">Age:</label>
<input
  type="number"
  id="age"
  name="age"
  class="form-input"
  min="18"
  max="100"
  required
/>
```

**Date Input**

```html
<label for="dob" class="form-label">Date of Birth:</label>
<input type="date" id="dob" name="dob" class="form-input" required />
```

**Radio Buttons (Single Choice Selection)**

```html
<p class="form-label">Choose your gender:</p>
<input
  type="radio"
  id="male"
  name="gender"
  value="male"
  class="form-radio"
  required
/>
<label for="male" class="form-label">Male</label>

<input
  type="radio"
  id="female"
  name="gender"
  value="female"
  class="form-radio"
/>
<label for="female" class="form-label">Female</label>
```

**Checkboxes (Multiple Choice Selection)**

```html
<p class="form-label">Select your interests:</p>
<input
  type="checkbox"
  id="coding"
  name="interests"
  value="coding"
  class="form-checkbox"
/>
<label for="coding" class="form-label">Coding</label>

<input
  type="checkbox"
  id="music"
  name="interests"
  value="music"
  class="form-checkbox"
/>
<label for="music" class="form-label">Music</label>
```

**Dropdown (Select Menu)**

```html
<label for="country" class="form-label">Select your country:</label>
<select id="country" name="country" class="form-select" required>
  <option value="">-- Select --</option>
  <option value="us">United States</option>
  <option value="uk">United Kingdom</option>
</select>
```

## 3. Form Submission (Button)

```html
<button type="submit" class="form-button">Submit</button>
```

## 4. CSS Styling Guide

```css
.form-container {
  width: 100%;
  max-width: 400px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.form-group {
  margin-bottom: 15px;
}

.form-title {
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.form-label {
  display: block;
  margin-bottom: 5px;
}

.form-input,
.form-textarea,
.form-select {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.form-radio,
.form-checkbox {
  margin-right: 5px;
}

.form-button {
  background-color: #28a745;
  color: white;
  padding: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.form-button:hover {
  background-color: #218838;
}
```

## 5. Common Best Practices

- ✅ Always use <label> for accessibility.

- ✅ Use name attributes for form submission.

- ✅ Use placeholder for hints, but don't rely on it.

- ✅ Use required, min, max, and pattern for validation.

- ✅ Group related inputs with <fieldset>.

- ✅ Use class attributes to style elements efficiently.
