# Git Commands Cheatsheet

## Identity Setup
```bash
git config --global user.name "Manohar Paruchuru"
git config --global user.email "your.email@example.com"

Sets your identity for commits across all repositories.

Basic Operations

git init
git diff
git add <file-name>
git restore <file-name>
git commit -m "message"
git show HEAD:<filename>
git reset --hard <commitID>
git log
git log --oneline

- git init → Initializes repo
- git diff → Shows changes
- git add → Stages changes
- git restore → Discards changes
- git commit → Saves changes
- git show HEAD:<filename> → Shows file from last commit
- git reset --hard <commitID> → Resets branch to commit
- git log → Full commit history
- git log --oneline → Compact commit history



