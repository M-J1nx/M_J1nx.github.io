---
title:  "Git & Github Basic"
excerpt: "Basic information you should know if you want to cooperate with co-workers"
categories: 
- Git & Github
tags:
- Theory
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-01-21
last_modified_at: 2025-01-31
published: true
---

### What's Git&Github

Git : Software or tool to manage code. To use git, you should install software calling Git at your local environment.

Github : Storage to save code online. You can cooperate with other people by using github. 

However, Git is CLI(Command Line Interface), managing code through command like terminal, It can take time to get used to CLI environment for people who are not familier with CLI environment.

Therefore, if you are not used to CLI environment, and want to use git real quick, I recommend using **Github Desktop**.

To use git&github, we need three things below based on sumption you already have code editor such as visual studio code.

1. git ([git download](https://git-scm.com/downloads))
2. Sign up for github ([github homepage](https://github.com/github))
3. github desktop ([github desktop download](https://desktop.github.com/))

### Base concept of git 

1. **Branch** : Location of current work & Stem of work

![Branch has created and Stem of work exists ](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a656925-fc0e-4de1-9947-61a6517e8bb1/b1a63d6c-f42d-4510-8cea-b31d72fd206d/image.png)

Branch has created and Stem of work exists 

There is concept called **Branch** at git.

You can manage your work like one tree has many branches. Each branch's workspace is independent, and branches can't affect one another.

If main stem of the project is stem in the middle(It normally called as **master branch**.), you can make branches not to effect master branch whenever you need. 

Therefore, if you start new job in green branch, it doesn't effect main branch or purple branch. 


2. **Merge** : Combine branches  

We have master branch, which means main work, and work by dividing branches. We normally release master branch as total service, so if you want to update function of released service, you should update your new works in master branch.

We update new works by combining branches into mater branch in git.

We call combining action as **merge**. 

※ Merge is possible action not only for branches and mater branch, but also for branches each other.

3. **Commit** : Checkpoint of works  

When you are working, there will be changes. You may want to save those changed states at somewhere and keep working.

In this case, we can make checkpoint of work by commiting our works to git.

When you commit your works while you working in branch, works at commited point updated to branch, and we can use this as checkpoint. 

In other words, you can revert branch's state as you want.

4. **Repository** : Storage of the work 

We update works by commit, combine works by merge, manage work by branch.

The place where we saving our works called repository, and we usually call this as **repo** in short.

Repository can be local floder in your computer, and it also can be online storage like github.

### Works of git 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a656925-fc0e-4de1-9947-61a6517e8bb1/abe2631e-d382-4925-87f1-499defb88654/image.png)

- push
    
    로컬 컴퓨터에서 작업하고, 작업을 커밋했을 때 만약 이를 깃허브에서 온라인으로 보기를 원하다면 푸시라는 작업을 해줘야 한다. 커밋한 작업을 온라인으로 올려주는 것이다. 
    
- pull
    
    로컬 컴퓨터에서 작업할 때, 작업하고 있는 레포지토리의 상태를 받아오고 싶다면 pull을 해줘야 한다. 레포지토리를 당겨온다고 생각하면 된다.
    
    보통 깃허브에서 다른 사람과 온라인으로 함께 작업을 할 때, 다른 사람의 작업물을 받아오고 싶다면 pull을 해준다. 
    
- pull request
    
    코드의 변경사항을 원본 코드에 병합하기 위해 제안하는 것을 의미한다. 즉, 병합하기 전에 해당 코드를 병합해도 되는지 물어보는 것이다. 
    
    일반적으로 마스터 브랜치에 머지 하기 전에 해당 과정을 거친다.
