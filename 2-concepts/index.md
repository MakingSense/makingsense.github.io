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

In that `.git` directory there are four important entries (among others): the `HEAD` and `index` files and the `objects` and `refs directories`. These are the core parts of Git. The `objects` directory stores all the content for your database, the `refs` directory stores pointers into commit objects in that data (branches), the `HEAD` file points to the branch you currently have checked out, and the `index` file is where Git stores your staging area information.

#### Objects everywhere

Initially, Git stores the content as a single file per piece of content, named with the SHA-1 checksum of the content and its header. The subdirectory is named with the first 2 characters of the SHA, and the filename is the remaining 38 characters:

    .git/objects/d6/70460b4b4aece5915caf5c68d12f560a9fe3e4
    
##### Tree Objects

All the content is stored as tree and blob objects, with trees corresponding to UNIX directory entries and blobs corresponding more or less to inodes or file contents. A single tree object contains one or more tree entries, each of which contains a SHA-1 pointer to a blob or subtree with its associated mode, type, and filename.

##### Commit Objects

Stores any information about who saved the snapshots, when they were saved, or why they were saved.

The format for a commit object is simple: it specifies the top-level tree for the snapshot of the project at that point; the author/committer information pulled from your `user.name` and `user.email` configuration settings, with the current timestamp; a blank line, and then the commit message.

### Glossary

#### Staging area aka Index

Is the place where you prepare your changes to commit, a _middle_ between your working copy and the repository. You could add or remove files from the stage. Once you build your potential _next commit_ you usually want to review it using `git status` or `git diff`. Only then, you can commit your changes with the command `git commit`.

#### Clone

Is a copy of a repository on your computer, always connected to the remote version in order to get the changes synced.

#### Fork

Is a copy of another user's repository that lives on a server but associated to your account. You can submit pull requests with your changes from your fork or even pull the updates from the original.

---

##### References

* [Pro Git book](http://git-scm.com/book)
* [GitHub Glossary](https://help.github.com/articles/github-glossary)

_Some texts are extracted directly from the references._
