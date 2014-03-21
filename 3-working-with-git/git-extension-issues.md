---
layout: default
title: Git Extensions Issues
---

### Issue when is performed a push to a remote repo

Git Extensions has an issue when you want to do a Push operation to a remote repo. It will always nag you requesting your credentials and it becomes extremely tedious.

![Push Issue](git-push-issue.png)

So, to solve this, you should modify the `.gitconfig` file located in `C:\Users\[USERNAME]\.gitconfig`. This file contains this structure:

    [merge]
        tool = kdiff3
    [mergetool "kdiff3"]
        path = C:/Program Files (x86)/KDiff3/kdiff3.exe
    [diff]
        guitool = kdiff3
    [difftool "kdiff3"]
        path = C:/Program Files (x86)/KDiff3/kdiff3.exe
    [core]
        editor = \"C:/Program Files (x86)/GitExtensions/GitExtensions.exe\" fileeditor
        autocrlf = true
    [credential]
        helper = !\\\"C:/Program Files/GitExtensions/GitCredentialWinStore/git-credential-winstore.exe\\\"
    [user]
        name = [your username]
        email = [your email]
		
The `[credential]` tag should be modified with: 

    [credential]
        helper = !\"C:/Program Files/GitExtensions/GitCredentialWinStore/git-credential-winstore.exe\"
	
And after that, bye bye nag screen and welcome peace of mind. :)
