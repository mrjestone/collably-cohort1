# Topic: JavaScript Fundamentals 2 - Collections & Logic

### **Objective**
To store and access collections of data using Arrays and Objects, create reusable code blocks with Functions, and control program flow with `if/else` statements.

### **Recap of The task**
*   **Arrays `[]`** are for ordered lists of items, accessed by a numerical index (starting at 0).
*   **Objects `{}`** are for unordered collections of labeled data (key-value pairs), accessed by the key name (e.g., `user.name`).
*   **Functions `()`** are reusable blocks of code. We define them once and can call them many times. They can take in data (parameters) and can give back a result (`return`).
*   **`if/else` statements** let our code make decisions based on `true` or `false` conditions.

---

### **Task: Build a Mini "User Profile" System**

You will use arrays, objects, and functions to model a simple user profile and create logic to check their status.

1.  **Create Your User Object:**
    *   In your `script.js` file, create a `const` variable named `userProfile`.
    *   Assign it an **object** with the following properties (key-value pairs):
        *   `username`: Your name (string).
        *   `age`: Your age (number).
        *   `isLoggedIn`: A boolean set to `true`.
        *   `skills`: An **array** containing at least three strings of skills you want to learn (e.g., `"HTML"`, `"CSS"`, `"JavaScript"`).

2.  **Access and Log Data:**
    *   Using `console.log()` and dot notation, print the user's `username` to the console.
    *   Using `console.log()` and array index notation, print the *second* skill from the `skills` array to the console.

3.  **Create a "Welcome" Function:**
    *   Define a new function called `displayWelcomeMessage`.
    *   This function should accept one **parameter**: `user`.
    *   Inside the function, create a welcome message using a template literal that includes the user's username.
    *   Call the function, passing your `userProfile` object as the argument.

4.  **Create a "Status Check" Function:**
    *   Define a new function called `checkLoginStatus`.
    *   This function should accept one parameter: `profile`.
    *   Inside the function, use an **`if/else` statement**:
        *   **If** `profile.isLoggedIn` is `true`, the function should `return` the string "User is currently logged in."
        *   **Else**, it should `return` the string "User is not logged in."
    *   Call this function, passing in your `userProfile` object. Store the returned value in a new variable called `statusMessage`.
    *   Log `statusMessage` to the console.

5.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Practice with JS objects, arrays, and functions`.

**When you run your code, your console should display the username, the second skill, the welcome message, and the login status message.**

6.  **Share your work on discord as always**
    