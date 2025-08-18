# Topic: React Fundamentals 2 - Passing Data with Props

### **Objective**
To understand how to pass data from parent components to child components using `props` and to refactor a complex component into smaller, reusable pieces.

### **Recap of Today's Lecture**
*   **Props** (properties) are used to pass data down from a parent to a child component.
*   Data is passed as attributes in JSX (`<MyComponent myProp="some value" />`).
*   The child component receives this data in a `props` object.
*   **Destructuring** props (`const MyComponent = ({ myProp }) => ...`) is the modern, preferred syntax.
*   React has a **one-way data flow**: data flows down, and props are read-only for the child.

---

### **Today's Task: Refactor and Create Reusable Profile Cards**

You will refactor your `react-counter-app` into a more structured application. You will create a reusable `UserProfile` card component and use props to display data for several different users.

#### **Part 1: Setting up the Project**

1.  **Start with a Clean Slate:**
    *   Open your `react-counter-app` project.
    *   In `src/App.jsx`, remove the counter logic. Let's start with a fresh `App` component that just returns a `<div>`.
        ```jsx
        function App() {
          return (
            <div>
              <h1>User Profiles</h1>
            </div>
          );
        }
        export default App;
        ```

2.  **Prepare the User Data:**
    *   Inside your `App` component (before the `return` statement), create an array of user objects. This will be the "database" for our application.
        ```javascript
        const users = [
          { id: 1, name: 'Bona S', job: 'Lead Developer', avatar: 'https://i.pravatar.cc/150?img=1' },
          { id: 2, name: 'Alice Smith', job: 'UI/UX Designer', avatar: 'https://i.pravatar.cc/150?img=2' },
          { id: 3, name: 'Charlie Brown', job: 'Project Manager', avatar: 'https://i.pravatar.cc/150?img=3' }
        ];
        ```

#### **Part 2: Creating the Reusable Component**

1.  **Create a New Component File:**
    *   In the `src` folder, create a new file named `UserProfile.jsx`.
2.  **Build the `UserProfile` Component:**
    *   In `UserProfile.jsx`, create a new functional component.
    *   This component will receive `user` data via props. Use **destructuring** to get the data you need.
    *   The component should return JSX that displays the user's information in a "card" format.
        ```jsx
        // src/UserProfile.jsx

        const UserProfile = ({ name, job, avatar }) => {
          const cardStyle = {
            border: '1px solid #ccc',
            borderRadius: '8px',
            padding: '20px',
            margin: '10px',
            width: '200px',
            textAlign: 'center',
            boxShadow: '0 2px 4px rgba(0,0,0,0.1)',
          };

          return (
            <div style={cardStyle}>
              <img src={avatar} alt={`Avatar for ${name}`} style={{ width: '100px', height: '100px', borderRadius: '50%' }} />
              <h2 style={{ marginTop: '10px' }}>{name}</h2>
              <p style={{ color: '#555' }}>{job}</p>
            </div>
          );
        };

        export default UserProfile;
        ```

#### **Part 3: Using the Component in the App**

1.  **Import the New Component:**
    *   Back in `src/App.jsx`, import your new component at the top of the file: `import UserProfile from './UserProfile';`
2.  **Map Over the Data and Render Components:**
    *   In the `return` statement of `App.jsx`, we want to render one `UserProfile` card for each user in our `users` array. The `.map()` method is perfect for this.
    *   Add a container `div` to help with styling.
    *   Modify your `App.jsx` return statement:
        ```jsx
        // Inside App.jsx's return statement
        return (
          <div>
            <h1 style={{ textAlign: 'center' }}>User Profiles</h1>
            <div style={{ display: 'flex', justifyContent: 'center', flexWrap: 'wrap' }}>
              {users.map(user => (
                <UserProfile
                  key={user.id} // 'key' is a special prop React needs for lists
                  name={user.name}
                  job={user.job}
                  avatar={user.avatar}
                />
              ))}
            </div>
          </div>
        );
        ```
    > **Note:** The `key` prop is essential. It helps React efficiently update the list if items are added, removed, or reordered. It must be a unique value for each item in the list, which is why we use `user.id`.

3.  **Test and Verify:** Your browser should now display three distinct user profile cards, all rendered by your single, reusable `UserProfile` component.

4.  **Commit and Push:**
    *   Stage, commit, and push your changes.
    *   Use the commit message: `feat: Create reusable UserProfile component and render data with props`.