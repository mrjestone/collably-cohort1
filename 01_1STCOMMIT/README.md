# Task 1: Your First Local Commit

### **Objective**
By the end of this task, you will have created a local Git repository, added a file, and made your very first commit. You'll understand the basic workflow for saving your work like a professional developer.

### **Recap of Today's Lecture**
*   **Git** is our "save system" (version control).
*   The core workflow is moving files from the **Working Directory** -> **Staging Area** -> **Repository**.
*   We use commands like `git init`, `git status`, `git add`, and `git commit`.

---

### **Today's Task: Introduce Yourself**

Your mission is to create a new project on your computer, track it with Git, and add a file introducing yourself.

1.  **Create a Project Folder:** On your computer (e.g., on your Desktop or in your Documents), create a new folder named `collably-bootcamp`.
2.  **Open in VS Code:** Open this `collably-bootcamp` folder using Visual Studio Code.
3.  **Open the Terminal:** In VS Code, open the integrated terminal (`Ctrl + `` ` or `Cmd + `` `).
4.  **Initialize Git:** In your terminal, run the command `git init`. You should see a message saying "Initialized empty Git repository...".
5.  **Create Your File:** Create a new file inside the folder named `introduction.md`.
6.  **Write Your Intro:** In this new file, write a short paragraph about yourself. What are you excited to learn in this bootcamp?
7.  **Check the Status:** In the terminal, run `git status`. Notice how Git sees your new file and lists it as "untracked."
8.  **Stage Your File:** Run the command `git add introduction.md`. This moves your file to the staging area.
9.  **Commit Your File:** Now, save this snapshot permanently by running:
    ```bash
    git commit -m "feat: Add initial self-introduction"
    ```
    > **Pro Tip:** The `feat:` part is a convention many teams use to signify a new feature. It keeps commit history clean and readable.

10. **Verify Your Work:** Run `git log` in the terminal. You should see your commit listed, with your name, email, date, and commit message.

**You've just made your first commit! Congratulations!**

### **Stuck?**
If you encounter any errors, copy the error message and paste it into our `#help-requests` channel on Discord. I'm here to help!