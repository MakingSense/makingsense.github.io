---
layout: default
title: Git concepts
---

It will include information about:

* Nomenclature 
* Concepts
* Git internal behaviour

### Internal

Git is fundamentally a content-addressable filesystem with a VCS user interface written on top of it. This means that at the core of Git is a simple key-value data store. You can insert any kind of content into it, and it will give you back a key that you can use to retrieve the content again at any time.

When you run `git init` in a new or existing directory, Git creates the `.git` directory, which is where almost everything that Git stores and manipulates is located. If you want to back up or clone your repository, copying this single directory elsewhere gives you nearly everything you need.

In that `.git` directory there are four important entries: the `HEAD` and `index` files and the `objects` and `refs directories`. These are the core parts of Git. The `objects` directory stores all the content for your database, the `refs` directory stores pointers into commit objects in that data (branches), the `HEAD` file points to the branch you currently have checked out, and the `index` file is where Git stores your staging area information.

### Glossary

#### Staging area aka Index

Is the place where you prepare your changes to commit_, a _middle_ between your working copy and the repository. You could add or remove files from the stage. Once you build your potential _next commit_ you usually want to review it using `git status` or `git diff`. Only then, you can _commit_ your changes with the command `git commit`.

#### Clone

Is a copy of a repository on your computer, always connected to the remote version in order to get the changes synced.

#### Fork

Is a copy of another user's repository that lives on a server but associated to your account. You can submit pull requests with your changes from your fork or even pull the updates from the original.

---

##### References

* [Pro Git book](http://git-scm.com/book)
* [GitHub Glossary](https://help.github.com/articles/github-glossary)

_Some texts are extracted directly from the references._
