---
layout: default
title: Configure remotes
---

Is is common to work with more than one remote repository. For example, you have 
a fork of an open source repository. Your fork is your **origin** remote and 
remote original repository is commonly called **upstream**. 

Another scenery is when you are working against a private remote repository 
called **origin** and you have a personal fork named as your username. 

In both cases you can have more remotes to see what is doing other people with 
their forks.

Suppose that you have a repository `https://github.com/MakingSense/migration-to-git`
cloned as `origin` in `c:\projects\migration-to-git`. And you want to add a remote
named `bartsimpson` related to `https://github.com/bartsimpson/migration-to-git`:

    cd c:\projects\migration-to-git
	git remote add bartsimpson https://github.com/bartsimpson/migration-to-git

You can list your remotes:

    git remote -v
	
You can rename `bartsimpson` as `bart`:

    git remote rename bartsimpson bart

You can change remote's URL:
	
	git remote set-url bart https://github.com/bart/migration-to-git
	
And you can delete it:

    git remote rm bart
