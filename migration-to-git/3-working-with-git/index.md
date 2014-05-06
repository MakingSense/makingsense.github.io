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
[Git GUI](git-clients.html) because they also include the command line 
tool.

**Warning**: Do not use PuTTY if you are given the option. GitHub only provides 
support for openssh.

### Conventions, standards and tips

* [commit conventions]
* [dealing with line endings]
* [Repo Boilerplate]


[commit conventions]: {{ site.github.url }}/migration-to-git/3-working-with-git/commit-conventions.html
[dealing with line endings]: {{ site.github.url }}/migration-to-git/3-working-with-git/dealing-with-line-endings.html
[Repo Boilerplate]: {{ site.github.url }}/migration-to-git/3-working-with-git/repo-boilerplate.html

### Operations

<!-- it is pending to sort this -->

* [fork a remote repo]
* [clone a remote repo]
* [configure remotes]
* [fetch remotes]
* [create a new branch]
* [commit changes]
* [push to a remote repo]
* [creating a pull request]
* [working with pull requests]
* [merge remote branches]
* [solve merge and rebase conflicts]


[fork a remote repo]: {{ site.github.url }}/migration-to-git/3-working-with-git/fork-a-repo.html
[clone a remote repo]: {{ site.github.url }}/migration-to-git/3-working-with-git/clone-remote-repo.html
[configure remotes]: {{ site.github.url }}/migration-to-git/3-working-with-git/configure-remotes.html
[fetch remotes]: {{ site.github.url }}/migration-to-git/3-working-with-git/fetch-remotes.html
[create a new branch]: {{ site.github.url }}/migration-to-git/3-working-with-git/create-a-new-branch.html
[commit changes]: {{ site.github.url }}/migration-to-git/3-working-with-git/commit-changes.html
[push to a remote repo]: {{ site.github.url }}/migration-to-git/3-working-with-git/push-to-a-remote-repo.html
[creating a pull request]: {{ site.github.url }}/migration-to-git/3-working-with-git/creating-a-pull-request.html
[working with pull requests]: {{ site.github.url }}/migration-to-git/3-working-with-git/working-with-pull-requests.html
[merge remote branches]: {{ site.github.url }}/migration-to-git/3-working-with-git/merge-remote-branches.html
[solve merge and rebase conflicts]: {{ site.github.url }}/migration-to-git/3-working-with-git/solve-merge-and-rebase-conflicts.html

### Configuration files

* [.gitignore-file]
* [.gitattributes-file]
* [.gitconfig-file]

[.gitignore-file]: {{ site.github.url }}/migration-to-git/3-working-with-git/gitignore-file.html
[.gitattributes-file]: {{ site.github.url }}/migration-to-git/3-working-with-git/gitattributes-file.html
[.gitconfig-file]: {{ site.github.url }}/migration-to-git/3-working-with-git/gitconfig-file.html

### Common Problems

* [Git Extensions issues]

[Git Extensions issues]: {{ site.github.url }}/migration-to-git/3-working-with-git/git-extension-issues.html

### Git Clients

There are a lot of [Git GUI clients](git-clients.html). In general, we can said 
that [Git Extensions]({{ site.github.url }}/migration-to-git/3-working-with-git/git-clients.html#git_extensions)
is a good choice to start because it helps you to understand how Git is working
internally.

### git-tfs

It is an useful tool when you have to migrate a TFS repository and also when Git and TFS should co-exist.

See [git-tfs readme](https://github.com/git-tfs/git-tfs/#readme) for a complete reference.

* [Clone a TFS repository to GitHub](git-fts-to-github.html)
* [Using TFS and Git together](git-fts-as-bridge.html)

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
