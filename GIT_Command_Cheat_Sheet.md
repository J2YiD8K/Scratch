# Git Command Cheat Sheet

This cheat sheet provides a quick reference to commonly used Git commands.

## Basic Commands

- `git init`  
  Initialize a new Git repository.

- `git clone <repository-url>`  
  Clone an existing repository.

- `git status`  
  Show the working directory status.

- `git add <file>`  
  Add a file to the staging area.

- `git commit -m "message"`  
  Commit changes with a message.

- `git push`  
  Push changes to the remote repository.

- `git pull`  
  Fetch and merge changes from the remote repository.

- `git fetch`  
  Download objects and refs from another repository.

## Branching

- `git branch`  
  List all branches.

- `git branch <branch-name>`  
  Create a new branch.

- `git checkout <branch-name>`  
  Switch to a branch.

- `git merge <branch-name>`  
  Merge a branch into the current branch.

## Remote Management

- `git remote -v`  
  Show remote URLs.

- `git remote add <name> <url>`  
  Add a new remote.

- `git remote remove <name>`  
  Remove a remote.

## Prune Commands

- `git remote prune origin`  
  Remove stale remote-tracking branches that no longer exist on the remote.

- `git fetch --prune`  
  Prune remote-tracking branches during fetch.

- `git gc --prune=now`  
  Prune unreachable objects from the local repository immediately.

- `git reflog expire --expire=now --all`  
  Expire all reflog entries immediately.

## Stashing

- `git stash`  
  Stash changes in a dirty working directory.

- `git stash apply`  
  Reapply stashed changes.

- `git stash pop`  
  Apply and remove the latest stash.

## Logs and History

- `git log`  
  Show commit logs.

- `git log --oneline`  
  Show commit logs in one line per commit.

- `git diff`  
  Show changes between commits, commit and working tree, etc.

## Undoing Changes

- `git reset <file>`  
  Unstage a file.

- `git checkout -- <file>`  
  Discard changes in the working directory.

- `git revert <commit>`  
  Create a new commit that undoes the changes from a previous commit.

## Tags

- `git tag`  
  List all tags.

- `git tag <tag-name>`  
  Create a new tag.

- `git push origin <tag-name>`  
  Push a tag to the remote repository.

## Configuration

- `git config --global user.name "Your Name"`  
  Set the global username.

- `git config --global user.email "you@example.com"`  
  Set the global email.

