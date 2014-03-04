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

See more details in [the Index].

#### Clone

Is a copy of a repository on your computer, always connected to the remote version in order to get the changes synced.

#### Fork

Is a copy of another user's repository that lives on a server but associated to your account. You can submit pull requests with your changes from your fork or even pull the updates from the original.

_References_

* [GitHub Glossary](https://help.github.com/articles/github-glossary)

[the Index]: /migration-to-git/2-concepts/the-index.html

