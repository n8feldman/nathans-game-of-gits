KEY TERMS TO KNOW:

Working directory: Where we're editing the files we work on.
Staging area: Where we stage files that we fix to commit them. (command: git add).
.git directory (Repository): This is where committed changes go. We can then checkout the project again into the working directory. (command: git commit -m "message").
Branch: If we want to make changes to a particular part of the project, we make a branch which has its own set of files, commits, and changes. We later merge these changes into the master branch, which has the full codebase. This protects the master branch in case we have issues.

Initialize a repository:
git init

Check status of repository (can do this anytime, actually do it constantly tbh, like every time we do a git command):
git status

Note: Results from git status show which files are being tracked/are not being tracked for changes. It will also show which files have changes which have not been staged and which files have their final versions added to the staging area.

Stage files we've changed to be committed:
git add {filename}

"Save" a version of all current files that have been staged in our working branch (and leave a message). We can recover this batch of files in their current saved state later by going into our commit history. No change is too small to commit. Commit early, and commit often.
git commit -m "message"

"Un-stage" a file we staged too early:
git reset {filename}

Remove a file from git tracking because we removed it in our system:
git rm {filename}

Create a git branch:
git branch {branchname}

Checkout a git branch (use "master" for master):
git checkout {branchname}

See differences between two branches:
git diff {branch1} {branch2}

USING BRANCHES: Say we're on branch "dreamstory" and want to make changes to the code for the master branch.
Step 1: Edit the file.
Step 2: git add {file}
step 3: git commit -m "message"
Step 4: git checkout master
step 5: git merge dreamstory master

PUSHING LOCAL REPO TO REMOTE:
Step 1: Go to github.com
Step 2: Click "New Repository"