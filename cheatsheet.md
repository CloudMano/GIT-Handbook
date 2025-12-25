**# Git Commands Cheatsheet**

**## Identity Setup**
```bash
git config --global user.name "Manohar Paruchuru"
git config --global user.email "your.email@example.com"
```
Sets your identity for commits across all repositories.

**## Repository and Commit Operations**
```bash
git init
git diff
git add <file-name>
git restore <file-name>
git commit -m "message"
git show HEAD:<filename>
git reset --hard <commitID>
git log
git log --oneline
```
git init → Initializes a new local Git repository in the current folder, creating a `.git` directory to track all version control operations.  
git diff → Displays changes in files that are not yet staged (before being added to the index).  
git add <file-name> → Adds the specified file’s changes to the staging area (index), preparing them for the next commit (the index is a snapshot of your files as they are about to be committed).  
git restore <file-name> → Discards changes in the working directory and restores the file to its last committed state (can be used before committing or after adding changes to the index).  
git commit -m "message" → Saves the staged snapshot to the project history as a new commit with a descriptive message.  
git show HEAD:<filename> → Shows the content of the specified file as it existed in the latest commit (HEAD points to the latest commit).  
git reset --hard <commitID> → Moves the current branch and working directory to the specified commit, permanently removing all later commits and local changes.  
git log → Displays a detailed list of previous commits on the branch.  
git log --oneline → Shows a concise, single-line summary for each commit in the branch history.  

**## Branch Operations**
```bash
git branch
git branch branchname
git checkout -b "branchname"
git checkout branchname
git switch branchname
git switch -c branchname
git branch -d "branchname"
git branch -D "branchname"
```
git branch → Lists all available branches within the index  
git branch branchname → Creates a new branch in the index  
git checkout -b "branchname" → Creates a new branch and switches to the newly created branch immediately  
git checkout branchname → Used to switch between branches  
git switch branchname → Works similar to git checkout branchname  
git switch -c branchname → Works similar to git checkout -b branchname  
git branch -d "branchname" → Deletes the specified branch if merges are done properly  
git branch -D "branchname" → Deletes the branch forcefully even if merges are not done properly  

**## Merging and Integrating Changes**
```bash
git cherry-pick <commit>
git merge <branch>
git rebase <branch>
```
git cherry-pick <commit> → Applies the changes from a specific commit (from any branch) onto your current branch, creating a new commit.  
git merge <branch> → Integrates changes from the specified branch into your current branch by creating a new merge commit.  
git rebase <branch> → Replays your current branch’s commits on top of the target branch, rewriting history to produce a linear sequence of commits.  

**## Remote Repository Management**
```bash
git remote add origin <remote-repository-URL>
git clone <remote-repository-URL>
git remote -v
git remote remove origin
git push --set-upstream origin master
git push
git pull
git fetch origin
git log HEAD..origin/master
```
git remote add origin <remote-repository-URL> → Sets the remote repository named "origin" without cloning any files or folders.  
git clone <remote-repository-URL> → Clones an entire remote Git repository into a local directory.  
git remote -v → Lists remote repositories connected to your local repo and their URLs.  
git remote remove origin → Removes the remote connection named "origin" from your local repository.  
git push --set-upstream origin master → Links your current local branch (e.g., master) to a remote branch and pushes code for the first time.  
git push → Pushes local commits to the connected remote repository.  
git pull → Fetches changes from the remote repository and merges them into your local branch.  
git fetch origin → Downloads changes from the specified remote but does not integrate them or modify your working directory.  
git log HEAD..origin/master → Displays commits in the remote branch (origin/master) that are not in your current branch (after a fetch).  

**## SSH Authentication for GitHub**
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
cat ~/.ssh/id_rsa.pub
git clone <ssh-remote-repository-URL>
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com" → Generates a new SSH key pair for authentication with GitHub.  
cat ~/.ssh/id_rsa.pub → Displays the public SSH key, which you can add to your GitHub account for SSH-based authentication.  
git clone <ssh-remote-repository-URL> → Clones a repository using SSH instead of HTTPS.  