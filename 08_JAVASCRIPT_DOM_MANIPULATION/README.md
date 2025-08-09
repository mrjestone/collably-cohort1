# Topic: Bringing the Page to Life (DOM Manipulation)

### **Objective**
To use JavaScript to select HTML elements from the DOM, modify their content and style, and respond to user events like clicks.

### **Recap of Today's Lecture**
*   The **DOM (Document Object Model)** is a live, object-based map of our HTML page that JavaScript can interact with.
*   We use **`document.querySelector()`** to select an element using a CSS-style selector.
*   We can change an element's text with `.textContent` and its style with `.style`.
*   A better way to change style is to add/remove CSS classes using `.classList.add()` and `.classList.remove()`.
*   We use **`.addEventListener('click', myFunction)`** to make a function run when an element is clicked.

---

### **Today's Task: Create an Interactive "Profile Card"**

You will use your existing portfolio page and JavaScript to make it interactive. You'll add a button that changes the theme of the page.

#### **Part 1: Preparing the HTML and CSS**

1.  **Add a Button:** In your `portfolio-project/index.html` file, add a button inside your `<header>`. Give it an ID so you can easily select it.
    ```html
    <button id="theme-button">Toggle Dark Mode</button>
    ```

2.  **Add Dark Mode Styles:** At the bottom of your Tailwind `src/input.css` file, add some styles for a "dark mode". We will trigger these styles by adding a `.dark` class to the `<body>` element.
    ```css
    /* Add this AFTER the @tailwind directives */
    .dark {
        background-color: #111827; /* A dark gray */
        color: #d1d5db; /* A light gray for text */
    }

    .dark .bg-white {
        background-color: #1f2937; /* A slightly lighter gray for cards */
    }
    
    .dark .shadow-md {
        box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.4), 0 2px 4px -2px rgb(0 0 0 / 0.4);
    }
    ```
    > **Note:** Make sure your Tailwind build process (`npx tailwindcss --watch...`) is running so these new styles are added to your `output.css`.

#### **Part 2: The JavaScript Logic**

In your `portfolio-project/script.js` file, add the following logic:

1.  **Select the Elements:**
    *   At the top of your script, create a `const` variable named `themeButton` that selects the button with the ID `#theme-button`.
    *   Create another `const` variable named `bodyElement` that selects the `<body>` tag.

2.  **Create the Function:**
    *   Define a new function called `toggleTheme`. This function will not take any parameters.
    *   Inside the function, use `bodyElement.classList.toggle('dark')`. The `toggle` method is a shortcut that adds the class if it's not there, and removes it if it is.

3.  **Attach the Event Listener:**
    *   Add an event listener to your `themeButton`.
    *   The event you are listening for is `'click'`.
    *   The function that should run when the click happens is `toggleTheme`.

4.  **Test and Verify:**
    *   Open your `index.html` in the browser.
    *   When you click the "Toggle Dark Mode" button, the entire page should switch between your light and dark themes.

5.  **Bonus Task: Change Button Text**
    *   Modify your `toggleTheme` function.
    *   Inside it, add an `if/else` statement.
    *   **If** `bodyElement.classList.contains('dark')` is true, change the `themeButton.textContent` to "Toggle Light Mode".
    *   **Else**, change the `themeButton.textContent` back to "Toggle Dark Mode".

6.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Implement dark mode toggle with DOM manipulation`.