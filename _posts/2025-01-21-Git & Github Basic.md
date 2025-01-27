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
last_modified_at: 2025-01-27
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

1. **Branch :** Location of current work & Stem of work

![Branch has created and Stem of work exists ](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a656925-fc0e-4de1-9947-61a6517e8bb1/b1a63d6c-f42d-4510-8cea-b31d72fd206d/image.png)

Branch has created and Stem of work exists 

There is concept called **Branch** at git.

마치 하나의 나무가 가지를 뻗어나가듯이 작업을 관리하게 되는데, 각각의 브랜치는 작업 영역이 독립적이고, 브랜치끼리는 영향을 미치지 않는다. 

가장 핵심 작업의 줄기가 중앙에 있는 줄기라고 할 때(흔히 master 브랜치 라 불림), 필요의 따라서 master 브랜치의 영향이 없도록 브랜치들을 만들어서 작업을 수행함 

즉, 초록색 브랜치에서 새롭게 작업을 한다고 하더라도 핵심 작업의 브랜치나 보라색 브랜치에 변화를 주지 않는다. 

1. **Merge** : Branch 들을 합치는 행위 

앞서 우리는 중앙 작업인 마스터 브랜치를 두고, 브랜치를 나누어서 작업을 했다. 통상적으로 마스터 브랜치를 서비스로써 배포하기 때문에, 배포할 서비스의 기능을 업데이트 하기 위해서는 작업한 내용을 마스터 브랜치에 업데이트 해줘야 한다. 

우리는 깃에서 브랜치를 마스터 브랜치에 병합시켜줌으로써 마스터 브랜치에 작업을 업데이트 해 준다. 

이 때 병합하는 것을 ‘머지한다’ 라고 표현한다.

※ 머지는 브랜치를 마스터 브랜치에 병합시키는 것 뿐만 아니라 브랜치들끼리 병합시키는 것도 가능하다. 

1. **Commit** : 작업의 체크포인트 

우리는 브랜치를 두고 작업을 할 것이다. 작업을 하다 보면 변경 사항이 생길 것이고, 변경된 상태를 어딘가에 저장해두고 작업을 이어나가고 싶을 수도 있을 것이다. 

이 경우, 우리는 깃에 작업을 커밋 해줌으로써 작업의 체크포인트를 생성할 수 있다.

브랜치에서 작업을 하다가 작업을 커밋하면, 커밋한 시점의 작업이 브랜치에 반영 되고, 우리는 이것을 체크포인트처럼 사용할 수 있다. 즉, 원하는 커밋으로 브랜치의 상태를 되돌릴 수 있는 것이다. 

1. **Repository** : 작업의 저장소

우리는 커밋으로 작업을 업데이트하고, 머지로 작업들을 합칠 수 있으며, 브랜치로 작업을 관리할 수 있다.

이런 작업들을 저장하는 것을 깃에서는 레포지토리라고 부르며, 대게 줄여서 레포라고 부른다. 

레포지토리는 컴퓨터 안의 로컬 폴더가 될 수도 있고, 깃허브나 다른 온라인 저장 공간이 될 수도 있다. 

### 깃의 작업

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a656925-fc0e-4de1-9947-61a6517e8bb1/abe2631e-d382-4925-87f1-499defb88654/image.png)

- push
    
    로컬 컴퓨터에서 작업하고, 작업을 커밋했을 때 만약 이를 깃허브에서 온라인으로 보기를 원하다면 푸시라는 작업을 해줘야 한다. 커밋한 작업을 온라인으로 올려주는 것이다. 
    
- pull
    
    로컬 컴퓨터에서 작업할 때, 작업하고 있는 레포지토리의 상태를 받아오고 싶다면 pull을 해줘야 한다. 레포지토리를 당겨온다고 생각하면 된다.
    
    보통 깃허브에서 다른 사람과 온라인으로 함께 작업을 할 때, 다른 사람의 작업물을 받아오고 싶다면 pull을 해준다. 
    
- pull request
    
    코드의 변경사항을 원본 코드에 병합하기 위해 제안하는 것을 의미한다. 즉, 병합하기 전에 해당 코드를 병합해도 되는지 물어보는 것이다. 
    
    일반적으로 마스터 브랜치에 머지 하기 전에 해당 과정을 거친다.