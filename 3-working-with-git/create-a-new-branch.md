---
layout: default
title: Create a new branch
---

You want to create a new branch named `edit-mobile-locations` based on `develop` 
branch. In the future you want to push the branch commits to `bartsimpson` 
remote repository.

The first step is to checkout the base branch:

    git checkout develop 
	
Now you can create a new branch based on current that is associated to an 
specific remote repository/branch:

    git checkout edit-mobile-locations --track bartsimpson/edit-mobile-locations
	
Since you have been used `checkout` command, your working tree is pointing to 
the new branch.
	
More about checkout in [git-checkout Manual Page]


[git-checkout Manual Page]: http://git-scm.com/docs/git-checkout