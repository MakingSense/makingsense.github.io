---
layout: default
title: Git concepts
---

It will include information about:

* Nomenclature 
* Concepts
* Git internal behaviour

#### Staging area aka Index

Is the place where you prepare your changes to _commit_, a _middle_ between your working copy and the repository. You could add or remove files from the stage. Once you build your potential _next commit_ you usually want to review it using `git status` or `git diff`. Only then, you can _commit_ your changes with the command `git commit`.