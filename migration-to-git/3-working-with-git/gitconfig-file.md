---
layout: default
title: .gitconfig File
---

`.gitconfig` file is stored into your home folder, for example `C:\Users\bartsimpson` or `/home/bartsimpson`.

In general, is not necessary to edit this file. You can find more information about how to edit git configuration in [git-config Manual Page](http://git-scm.com/docs/git-config#FILES). In general Git GUI editors, have tools to help you on this.

Only an advertisement, in order to avoid line endings conversion problems we recommend to keep is as is by default:

    [core]
	autocrlf = false
    safecrlf = false

The property `safecrlf = false` is to avoid warning errors converting line endings in the files that we choose to convert automatically.

See more information in [dealing with line endings]({{ site.github.url }}/migration-to-git/3-working-with-git/dealing-with-line-endings.html) 


---

Some text extracted from <http://git-scm.com/docs/git-config> ([CC BY SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/))