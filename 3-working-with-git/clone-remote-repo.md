---
layout: default
title: Clone remote repo
---

Suppose that you want to work in a repository that exists in a server or in the 
cloud. You cannot commit directly there. You need a local clone of that 
repository.

GitHub recommends accessing to repositories by HTTPS URL, SSH URL is also 
available if you prefer. See [this GitHub help page][remote-url-help] if you 
have troubles with authentication.  

We will create a local repository in the folder `c:\projects\migration-to-git` 
cloning `https://github.com/MakingSense/migration-to-git`

    cd c:\projects 
	git clone https://github.com/MakingSense/migration-to-git.git
	cd migration-to-git

It downloads a full copy of the remote repository into the selected folder 
(.git folder) and also prepare the working tree and configure a _remote_ repo 
named **origin** where you can fetch other people commits and push yours.

If you want to work with more that one remote repository see [configure remotes].

[configure remotes]: /migration-to-git/3-working-with-git/configure-remotes.html

