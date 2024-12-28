### 1. git reset

What it does:
git reset allows you to undo changes in your working directory or reset your repository to a previous commit. It’s a simple command with different options for how much you want to reset.

Example: To reset your branch to a specific commit:

```
git reset --hard <commit-hash>
```

Options:

`--soft` keeps changes staged.

`--mixed` keeps changes in the working directory but unstaged.

`--hard` discards changes completely.

Example of --mixed reset:

```
git reset --mixed abc1234
```

### 2. git stash

What it does:
git stash temporarily saves changes that are not ready to be committed. This allows you to switch branches or work on something else without losing your progress.

Example: Save changes temporarily:

```
git stash
```

View stashed changes:

```
git stash list
```

Apply the most recent stash:
```
git stash apply
```

Apply a specific stash:
```
git stash apply stash@{1}
```

Drop the stash after applying:
```
git stash drop stash@{1}
```

### 3. git reflog

What it does:
git reflog keeps track of all changes to your branches and HEAD. It’s useful for recovering lost commits or navigating through the history of your repository, especially when you need to find a commit that was recently discarded.

Example: Display all recent actions in your repository:

```
git reflog
```

Output:
```
abc1234 HEAD@{0}: commit: Added new feature

def5678 HEAD@{1}: commit: Fixed a bug

ghi9012 HEAD@{2}: reset: moved to previous commit
```

Checkout a previous commit from the reflog:
```
git checkout HEAD@{2}
```

### 4. git cherry-pick

What it does:
git cherry-pick applies a specific commit from one branch to another, which is helpful when you want to bring in specific changes without merging entire branches.

Example: Apply a specific commit from another branch:
```
git cherry-pick <commit-hash>
```

Example:
```
git cherry-pick abc1234
```
This will apply the commit abc1234 to the current branch. If there are conflicts, Git will ask you to resolve them before continuing.

### 5. git rebase

What it does:
git rebase is used to apply changes from one branch onto another. It’s commonly used to integrate upstream changes or keep a feature branch updated with the latest changes from the main branch. Rebase rewrites commit history and can cause conflicts that need resolution.

Example: To rebase a feature branch onto main:
```
git checkout feature-branch
git rebase main
```

If there are conflicts, Git will stop, and you can resolve the conflicts before continuing:

```
git rebase --continue
```

To cancel the rebase and return to the original state:
```
git rebase --abort
```

### 6. git squash

What it does:
Git squash is a technique used during an interactive rebase to combine multiple commits into a single one. This is particularly useful for cleaning up commit history before merging a feature branch.

Example:

Start an interactive rebase to combine commits:

```
git rebase -i HEAD~3
```

In the editor that opens, change pick to squash (or s) for the commits you want to combine.

Example:
```
pick abc1234 Commit 1
squash def5678 Commit 2
squash ghi9012 Commit 3
```

After saving and closing the editor, Git will combine the selected commits into one and let you edit the commit message.

### Summary of Commands (from Easy to Hard):

* `git reset` - Undo changes and reset your branch to a previous state.
* `git stash` - Temporarily save changes to apply later.
* `git reflog` - View the history of all actions in the repository.
* `git cherry-pick` - Apply a specific commit from another branch.
* `git rebase` - Reapply commits from one branch onto another.
* `git squash` - Combine multiple commits into one using interactive rebase.