# Purpose
This little test serves as a walkthrough to work with git. This document should include a Git cheat sheet, as well at the steps taken to create the test file, create a repository, and make edits, among other things. 


## Important commands
When initializing a brand new folder/project, you should run `git init` in the command prompt (this can be done in VScode without issues). You can check the status of git by running `git status`. Then `git remote add origin (https://)` should be run, where the `https://` link is the repository link after creating on Github. 

Once you are ready to commit your first change, you should use `git add` followed by the relevant file you would like to commit, and then run `git commit -m "insert message"` which commits your changes as well as a message to help identify it. You can also use `git add .` to add all files that have changes. This stages the changes in your local repository. The following `push` command publishes these changes to the remote reposity.

next, you can run `git push -u origin (branchname)` to actually commit your changes to the repo. The `-u` portion of this sets the upstream branch so future `push` and `pull` commands do not require branch information. Also, running this command while a branch does not yet exist will create a new branch. 

you can also create a new branch with `git branch (branch_name)`. to switch between old and new branches, you can use `git switch (branch name)`.

Now, to merge, users should use `git merge (branchname)` while in the desired branch they want to merge everything to (likely `main` or `master`). 

## VScode specific notes
some other things to note, particularly somem details with VScode. Once VScode is set up and linked with your github (which I'll go into at a later time), it does become quite easy to visualize where exactly your specific branch/version/everything is in relation to everything else, particularly with the graph the pops up in the bottom left of the "Source control" window. It will show you the message history, as well as show you every change that was made for each commit. 


## Cheatsheet
| Command | Purpose |
---|---
git init | Initialize a new Git repository
git status | Show branch, staged/untracked files
git add <file> | Stage a file
git add . | Stage all changes
git commit -m "message" | Commit staged changes
git log --oneline --graph --all | Show commit history visually
git remote add origin <url> | Add a remote repository
git push -u origin <branch> | Push branch to remote and track
git branch <name> | Create a new branch
git switch <name> | Switch branches
git merge <branch> | Merge another branch into current branch
git branch -d <branch> | Delete a local branch
git push origin --delete <branch> | Delete a remote branch


# Git Important Definitions

This table lists important Git terms from the very basics to more advanced concepts, with clear definitions to help learners understand how Git works.

| Term | Definition |
|------|------------|
| Repository (repo) | A folder that contains your project’s files and all of Git’s version history. Can be local (on your machine) or remote (on GitHub, GitLab, etc.). |
| Commit | A snapshot of your repository at a given point in time. Each commit has a unique ID (hash) and a message describing the change. |
| Staging / Staged | The process of selecting changes to include in the next commit. Files must be staged (`git add`) before committing. |
| Unstaged / Working Directory | Files that have been changed but not yet staged for commit. |
| Tracked | Files Git is already monitoring for changes (i.e., they’ve been committed at least once). |
| Untracked | Files Git is not yet monitoring. They won’t be included in commits until added (`git add`). |
| Branch | A pointer to a series of commits. Used to develop features independently from the main project. Default branch is often `main` or `master`. |
| Main / Master Branch | The default branch in a repository, usually representing the stable production-ready code. |
| Feature Branch | A separate branch created to develop a specific feature without affecting the main branch. |
| Merge | Combining changes from one branch into another. Can result in fast-forward, merge commits, or conflicts. |
| Merge Conflict | Occurs when Git cannot automatically reconcile differences between branches. Requires manual resolution. |
| Remote | A version of your repository hosted on another server (like GitHub) that you can fetch from or push to. |
| Origin | Default name Git gives to the remote repository you cloned or added. |
| Push | Upload local commits to a remote repository. |
| Pull | Fetch changes from a remote repository and merge them into your local branch. |
| Clone | Create a local copy of a remote repository. |
| Checkout / Switch | Command to move between branches or restore files to a previous state. (`git switch <branch>` is the modern form) |
| Upstream / Tracking Branch | A remote branch that a local branch is linked to, so `git push` or `git pull` works without specifying the remote and branch. |
| HEAD | Pointer to the current commit on your current branch. Represents “where you are” in the repo. |
| Tag | A named pointer to a specific commit, usually used for marking releases or versions. |
| Diff | A comparison of changes between commits, branches, or the working directory and staging area. Shows what was added or removed. |
| Reset | Undo changes in your working directory or staging area. (`soft`, `mixed`, `hard`) |
| Revert | Create a new commit that undoes changes from a previous commit. Safe for shared repos. |
| Stash | Temporarily save changes that are not ready to commit, so you can switch branches without committing. |
| Fork | A personal copy of someone else’s repository, usually on GitHub, allowing you to propose changes without affecting the original repo. |
