---
layout: default
title: Why migrate to Git
---

<iframe src="http://prezi.com/embed/o3oij020l_oc/?bgcolor=ffffff&amp;lock_to_path=0&amp;autoplay=0&amp;autohide_ctrls=0&amp;features=undefined&amp;disabled_features=undefined" width="550" height="400" frameBorder="0">Prezi iframe (this content is required for markdown parsing)</iframe>

### Benefits for individuals
There are plenty of articles on the Internet about the benefits of using Git. Here we summarize some of the most important items for individuals:

#### You are in control
* You decide when (and how) to integrate changes from others.
* You decide when and what to commit
* You decide when the commits are published to others
* You decide how your commits will look like when published
* You decide what kind of workflow you want to use

#### You can truly isolate your tasks
* You can do as many local branches as you want
* You can stash your changes aside (or in a branch) whenever you want
* You can start a branch from any point in the history
* There’s never need to have same repository checked out more than once on your computer

#### You can do things fast
* Really many operations are local
* You’re not limited by the access speed to the source code server
* If source code server is offline, you’ll be able to continue working
* Even though Git repositories come with full history, Git uses disk space sparingly. In most cases repositories on disk are smaller than equivalent Subversion repositories.

#### You can learn from the past
* You can really easily check out any version of any file at any time. You don’t even need access to the source code server.
* You have full history of the repository available at all times.
* You can quickly view log, blame, branch or diff whatever and whenever you want

#### You can easily correct your mistakes
* You can perfect your commits before you publish them. If you want, you can squeeze your 28 commits into one.
* Totally messed up everything? Just scratch everything since last update from the server and start over.
* Want to revert what you already published? No problem, you can safely revert any commit when ever.
* Want to correct type in a commit message? If you didn’t publish your commits yet, it’s easy as taking a lollipop from a child.
You have plenty of backups
* Every clone of your repository is the whole repository. If your source code server blows up, repositories can be restored really quickly.

#### You can focus on the most important things
* Want to ignore some files relevant only for you? Easy.
* Want to ignore certain files on all clones of your repository? Easy.
* Want to create a new repository? Shouldn’t take longer than few minutes.
* Want to publish your local branch to others? It’s one command.

### Corporative reasons
Aside from making individuals life easier, Git has a number of other benefits for Corporations too, including:
* Data redundancy and replication -- Since there are multiple full repositories on multiple machines (instead of one central repository), the risk of project loss due to server failure or some other catastrophe is much lower.
* High availability -- Server down? Network down? No problem. Work in your repo (commit, view history, branch, etc) to your heart's content. 
* Only one .git directory per repository -- Versus a .svn in every subfolder, which, as you may know from painful personal experience, can lead to problems.
* Superior disk utilization and network performance
* Properties such as ignores are much easier to manage than in Subversion
* Collaboration Friendly -- Git makes it easy to collaborate on projects with groups of contributors. And with great services like Github, Git's collaboration friendliness is even further magnified.
* Not just for code! -- Git is great for all sorts of projects, not just hacking code. For example, written content.

In summary, source code management in Git it's secure, fast, and enterprise grade, allowing to create and manage repositories, set up fine-grained permissions, and collaborate on code – all with the flexibility of the own company servers.


<!--
TODO:

* Basic introduction
    * What is a version control system
    * centralized vs distributed
    * Git
    * GitHub
-->
