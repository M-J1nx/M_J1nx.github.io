---
title:  "Can’t access to same room in photon"
excerpt: "If you can't access to same room, here's the solution"
categories: 
- Game
tags:
- Theory
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-02-12
last_modified_at: 2025-02-12
---

I’m developing match making system in Unity using Photon.

But suddenly, I can’t access to same room even if I check that I’m accessing same room.

⚠️ This solution assume that you already have Photon in your project. 

Here is the solution:

Window → Photon Unity Networking → Highlight server settings

You can see `Fixed Region` box. 

Type **only one** region to fix region. 
Then, you’ll see your server works.
