---
layout: default
title: Configure remotes
---

Is is common to work with more than one remote repository. For example, you have 
a fork of an open source repository. Your fork is your `origin` remote and 
remote original repository is commonly called `upstream`. You can also have more 
remotes to see what is doing other people with their forks.

Suppose that your name is "Bart Simpson", you have a repository `https://github.com/bartsimpson/migration-to-git` cloned as `origin` in `c:\projects\migration-to-git`. You want to add a remote
named `upstream` related to `https://github.com/MakingSense/migration-to-git`:

    cd c:\projects\migration-to-git
	git remote add upstream https://github.com/MakingSense/migration-to-git

You can list your remotes:

    git remote -v
	
You can rename `upstream` as `making`:

    git remote rename upstream making

You can change remote's URL:
	
    git remote set-url making https://github.com/MakingSenseRepo2/migration-to-git
	
And you can delete it:

    git remote rm making
