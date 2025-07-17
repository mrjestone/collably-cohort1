# Topic: The Structure of Everything (HTML)

### **Objective**
To understand and write semantic HTML, creating a well-structured webpage that accurately describes its content.

### **Recap of Today's Lecture**
*   **Semantic HTML** means using the right tag for the right job to give our content meaning.
*   We use structural elements like `<header>`, `<main>`, and `<footer>` to outline our page.
*   We use content tags like `<h1>`, `<p>`, `<a>`, and `<img>` to describe the content itself.

---

### **Today's Task: Create a "Portfolio" Skeleton**

Your mission is to create the basic structure for your future portfolio page. This task focuses purely on the HTML structure, not the styling.

1.  **Create Your Files:** Inside your `collably-bootcamp` folder, create a new folder named `portfolio-project`. Inside this new folder, create a file named `index.html`.
2.  **Basic Boilerplate:** Start your `index.html` with the standard HTML boilerplate.
    > **Pro Tip:** In VS Code, in an empty `.html` file, type `!` and press Enter. It will generate this for you.
3.  **Build the Structure:** Inside the `<body>` tag, create the following structure using semantic tags:
    *   A `<header>` element.
        *   Inside the header, add an `<h1>` with your name.
        *   Add a `<nav>` element. Inside the nav, add an unordered list `<ul>` with three list items `<li>`. Each list item should contain an `<a>` link for "About", "Projects", and "Contact". For now, the `href` can be `#` (e.g., `<a href="#">About</a>`).
    *   A `<main>` element.
        *   Inside the main, add a `<section>` for your "About Me" content.
            *   Give this section a `<h2>` that says "About Me".
            *   Add an `<img>` tag. For the `src`, you can use a placeholder image URL like `https://via.placeholder.com/150`. The `alt` text should describe the image.
            *   Add a few `<p>` tags with some text about your goals.
        *   Add another `<section>` for your "Projects".
            *   Give this section a `<h2>` that says "My Projects".
            *   (Leave this section empty for now).
    *   A `<footer>` element.
        *   Inside the footer, add a `<p>` with copyright text (e.g., `© 2025 Your Name`).
        *   Add a link to your GitHub profile.
4.  **Commit and Push:**
    *   Navigate into your main `collably-bootcamp` folder in the terminal.
    *   Stage all your changes (`git add .`).
    *   Commit your work with the message: `feat: Create initial HTML structure for portfolio page`.
    *   Push your changes to GitHub.