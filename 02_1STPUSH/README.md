# Task 2: Pushing to GitHub

### **Objective**
In this task, you will connect your local Git repository to a remote repository on GitHub. You will push your work to the cloud, making it accessible from anywhere and starting the foundation of your professional portfolio.

### **Recap of Today's Lecture**
*   **GitHub** is the website where we store our code.
*   A **remote** (usually named `origin`) is the link between your local computer and GitHub.
*   The command `git push` sends your local commits to your remote repository.

---

### **Task: Put Your Work Online**

You will take the project you created yesterday and upload its history to a new GitHub repository.

1.  **Create a GitHub Repository:**
    *   Go to [GitHub.com](https://github.com).
    *   Click the "+" in the top-right corner and select "New repository."
    *   Name your repository `collably-bootcamp`.
    *   Make sure it's set to **Public**.
    *   **DO NOT** initialize it with a README, .gitignore, or license. We want an empty repository.
    *   Click "Create repository."

2.  **Connect Your Local Project:**
    *   On the new repository page, GitHub will show you a URL. Copy the HTTPS URL.
    *   Go back to your `collably-bootcamp` folder in your VS Code terminal (the same one from previous task).
    *   Run the following command, replacing `<URL>` with the one you just copied:
        ```bash
        git remote add origin <URL>
        ```

3.  **Push Your Code:**
    *   Now, send your local commit history to GitHub by running:
        ```bash
        git push -u origin main
        ```
    *   You may be prompted to log in to GitHub.

4.  **Verify Your Work:**
    *   Refresh your GitHub repository page in your browser.
    *   You should now see your `introduction.md` file! You've successfully pushed your code.

### **Bonus Task: The Magic of README.md**

1.  In your **local** VS Code, create a new file named `README.md`.
2.  In this file, write a short description of the project. For example: "This repository contains my daily tasks and projects for the Collably Bootcamp."
3.  Stage, commit, and push this new file:
    ```bash
    git add README.md
    git commit -m "docs: Add README file"
    git push
    ```
    *(Notice you don't need to type `git push -u origin main` this time!)*
4.  Refresh your GitHub page again. See how the `README.md` content is automatically displayed on the repository's home page. This is a standard practice for all professional projects.