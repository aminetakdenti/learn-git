## 1. `git init`
**What it does:**  
Initializes a new Git repository in your current directory. It creates a `.git` directory to track changes.

**Command:**
```bash
git init
```

## 2. git add

**What it does:**  
Stages changes in your working directory to be committed. It’s the first step to preparing your changes for commit.

**Command:**
```bash
git add <file-name>   # Stage specific file
git add .             # Stage all changes in the current directory
```

## 3. git commit

What it does:
Commits the staged changes to the local repository with a message describing the changes.

**Command:**
```
git commit -m "Commit message describing the changes"
```

## 4. git status

What it does:
Shows the current status of the working directory and staging area. It indicates which files have been modified, staged, or committed.

**Command:**
```
git status
```

## 5. git log

What it does:
Displays the commit history, showing all commits made in the current branch, starting from the latest one.

**Command:**
```
git log
```
Options:  
    
`git log --oneline` - Shows a concise version of the commit history.   
`git log --graph --oneline` - Displays a graphical representation of the commit history.  

## 6. git branch

What it does:
Shows a list of branches in your repository. The current branch will be highlighted.

**Command:**
```
git branch
```

## 7. git checkout

What it does:
Switches to another branch or commit. This command is used to navigate between branches or to check out a specific commit.

**Command:**
```
git checkout <branch-name>   # Switch to an existing branch
git checkout -b <new-branch-name>   # Create and switch to a new branch
```

## 8. git merge

What it does:
Merges the changes from one branch into another. It is used to combine the history of two branches.

**Command:**
```
git merge <branch-name>
```

## 9. git remote add

What it does:
Links your local repository to a remote repository, enabling you to push and pull changes from a remote location (e.g., GitHub).

**Command:**
```
git remote add origin <remote-repository-URL>
```

## 10. git push

What it does:
Pushes your local commits to a remote repository, making them available to others.

**Command:**
```
git push origin <branch-name>
```

## 11. git pull

What it does:
Fetches changes from a remote repository and merges them into your local repository. It’s a combination of git fetch and git merge.

**Command:**
```
git pull origin <branch-name>
```