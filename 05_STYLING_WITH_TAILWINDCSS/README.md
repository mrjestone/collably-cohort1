# Topic: The Modern Way to Style (TailwindCSS)

### **Objective**
To set up TailwindCSS in a project and use its utility classes to build a clean, responsive design directly within the HTML.

### **Recap of Today's Lecture**
*   **Utility-First CSS** means we use small, single-purpose classes (like `p-4`, `font-bold`) instead of creating custom component classes.
*   This approach helps us work faster and keeps our CSS codebase from getting bloated.
*   Tailwind has built-in **responsive modifiers** (like `md:`, `lg:`) that make creating mobile-friendly layouts incredibly easy.

---

### **Today's Task: Refactor Your Portfolio with TailwindCSS**

You will remove the old `style.css` and re-style your portfolio page using only TailwindCSS utility classes.

#### **Part 1: Setting up TailwindCSS**

1.  **Open Your Project:** In your VS Code terminal, navigate into your `portfolio-project` folder. `cd portfolio-project`
2.  **Initialize NPM:** Tailwind is installed via `npm` (Node Package Manager). Run `npm init -y`. This will create a `package.json` file.
3.  **Install Tailwind:** Run the following command to install TailwindCSS:
    ```bash
    npm install -D tailwindcss
    npx tailwindcss init
    ```
    This creates `tailwind.config.js` and `postcss.config.js` files.
4.  **Configure Template Paths:** Open your `tailwind.config.js` file and tell Tailwind where to look for your HTML files.
    ```javascript
    /** @type {import('tailwindcss').Config} */
    module.exports = {
      content: ["./*.{html,js}"], // Looks for all .html and .js files in the root
      theme: {
        extend: {},
      },
      plugins: [],
    }
    ```
5.  **Create Your CSS Entrypoint:** Create a new folder named `src` and inside it, a file named `input.css`. Add the following lines to `input.css`:
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```
6.  **Start the Build Process:** Run the following command in your terminal. This will watch your `input.css` for changes and automatically create your `output.css` file with all of Tailwind's styles.
    ```bash
    npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
    ```
    Keep this terminal running in the background!
7.  **Link the Output CSS:** In your `index.html`, remove the old `<link>` to `style.css` and replace it with the new compiled file:
    ```html
    <link href="./dist/output.css" rel="stylesheet">
    ```

#### **Part 2: Styling with Utilities**

Now, go through your `index.html` file and replace the old structure with Tailwind classes.

1.  **Body Styling:** Add classes directly to the `<body>` tag:
    `<body class="bg-slate-100 text-slate-800">`
2.  **Container:** Your `.container` class is no longer needed in a CSS file. You can replicate it with Tailwind classes:
    `<header class="w-full max-w-5xl mx-auto p-4">`
    Apply similar classes to `<main>` and `<footer>`.
3.  **Header & Nav:** Style your header with background, shadow, and flexbox utilities.
    *   Example for your `<header>`: `<header class="bg-white shadow-md">`
    *   Example for your `<nav>`'s `<ul>`: `<ul class="flex space-x-4">`
4.  **Sections:** Style your sections with padding, margins, and background colors.
    *   Example: `<section class="bg-white p-6 rounded-lg shadow-md mt-6">`
5.  **Typography:** Use classes like `text-4xl`, `font-bold`, `text-gray-500`, `mt-2` on your `<h1>`, `<h2>`, and `<p>` tags.
6.  **Responsive Design:** Try making your header navigation stack vertically on small screens.
    *   Example for the nav `<ul>`: `<ul class="flex flex-col md:flex-row md:space-x-4">` (It's a column by default, but becomes a row on `md` screens and up).
7.  **Commit and Push:**
    *   **Important:** Before committing, create a `.gitignore` file in your `portfolio-project` root and add `node_modules` to it. This tells Git to ignore the thousands of files from the installation.
    *   Stage all your files (`git add .`).
    *   Commit with the message: `refactor: Convert portfolio styling to TailwindCSS`.
    *   Push to GitHub.

Open your `index.html` in the browser. It should now be styled with Tailwind!