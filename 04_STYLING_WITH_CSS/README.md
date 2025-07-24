
# Topic: Making it Look Good (CSS)

### **Objective**
To apply external CSS to an HTML document, understanding the box model, selectors, and core styling properties.

### **Recap of Today's Lecture**
*   We use **external stylesheets** to separate content from presentation.
*   CSS rules are made of a **selector** and a `property: value` pair.
*   **Class selectors** (`.my-class`) are the most common way to target elements.
*   The **Box Model** (`margin`, `padding`, `border`) controls the space around and inside our elements.

### **Pro-Tip: Install the Live Server Extension**
To make development easier, we recommend installing the **Live Server** extension in VS Code. It lets you see your changes in real-time without manually refreshing the browser.

1.  In VS Code, look at the vertical toolbar on the far left. Click the **Extensions** icon (it looks like four squares, with one flying off).
2.  In the search bar that appears at the top, type `Live Server`.
3.  Find the one by **Ritwick Dey** in the list and click the blue **Install** button next to it.

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
    *   Create a `.container` class to center our content.
        ```css
        .container {
          width: 80%;
          max-width: 960px;
          margin: 0 auto;
        }
        ```
    *   In your `index.html`, add `class="container"` to your `<header>`, `<main>`, and `<footer>` elements.
4.  **Style the Header:**
    *   Select your `header`. Give it a `background-color` (`#333`), a `color` of `white`, and `padding` (`20px`).
    *   Style the navigation links (`nav a`) to be white and have `text-decoration: none;`.
5.  **Style the Sections:**
    *   Select all `section` elements. Give them a white `background-color`, `padding`, and a `margin-top` of `20px`.
6.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Add basic CSS styling to portfolio page`.

---

### **7. View Your Page in the Browser 👀**

This is the fun part! Let's see your work.

*   **Recommended Method (with Live Server):**
    1.  In VS Code, find your `index.html` file in the file explorer on the left.
    2.  **Right-click** on the `index.html` file name.
    3.  Select **`Open with Live Server`** from the menu.
    4.  Your default web browser will automatically open a new tab showing your styled page!

*   **Manual Method (if Live Server isn't working):**
    1.  Open your computer's file manager (File Explorer on Windows).
    2.  Navigate to where you saved your `portfolio-project` folder.
    3.  **Double-click** the `index.html` file. It will open in your web browser.

### **8. Share Your Progress 🚀**

Now, let's share what you've accomplished. Follow these steps exactly.

**Step 1: Take a Screenshot**
Capture an image of your entire browser window showing your newly styled portfolio page.

**Step 2: Get Your GitHub Repository Link**

1.  Open your web browser and go to **`github.com`**.
2.  Log in to your account.
3.  On the main page, you'll see a list of your **Repositories** on the left. Click on your `portfolio-project` repository.
4.  Now, look at the **address bar at the very top of your browser**. The URL should look like this:
    `https://github.com/YourUsername/portfolio-project`
5.  Click inside that address bar. The entire link will turn blue. **Copy this link** (right-click and select `Copy`, or press `Ctrl+C`).

**Step 3: Post in the Discord Channel**

1.  Go to our Discord server and click on the **`#daily-progress`** channel.
2.  In the message box at the bottom, paste the GitHub link you just copied.
3.  Now, add your screenshot. You can either drag the screenshot file from your desktop into the Discord window or paste the screenshot you took on Windows directly (`Ctrl+V`).
4.  Add a nice message and hit Enter!

**Your post should look something like this:**

> Youre message if any
>
> *[Your screenshot will appear here]*
>
> your link to the code e.g: `https://github.com/YourUsername/portfolio-project`