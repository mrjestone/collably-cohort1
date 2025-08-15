# Topic: React Fundamentals 1 - Thinking in Components

### **Objective**
To understand the core philosophy of React, create your first functional component using JSX, and manage component memory with the `useState` hook.

### **Recap of Today's Lecture**
*   React is a **declarative** library: we describe the UI we want, and React builds it for us.
*   We build UIs by composing **Components**—reusable JavaScript functions that return HTML-like code.
*   **JSX** allows us to write HTML syntax directly in our JavaScript. Component names must be capitalized.
*   The **`useState` hook** is how we give our components "state" or memory. When we update the state, React automatically re-renders the component to reflect the change.

---

### **Today's Task: Build a Simple Counter Component**

You will set up your first React project and build a classic counter application to practice the fundamentals of components and state.

#### **Part 1: Setting up Your First React Project**

We will use a tool called **Vite** to quickly create a modern React project.

1.  **Navigate to Your Root Folder:** In your terminal, make sure you are in your main `collably-bootcamp` folder (not inside the `portfolio-project`).
2.  **Create the Vite Project:** Run the following command. This will guide you through a setup process.
    ```bash
    npm create vite@latest
    ```
    *   When it asks for a **Project name**, type `react-counter-app`.
    *   When it asks to **Select a framework**, use the arrow keys to choose **React**.
    *   When it asks to **Select a variant**, choose **JavaScript**.
3.  **Install Dependencies:** Follow the on-screen instructions.
    ```bash
    cd react-counter-app
    npm install
    ```
4.  **Explore the Code:** Open the new `react-counter-app` folder in VS Code. Look at the `src` folder. You'll see an `App.jsx` file. This is your main application component!
5.  **Start the Development Server:** Run the final command to see your app live.
    ```bash
    npm run dev
    ```
    Open the URL it gives you in your browser (usually `http://localhost:5173`). You should see the default Vite + React starter page.

#### **Part 2: Building the Counter**

1.  **Clean Up `App.jsx`:** Open `src/App.jsx`. Delete everything inside the `return` statement and replace it with a simple `<h1>Hello, React!</h1>`. Delete the `useState` import and the state variable for now. Your file should look very simple.

2.  **Create the Counter Component:**
    *   Inside the `App` function, before the `return` statement, import `useState` from React: `import { useState } from 'react';`
    *   Set up your state variable: `const [count, setCount] = useState(0);`
    *   Create two arrow functions:
        *   `handleIncrement`: calls `setCount(count + 1);`
        *   `handleDecrement`: calls `setCount(count - 1);`

3.  **Render the JSX:**
    *   Modify the JSX inside the `return` statement of your `App` component to build the UI for the counter.
        ```jsx
        function App() {
          const [count, setCount] = useState(0);

          const handleIncrement = () => {
            setCount(count + 1);
          };

          const handleDecrement = () => {
            setCount(count - 1);
          };

          return (
            <div style={{ textAlign: 'center', marginTop: '50px' }}>
              <h1>React Counter</h1>
              <p style={{ fontSize: '48px' }}>{count}</p>
              <div>
                <button onClick={handleDecrement} style={{ marginRight: '10px' }}>Decrement</button>
                <button onClick={handleIncrement}>Increment</button>
              </div>
            </div>
          );
        }

        export default App;
        ```
    *   Notice how we use `onClick` to attach our functions to the button clicks.

4.  **Test and Verify:** Your browser should have automatically updated. You now have a working counter! Clicking the buttons should change the number on the screen.

5.  **Commit and Push:**
    *   In your terminal, stop the dev server (`Ctrl + C`).
    *   Navigate back to the root `collably-bootcamp` folder.
    *   Create a `.gitignore` file inside `react-counter-app` if it doesn't exist, and make sure it contains `node_modules` and `dist`.
    *   Stage, commit, and push your new `react-counter-app` project.
    *   Use the commit message: `feat: Create first React app with a stateful counter`.
```