# Topic: Making it Look Good (CSS)

### **Objective**
To apply external CSS to an HTML document, understanding the box model, selectors, and core styling properties.

### **Recap of Today's Lecture**
*   We use **external stylesheets** to separate content from presentation.
*   CSS rules are made of a **selector** and a `property: value` pair.
*   **Class selectors** (`.my-class`) are the most common way to target elements.
*   The **Box Model** (`margin`, `padding`, `border`) controls the space around and inside our elements.

---

### **Today's Task: Add Basic Styling to Your Portfolio**

You will bring your portfolio skeleton to life with some fundamental CSS.

1.  **Create and Link CSS:**
    *   In your `portfolio-project` folder, create a new file named `style.css`.
    *   In `index.html`, add the following line inside your `<head>` tag to link the stylesheet:
        ```html
        <link rel="stylesheet" href="style.css">
        ```
2.  **Apply Body and Font Styles:**
    *   In `style.css`, select the `body` element.
    *   Set a `font-family` (e.g., `sans-serif`).
    *   Set a light `background-color` (e.g., `#f4f4f4`).
    *   Remove the default `margin` by setting `margin: 0;`.
3.  **Style the Container:**
    *   Let's create a `.container` class to center our content.
        ```css
        .container {
          width: 80%; /* Takes up 80% of the screen width */
          max-width: 960px; /* But won't get bigger than 960px on large screens */
          margin: 0 auto; /* The magic trick for centering block elements */
        }
        ```
    *   In your `index.html`, add `class="container"` to your `<header>`, `<main>`, and `<footer>` elements.
4.  **Style the Header:**
    *   Select your `header`.
    *   Give it a `background-color` (e.g., `#333`), a `color` of `white`, and some `padding` (e.g., `20px`).
    *   Style the navigation links (`nav a`) to be white and have `text-decoration: none;`.
5.  **Style the Sections:**
    *   Select all `section` elements.
    *   Give them a white `background-color`, some `padding`, and a `margin-top` of `20px`.
6.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Add basic CSS styling to portfolio page`.
    *   Open your `index.html` file in your browser to see your styled page!