# Git Demo

## What is Git?

* Distributed version control
* History of all changes
* Collaboration with other developers
* Code backup

## Distributed means that the entire VCS lives on your local computer.

* All history, repositories and branches live on your computer.
* Every transaction happens first on your local repository.
    * How do I share changes?
    * How do I get changes from other developers?

## What is a Repository?

## What is a Remote?

## Remember: There is not just one right way to use git, but there are wrong ways.

## Basic Git Commands

```shell
# Initialize a brand new Git repository
git init

# Create a local copy from a remote repository
git clone https://github.com/ryan-w/git-demo.git .

# Show the current status of the repo
# Files: untracked, modified, or staged
# Status with remote
git status

# Add changes to the staging area (pre-commit)
git add . # Add all pending changes and untracked (recursively)
git add somefile.txt # Add a single file

# Commit the staged changes to history
git commit -m "Updated the so and so file"

# List commits/show history
git log
git log -5 --oneline

# Send local commits to the remote repository
git push

# Merge commits from remote repository into local repository
# Same as running 'git fetch' and 'git merge'
git pull

# Show detail of changes between commits of working directory
git diff
```

## What are Branches?

<img src="https://wac-cdn.atlassian.com/dam/jcr:746be214-eb99-462c-9319-04a4d2eeebfa/01.svg?cdnVersion=kc" alt="Branching" width="600"/>

```shell
# List branches in your local repository
git branch --list

# Create a new branch called 'my-branch' from the current branch
git branch my-branch

# Set the working directory to the 'my-branch' branch
git checkout my-branch

# Merge commits from 'my-branch' into 'master'
git checkout master
git merge my-branch
```

## Other Useful Commands

```shell
# Unstaging a staged file
git reset HEAD <file>

# Undo changes to a file
git checkout -- <file>

# WARNING: This will delete any changes in your working directory.
git reset HEAD --hard

# Make changes to your last commit.
# WARNING: Don't use this command if you have already pushed your commit.
git commit --amend

# Temporarily stash away changes in your working directory
git stash

# Reapply stashed changes to the working directory
git stash pop

# Tag the latest commit 'v1.4' (Useful for noting releases)
git tag -a v1.4 -m "my version 1.4"

# Push tag 'v1.4' to remote
git push origin v1.4

# Lookup help documentation for a particular command
git [command] --help
```

## The .gitignore File

* https://www.atlassian.com/git/tutorials/saving-changes/gitignore

## Git Workflows

* https://www.atlassian.com/git/tutorials/comparing-workflows

## Resources

Here is a good tutorial series that introduces version control and Git.  
https://www.atlassian.com/git/tutorials/what-is-version-control/

GitHub Guides  
https://guides.github.com/

Here is where you can download Git and find additional documentation.  
https://git-scm.com

Setup git config (see: 'Your Identity')  
https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

Sourcetree (GUI for git)  
https://www.sourcetreeapp.com/

And here are some advanced tutorials.  
https://www.atlassian.com/git/

Git Cheat Sheet  
https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet
