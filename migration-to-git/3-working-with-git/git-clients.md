---
layout: default
title: Git clients
---

There are a lot of available clients for Git, some of these expose the internal Git design and 
architecture to the user, others hide the real Git power simplifying it for non-technical 
users. 

In general, at least for programmers, it is a good thing to know how Git works, because it will
allow us to take advantage of it. For that reason, most of the Git clients including a short-cut 
to Git command line tool.

### Git command line tool

The original Git user interface is the command line tool. Since many of us are accustomed to using 
Visual Studio, it may intimidate, but, come on! we are 
[hackers](http://tools.ietf.org/html/rfc1392#page-21), right? It is a shame if we do not assume 
the challenge. What is more, Microsoft itself is taking that way with _C# compiler (csc)_, _Windows 
Azure Cross-Platform Command-Line Interface_, _TypeScript Compiler (tsc)_ and _PowerShell_.

![Posh-Git over PowerShell and Git bash](git-clients-commandline.png)

It is possible to use Git command line tool with `cmd.exe` (discouraged) and also with _bash_ in Linux, 
Mac and also in Windows or you can use it with _PowerShell_. It is a nice PowerShell extension named 
Posh-Git.

#### Git command line tool Pros

* Complete functionality
* Very quick when you know the commands
* No impedance with Git internal behaviour

#### Git command line tool Cons

* Need to remember the commands
* Difficult to see diffs and branches

### Git Extensions

[Git Extensions](https://code.google.com/p/gitextensions/) is a graphical user 
interface for Git that allows a complete Git control without using the command 
line. Optionally, on the installation process, it could install Git command 
line tool and Git bash.

![Git Extensions](git-clients-git-extensions.png)

#### Git Extensions Pros

* Complete Git functionality.
* Near to one to one relation with command line commands.
* Easy to remember commands because they have icons
* Nice view of diffs and branches.

#### Git Extensions Cons

* It is not so quick as command line.
* Difficult to understand if you do not want to understand Git internal behaviour.

#### Git Extensions Issues

* See the following [link]({{ site.github.url }}/migration-to-git/3-working-with-git/git-extension-issues.html) about issues.

### Atlassian SourceTree

#### Atlassian SourceTree Pros

* It notifies you about pending pull (and quantity of commits) on remote repo, and respective details about them.
* It displays some big "buttons" to execute different commands on top bar and respective name for this commands (this is a good point for git beginners)

![Atlassian SourceTree Pros](git-clients-atlassian-sourcetree-pros.png)

### Visual Studio

### GitHub for Windows

#### GitHub for Windows Pros

* Very useful and intuitive for non-technical users. 
* It abstracts Git representations and commands.
* Very nice UI.
* Completely integrated with your GitHub account.

#### GitHub for Windows Cons

* It abstracts Git representations and commands.
* Incomplete Git functionality.
* Not so intuitive if you understand and like Git internal behaviour.
* *It does not support remotes*, only origin

### GitHub for Mac
