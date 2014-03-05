---
layout: default
title: Fetch remotes
---

You already have your remotes configured (see [configure remotes]), now you want
to ensure that your local information related to them is updated with current 
remote status.

You can fetch the status of `bartsimpson` remote:

    git fetch bartsimpson
	
or you can fetch all your remotes:

    git fetch --all

Fetch does not make any changes to local branches, so you will need to merge a 
remote branch with a paired local branch to incorporate newly fetch changes.



[configure remotes]: /migration-to-git/3-working-with-git/configure-remotes.html