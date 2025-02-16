# Setting Up Tailwind CSS with Vite

Follow these steps to set up a Tailwind CSS project with Vite.

---

## **1. Create a Vite Project**

Open your terminal and run:

```sh
npm create vite@latest my-project
```

Replace my-project with your actual project name.

Navigate into the project folder:

```sh
cd my-project
```

---

## 2. Open the Project in VS Code

Once VSC is open make a new terminal

---

## 3. Install Tailwind CSS

Inside the terminal in VS Code, run:

```sh
npm install tailwindcss @tailwindcss/vite
```

---

## 4. Create a `vite.config.js` File

In the root directory of your project (where package.json is), create a file named vite.config.js and add:

```js
import { defineConfig } from "vite";
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [tailwindcss()],
});
```

---

## 5. Import Tailwind in Your CSS

Open `src/style.css` (or create it if it doesn’t exist) and add:

```html
<link href="/src/style.css" rel="stylesheet" />
```

This ensures Tailwind styles are applied.

---

## 7. Start Your Development Server

Run:

```sh
npm run dev
```

This will start the Vite server. You should now be able to use Tailwind classes in your HTML.

---

## 8. Test Tailwind

In your `index.html`, add this inside `<body>`:

```html
<h1 class="text-3xl font-bold underline">Hello world!</h1>
```

If you see a styled heading, Tailwind is working correctly!
