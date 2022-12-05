---
title: "Git Basics"
date: 022-03-09T20:18:44+01:00
draft: true
categories: [development]
ShowToc: true
---

## Git merge
What is merge?  

### How to merge feature branch to main branch
To merge a branch `my-new-feature` to main branch.

```java
git checkout main
git merge my-new-feature
```
This will take all changes made in `my-feature-branch` and merge them to the `main` branch.



## Git rebase
What is git rebase?  
Simply put, it is to merge two branches, but to make sure that your changes is put in the end of the merged branch.  
Imagine you have a main branch and two separate feature branched (branch A and B).  
You are working on branch B and someone else is working on 


Why use git rebase?
To keep git history readable. 

## Check if git knows about your config file for file exclusion
git config --get core.excludesFile

## Make sure git knows where your configuration file is:
git config --global core.excludesFile '~/.gitignore_global'

# Remote
git remote -v

# List branches
- List all local branches
```
git branch
```
- List all remote branches
```
git branch -r
```
- List both local and remote branches
```
git branch -a
```

# Get status of current branch
```
git status
```

# Git remote
The git remote command lets you create, view, and delete connections to other repositories.  




