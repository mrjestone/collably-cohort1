
***

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

1.  **Open Your Project:** In your VS Code terminal, navigate into your `portfolio-project` folder.
    ```bash
    cd portfolio-project
    ```

2.  **Prerequisite: Check for Node.js & npm**
    TailwindCSS is managed through `npm` (Node Package Manager), which comes bundled with Node.js. Before we continue, let's make sure you have it installed.

    *   **Check your version:** In your terminal, run the following command:
        ```bash
        node --version
        ```
    *   **If it's installed:** You will see a version number like `v20.10.0`. If so, you're all set! You can proceed to the next step.
    *   **If it's NOT installed:** You will get an error like "command not found". Follow these steps to install it:
        1.  Go to the official Node.js website: **[https://nodejs.org/](https://nodejs.org/)**
        2.  Download the installer for the **LTS** (Long-Term Support) version, as it's the most stable.
        3.  Run the installer and follow the on-screen instructions.
        4.  After installation is complete, **close and reopen your terminal** to ensure the command is available. Run `node -v` again to confirm. You should now see the version number.

3.  **Initialize NPM:** Now that you have `npm`, you can initialize your project. This command creates a `package.json` file, which will track your project's dependencies.
    ```bash
    npm init -y
    ```
4.  **Install Tailwind:** Run the following command to install TailwindCSS and its necessary peer dependencies.
    ```bash
    npm install -D tailwindcss
    npx tailwindcss init
    ```
    This creates `tailwind.config.js` and `postcss.config.js` files.

5.  **Configure Template Paths:** Open your `tailwind.config.js` file and tell Tailwind where to look for your HTML files so it knows which classes you're using.
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

6.  **Create Your CSS Entrypoint:** Create a new folder named `src` and inside it, a file named `input.css`. Add the following Tailwind "directives" to `input.css`:
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

7.  **Start the Build Process:** Run the following command in your terminal. This will watch your `input.css` file and your HTML for any changes, then automatically create your `output.css` file with all the styles you need.
    ```bash
    npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
    ```
    **Keep this terminal running in the background!**

8.  **Link the Output CSS:** In your `index.html`, remove the old `<link>` to `style.css` and replace it with the new compiled file:
    ```html
    <link href="./dist/output.css" rel="stylesheet">
    ```

#### **Part 2: Styling and Finishing Up**

Now, go through your `index.html` file and apply Tailwind classes directly to your HTML elements.

1.  **Body Styling:** Add classes directly to the `<body>` tag:
    `<body class="bg-slate-100 text-slate-800 font-sans">`
2.  **Container:** Your `.container` class is no longer needed in a CSS file. You can replicate its behavior with Tailwind classes:
    `<header class="w-full max-w-5xl mx-auto p-4">`
    Apply similar classes to `<main>` and `<footer>`.
3.  **Header & Nav:** Style your header with background, shadow, and flexbox utilities.
    *   Example for your `<header>`: `<header class="bg-white shadow-md">`
    *   Example for your `<nav>`'s `<ul>`: `<ul class="flex space-x-6">`
4.  **Sections:** Style your sections with padding, margins, and background colors to separate content.
    *   Example: `<section class="bg-white p-6 rounded-lg shadow-md mt-6">`
5.  **Typography:** Use classes like `text-4xl`, `font-bold`, `text-gray-500`, `mt-2` on your `<h1>`, `<h2>`, and `<p>` tags to create a clear visual hierarchy.
6.  **Responsive Design:** Make your header navigation stack vertically on small screens and switch to horizontal on medium screens and up.
    *   Example for the nav `<ul>`: `<ul class="flex flex-col items-center space-y-4 md:flex-row md:space-y-0 md:space-x-6">`
7.  **Commit and Push:**
    *   **Important:** Before committing, create a `.gitignore` file in your `portfolio-project` root and add `node_modules` to it. This tells Git to ignore this large folder.
    *   Stage all your files (`git add .`).
    *   Commit with a descriptive message: `refactor: Convert portfolio styling to TailwindCSS`.
    *   Push to your GitHub repository.

---

#### **Part 3: Share Your Work!**

1.  **Share Your Code:**
    *   Go to our Discord server and find the **`#daily-progress`** channel.
    *   Post the link to the GitHub repository you just pushed to. 
2.  **Share Your Result:**
    *   Take a screenshot of your live portfolio page in the browser.
    *   Post the screenshot in the same `#daily-progress` channel along with your link. This is the best way to showcase your design skills and see how far you've come.

