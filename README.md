# Purpose
This little test serves as a walkthrough to work with git. This document should include a Git cheat sheet, as well at the steps taken to create the test file, create a repository, and make edits, among other things. 

## Important commands
When initializing a brand new folder/project, you should run `git init` in the command prompt (this can be done in VScode without issues). You can check the status of git by running `git status`. Then `git remode add origin (https://)` should be run, where the `hppts://` link is the repository link after creating on Github. 

Once you are ready to commit your first change, you should use `git add` followed by the relevant file you would like to commit, and then run `git commit -m "insert message"` which commits your changes as well as a message to help identify it. You can also use `git add .` to add all files that have changes. This creates a local version of verious branches it seems, and the following `push` command actually publishes it

next, you can run `git push -u origin (branchname)` to actually commit your changes to the repo.

you can also create a new branch with `git branch (branch_name)`. to switch between old and new branches, you can use `git switch (branch name)`.

Now, to merge, users should use `git merge (branchname)` while in the desired branch they want to merge everything to (likely `main` or `master`). 

## VScode specific notes
some other things to note, particularly somem details with VScode. Once VScode is set up and linked with your github (which I'll go into at a later time), it does become quite easy to visualize where exactly your specific branch/version/everything is in relation to everything else, particularly with the graph the pops up in the bottom left of the "Source control" window. It will show you the message history, as well as show you every change that was made for each commit. 