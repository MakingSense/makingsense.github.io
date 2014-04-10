---
layout: default
title: Dealing with line endings
---

Git was designed to manage large projects, with programmers distributed along the world and working over different platforms. You are probably aware that [different platforms represents the end of line with different codes](http://en.wikipedia.org/wiki/Newline#Representations), so, in order to avoid issues comparing files, Git supports a configuration to convert automatically Windows to Linux representation on storing data and Linux to Windows representation on getting data. 

In general, it is great, but some package managers like nuget, require to keep some files without modifications, so it becomes into a problem worst than the original one.

Our recommendation is to keep line ending by default by this configuration in `gitconfig` file ([see more](gitconfig-file.html):

    [core]
    autocrlf = false
    safecrlf = false

The property `safecrlf = false` is to avoid warning errors converting line endings in the files that we choose to convert automatically.


And allow to convert only certain kind of files by `gitattributes` file ([see more](gitattributes-file.html)):

    # Set default behaviour, in case users don't have core.autocrlf unset.
    * -text
    
    # These files are text and should be normalized (convert crlf =&gt; lf)
    *.cs      text diff=csharp
    *.xaml    text
    *.csproj  text
    *.sln     text
    *.msbuild text
    *.md      text

To be sure that some files (commonly included in the packages) are not touched we recommend to specify it:

    # These files should not be normalized
    *.js     -text
    *.css    -text
    *.less   -text

You can see a `.gitattributes` file  example [in our GitHub repository]({{ site.github.repository_url }}/blob/master/migration-to-git/3-working-with-git/examples/.gitattributes).


### More information

You can read more about this issue and other ways to deal with it in the follow links:

* [You're just another carriage return line feed in the wall](http://www.hanselman.com/blog/YoureJustAnotherCarriageReturnLineFeedInTheWall.aspx)
* [Hanselman - Mind the End of Your Line](http://adaptivepatchwork.com/2012/03/01/mind-the-end-of-your-line/)
* [Stack Overflow - What's the best CRLF handling strategy with git?](http://stackoverflow.com/questions/170961/whats-the-best-crlf-handling-strategy-with-git)
* [GitHub - Dealing with line endings](https://help.github.com/articles/dealing-with-line-endings)
* [Git, Nuget packages and Windows line-endings](http://pampanotes.tercerplaneta.com/2012/07/git-nuget-packages-and-windows-line.html)