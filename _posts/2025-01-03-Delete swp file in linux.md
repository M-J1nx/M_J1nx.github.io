---
title:  "Delete .swp file in linux"
excerpt: "Let's delete .swp file when you're using linux."
categories: 
- Tips
tags:
- Theory
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-01-03
last_modified_at: 2025-01-03
published: true
---

## Situation  
![image](https://github.com/user-attachments/assets/687bdf2f-5892-42c9-9cec-2515504e15f0)


### Why is it happened?
If you use vim(vi) or Neovim, and if it closed unexpectly, it creates .swp file to recover. If you just leave .swp file, it does not matter, but you will encounter this screen everytime you try to access the file. 

## How to solve this?

![image](https://github.com/user-attachments/assets/9aca2f1e-1585-4f44-a5f1-18ab60e98002)
If you type ls -a , you can see .swp file. (Since it is hidden, you can't see this with `ls`) 

You can simply delete that. If you can’t find .swp file, try command below :
  cd /path/to/directory
  rm -i [swp file name] # Get confirm message before delete 

