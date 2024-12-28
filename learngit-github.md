### **1. Forking a Repository (On GitHub)**

- **What is Forking?**
    
    Forking creates a personal copy of someone else's repository, allowing you to freely make changes without affecting the original project.
    
- **How to Fork:**
    1. Visit the GitHub repository you want to fork.
    2. Click the **"Fork"** button in the upper-right corner of the page.
    3. GitHub will create a copy of the repository under your GitHub account.
    
    ![image.png](./Screenshot%20from%202024-12-28%2007-56-59.png)
    

### **2. Cloning a Repository Locally**

- **What is Cloning?**
    
    Cloning copies the entire repository (your fork) to your local machine so you can start working on it.
    
- **How to Clone:**
    1. On your GitHub account, navigate to the forked repository.
    2. Click the green **"Code"** button, then copy the URL (either HTTPS or SSH).
    3. Open your terminal and run the following command to clone the repo to your local machine:
    
    ```bash
    git clone <repository-url>
    ```
    

### **3. Creating a Branch for Your Changes**

```bash
git checkout -b <new-branch-name>
```

### **4. Make Changes and Commit Them**

- **What is a Commit?**
    
    A commit is a snapshot of your changes, saved in the repository’s history.
    
- **How to Commit Changes:**
    1. Stage the changes by adding modified files (or all files) to the staging area:
    2. Commit your staged changes with a meaningful message:

```bash
git add <file-name>    # For a specific file
git add .              # For all changes
```

```bash
git commit -m "Describe your changes here"
```

### **5. Push Your Changes to GitHub**

- **What is Pushing?**
    
    Pushing sends your committed changes from your local branch to your GitHub repository (your fork).
    
- **How to Push:**
    1. Push the changes from your local branch to your GitHub repository:
    
    ```bash
    git push origin <branch-name>
    ```
    

### **6. Create a Pull Request (PR)**

- **What is a Pull Request?**
    
    A pull request (PR) allows you to propose changes to the original repository. This is where project maintainers review and discuss your changes before merging them into the main codebase.
    
- **How to Create a PR:**
    1. Go to your forked repository on GitHub.
    2. Click the **"New Pull Request"** button.
    3. Select the branch you just pushed (e.g., `feature/add-login-page`).
    4. Choose the original repository’s main branch (usually `main` or `master`) as the base branch.
    5. Provide a clear title and description of your changes.
    6. Click **"Create Pull Request"** to submit.