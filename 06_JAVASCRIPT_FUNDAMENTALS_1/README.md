
# Topic: JavaScript Fundamentals 1 - Variables, Data, and Operators

### **Objective**
To understand how to write basic JavaScript, declare variables to store data, use different data types, and perform simple operations.

### **Recap of Today's Lecture**
*   JavaScript adds interactivity to our websites.
*   We use `<script src="script.js" defer></script>` to link our JS file.
*   The **developer console** is where we use `console.log()` to check our work.
*   We use `const` by default to declare variables, and `let` only when a variable needs to change.
*   Core data types include **String**, **Number**, and **Boolean**.
*   **Template Literals** (`` ` ``) are the best way to combine strings and variables.

---

### **Today's Task: Your First Script**

You will create your first JavaScript file and use it to define and display information about yourself in the browser console.

1.  **Create and Link the File:**
    *   Inside your `portfolio-project` folder, create a new file named `script.js`.
    *   In your `index.html`, add the following line just before the closing `</body>` tag:
        ```html
        <script src="script.js" defer></script>
        ```

2.  **Using the Console:**
    *   In `script.js`, add your first line of code:
        ```javascript
        console.log("Hello from script.js!");
        ```
    *   Open `index.html` in your browser. Open the developer console (press `F12` or `Ctrl/Cmd + Shift + I` and click the "Console" tab). You should see your message.

3.  **Declare Your Variables:**
    *   In `script.js`, declare the following variables using `const`:
        *   A `name` variable holding your name (a string).
        *   An `age` variable holding your age (a number).
        *   An `isStudent` variable set to `true` (a boolean).
    *   Log each of these variables to the console to make sure they are correct.

4.  **Work with Data:**
    *   Create a new variable called `info` using `let`.
    *   Use a **template literal** to create a sentence that combines your name and age, and assign it to the `info` variable.
        *   Example: `` `My name is ${name} and I am ${age} years old.` ``
    *   Log the `info` variable to the console.

5.  **Perform Calculations:**
    *   Declare two more `const` variables: `favNum1` and `favNum2`, and assign them any number values.
    *   Create a new variable called `sum` and assign it the value of `favNum1 + favNum2`.
    *   Log the `sum` to the console.
    *   Create a new variable called `product` and assign it the value of `favNum1 * favNum2`.
    *   Log the `product` to the console.

6.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Add initial JavaScript file and practice variables`.

**Your final output in the browser console should show all the values you have logged.**