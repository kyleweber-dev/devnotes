# HTML Emmet Shortcuts Cheat Sheet

## 📌 What is Emmet?

**Emmet** is a powerful shortcut system built into most code editors (like VS Code) to generate HTML and CSS structures quickly.

---

## 🏗️ **Basic HTML Structure**

```emmet
! + [Enter]
```

✅ Generates a full HTML boilerplate:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

---

## 📂 **Creating Parent & Child Elements**

### **Basic Parent > Child Structure**

```emmet
div>p>span
```

✅ Expands to:

```html
<div>
  <p>
    <span></span>
  </p>
</div>
```

### **Multiple Sibling Elements**

```emmet
div+p+h1
```

✅ Expands to:

```html
<div></div>
<p></p>
<h1></h1>
```

### **Grouping Elements with ()**

```emmet
div>(header>nav)+(section>article>p)
```

✅ Expands to:

```html
<div>
  <header>
    <nav></nav>
  </header>
  <section>
    <article>
      <p></p>
    </article>
  </section>
</div>
```

---

## 🔢 **Numbering Elements**

### **Using `$` to Auto-Number Elements**

```emmet
ul>li.item$*5
```

✅ Expands to:

```html
<ul>
  <li class="item1"></li>
  <li class="item2"></li>
  <li class="item3"></li>
  <li class="item4"></li>
  <li class="item5"></li>
</ul>
```

---

## 🏷️ **Adding Classes & IDs**

### **Class Names (`.`)**

```emmet
div.container
```

✅ Expands to:

```html
<div class="container"></div>
```

### **Multiple Classes**

```emmet
div.card.box.shadow
```

✅ Expands to:

```html
<div class="card box shadow"></div>
```

### **ID (`#`)**

```emmet
div#main
```

✅ Expands to:

```html
<div id="main"></div>
```

### **ID + Class**

```emmet
div#hero.banner
```

✅ Expands to:

```html
<div id="hero" class="banner"></div>
```

---

## 🎯 **Shortcut for Forms & Inputs**

### **Basic Form with Inputs**

```emmet
form>input:text+input:password+input:email+button:submit
```

✅ Expands to:

```html
<form>
  <input type="text" />
  <input type="password" />
  <input type="email" />
  <button type="submit"></button>
</form>
```

### **Labeled Form Inputs**

```emmet
label[for="name"]{Name:}+input#name
```

✅ Expands to:

```html
<label for="name">Name:</label> <input id="name" />
```

---

## 📍 **Lists and Tables**

### **Unordered List with Items**

```emmet
ul>li*5
```

✅ Expands to:

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

### **Table Structure**

```emmet
table>thead>tr>th*3+tfoot>tr>td*3+tbody>tr*3>td*3
```

✅ Expands to:

```html
<table>
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>
```

---

## 🎨 **Shortcut for Images & Links**

### **Image with Alt Text**

```emmet
img[src="image.jpg" alt="A sample image"]
```

✅ Expands to:

```html
<img src="image.jpg" alt="A sample image" />
```

### **Anchor Link**

```emmet
a[href="https://example.com"]{Click Here}
```

✅ Expands to:

```html
<a href="https://example.com">Click Here</a>
```

---

## 🚀 **Time-Saving Tips**

✅ **Use `$`** to generate numbered class names.  
✅ **Use `>`** for child elements and `+` for siblings.  
✅ **Use `{}`** to insert text inside an element.  
✅ **Use `()`** to group elements and control nesting.

---

## 🔥 **Pre-Made Shortcuts**

### Header w/ Logo, 4 Nav Links, and 2 Buttons

```emmet
header#header>img.navLogo[alt="Company Logo"]+(nav.navLinks>ul.navList>li.navLink*4>a[href="#"]{Nav Link $})+(div.navBtns>button.nav.btn*2{Button $})
```

✅ Expands to:

```html
<header id="header">
  <img src="" alt="Company Logo" class="navLogo" />
  <nav class="navLinks">
    <ul class="navList">
      <li class="navLink"><a href="#">Nav Link 1</a></li>
      <li class="navLink"><a href="#">Nav Link 2</a></li>
      <li class="navLink"><a href="#">Nav Link 3</a></li>
      <li class="navLink"><a href="#">Nav Link 4</a></li>
    </ul>
  </nav>
  <div class="navBtns">
    <button class="nav btn">Button 1</button
    ><button class="nav btn">Button 2</button>
  </div>
</header>
```

### Hero section w/

```emmet
section#hero>div.heroContent>h1{Your Compelling Headline}+p{Supporting text with keywords for SEO}+a.heroBtn[href="#"]{Call to Action}^div.heroImage>img[alt="Hero Section Image"]
```

✅ Expands to:

```html
<section id="hero">
  <div class="heroContent">
    <h1>Your Compelling Headline</h1>
    <p>Supporting text with keywords for SEO</p>
    <a href="#" class="heroBtn">Call to Action</a>
  </div>
  <div class="heroImage"><img src="" alt="Hero Section Image" /></div>
</section>
```
