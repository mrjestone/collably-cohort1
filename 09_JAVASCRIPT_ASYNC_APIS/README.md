# Topic: Asynchronous JavaScript and Fetching API Data

### **Objective**
To understand the basics of asynchronous programming and use the `fetch` API with `async/await` syntax to retrieve data from a live, external API.

### **Recap of Today's Lecture**
*   **Asynchronous (Async) JavaScript** prevents the browser from freezing during long tasks like network requests.
*   An **API** is a service that provides data in a structured format, usually **JSON**.
*   We use the `fetch()` function to request data from an API endpoint (a URL).
*   The modern syntax for handling this is **`async/await`**, which lets us write async code that looks clean and readable.
*   We use a **`try...catch`** block to handle potential errors during the request.

---

### **Today's Task: Build a "Random User" Generator**

You will fetch data from a free public API called "[Random User Generator](https://randomuser.me/)" and use it to display a profile card on your portfolio page.

#### **Part 1: Preparing the HTML**

1.  **Add a "Project" Section:** In your `portfolio-project/index.html`, find the `<section>` you created for "My Projects".
2.  **Create a Placeholder:** Inside this section, add the following HTML. This is where our user data will be displayed. Give the main container a unique ID so we can easily select it.
    ```html
    <!-- Inside your "My Projects" section -->
    <h3 class="text-2xl font-bold mb-4">Random User Project</h3>
    <div id="user-card" class="bg-slate-200 p-4 rounded-lg text-center">
        <p>Loading user data...</p>
    </div>
    <button id="fetch-user-button" class="mt-4 bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600">
      Get New User
    </button>
    ```

#### **Part 2: The JavaScript Logic**

In your `portfolio-project/script.js` file, add the following logic:

1.  **Select Elements:**
    *   At the top of your script, select the `#user-card` div and the `#fetch-user-button` button and store them in `const` variables.

2.  **Define Your `fetchUser` Function:**
    *   Create a new **`async`** function called `fetchUser`.
    *   **Inside a `try` block:**
        *   Use `await fetch('https://randomuser.me/api/')`. Store the result in a variable called `response`.
        *   Use `await response.json()`. Store the result in a variable called `data`.
        *   `console.log(data)` to inspect the structure of the data you get back. You'll see the user info is inside `data.results[0]`.
        *   Call a new function (that you will create next) called `displayUser`, and pass `data.results[0]` to it.
    *   **Inside a `catch` block:**
        *   Log an error message to the console (e.g., `console.error("Failed to fetch user:", error);`).

3.  **Define Your `displayUser` Function:**
    *   Create a new regular function called `displayUser` that accepts one parameter, `user`.
    *   Select your `#user-card` div from Part 1.
    *   Use template literals to create an HTML string with the user's information.
        ```javascript
        const userHTML = `
            <img src="${user.picture.large}" alt="User photo" class="rounded-full mx-auto border-4 border-white">
            <h2 class="text-xl font-bold mt-2">${user.name.first} ${user.name.last}</h2>
            <p class="text-slate-600">${user.email}</p>
            <p class="text-slate-500">Location: ${user.location.city}, ${user.location.country}</p>
        `;
        ```
    *   Set the `.innerHTML` of the user card div to this new `userHTML` string.

4.  **Attach the Event Listener and Initial Load:**
    *   Add an event listener to your "Get New User" button that calls the `fetchUser` function when clicked.
    *   To load a user immediately when the page loads, call `fetchUser()` one time at the bottom of your script file.

5.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Implement random user generator via API call`.

**Now, when you open your page, it should immediately fetch and display a random user. Clicking the button should fetch and display a new one.**