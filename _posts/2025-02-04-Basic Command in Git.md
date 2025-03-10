---
title:  "Basic Command in Git"
excerpt: "Basic commands that you'll often use in git."
categories: 
- Git
tags:
- Theory
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-02-04
last_modified_at: 2025-02-04
---

## Base commands

`git init` : Initialize an existing directory as a Git repository.  
`git remote add origin [url]` : add a remote repository.  
`git add [file] or git add .` : add one or more files to staging area.  
`git commit -m “[ Type in the commit message]”` : commit changes to head (but not yet to the remote repository).  
`git push origin [branch]` : send changes to the master branch of your remote repository.  

## Track project

`git status` : list which files are staged, unstaged, and untracked.  
`git log` : show all commits, and starting with newest.  

## Cloning and collaboration
`git clone [url]` : clone a repository that already exists on GitHub, including all of the files, branches, and commits.  
`git pull` : fetch and merge changes on the remote server to your working directory.  

## Branches
`git branch [branch-name]` : create a new branch at the current commit.  
`git checkout [branch-name]` : switch to another branch and check it out into your working directory.  
`git merge [branch]` : merge the specified branch’s history into the current one.  

## Setup
`git config --global user.name “[firstname lastname]”` : set a name that is identifiable for credit when review version history.  
