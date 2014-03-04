---
layout: default
title: Working with Git
---

It is a general information page, but we are using GitHub so we will deepen
into GitHub specific tips.

Since there are a lot of Git clients we need a shared language, for that reason
we will use [Git commands] to explain some common actions.

### Installation

Installing Git is easy. In Linux, all repositories of all distributions have the 
related packages available and updated. For Mac and Windows, you can download it 
from [official Git download page] but we recommend to install your favourite 
[graphic client](git-clients.html) because they also include the command line 
tool.

**Warning**: Do not use PuTTY if you are given the option. GitHub only provides 
support for openssh.

### Operations

<!-- it is pending to sort this -->

* [fork a remote repo]
* [clone a remote repo]
* [configure remotes]


[fork a remote repo]: /migration-to-git/3-working-with-git/fork-a-repo.html
[clone a remote repo]: /migration-to-git/3-working-with-git/clone-remote-repo.html
[configure remotes]: /migration-to-git/3-working-with-git/configure-remotes.html

---

# WORK IN PROGRESS (probably deprecated)

### Create a local repository

### Commit changes

### Push changes to a remote repository

### Cloning a remote repository locally

We will create a local repository in the folder `c:\projects\migration-to-git` 
cloning `https://github.com/MakingSense/migration-to-git`

    cd c:\projects 
	git clone https://github.com/MakingSense/migration-to-git.git
	cd migration-to-git

GitHub recommends accessing to repositories by HTTPS URL, SSH URL is also 
available if you prefer. See [this GitHub help page][remote-url-help] if you 
have troubles with authentication.  


* [Git clients](git-clients.html) (hint)
* [Remotes naming](remotes-naming.html) (hint)
* [Commits description](commits-description.html) (mandatory)


# MORE WORK IN PROGRESS (probably deprecated)

It will include information like:
* Commands
* Conventions
* Standards




[remote-url-help]: https://help.github.com/articles/which-remote-url-should-i-use "Which remote URL should I use?"
http://git-scm.com/downloads
[official Git download page]: http://git-scm.com/downloads "Official Git download page"
[Git commands]: http://git-scm.com/docs
