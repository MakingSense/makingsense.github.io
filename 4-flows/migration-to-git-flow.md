---
layout: default
title: Current Documentation Site Flow
---

### migration-to-git Flow

The idea behind this flow, is to allow quickly create a documentation site with useful information for our internal migration. All of us are learning about it, so some content could be wrong, but it is easy to fix, right?

#### Base branch

The sources of this site are stored on [GitHub repository](https://github.com/MakingSense/migration-to-git) (I will call it `upstream`). When something is pushed to the branch `upstream/gh-pages`, it is automatically published to [the site](http://makingsense.github.io/migration-to-git) by _GiHub Pages_.

#### Simple fixes and permissions

For simple fixes, like typos, errors in references, etc it is allowed to push directly to `upstream/gh-pages`, but in general, our flow is based on pull requests, so do not worry if you do not have write access (but if you need it feel free to ask for).

#### Reporting issues

If you do not have time to fix the errors or add content, you can collaborate anyway [reporting an issue](https://github.com/MakingSense/migration-to-git/issues). Suggestions and comments are welcome.

#### Prepare environment for collaborate

If you want to edit site content (or also layout, styles, etc) we recommend you to fork the repository (see [fork a remote repo]) (I will call it `origin`),  clone it locally and also add a local remote for `upstream` (see [configure remotes]).

#### Add and edit content

1. The first is to be sure to have local environment updated fetching remotes (see [fetch remotes]).
2. Then, you can create a new local branch based on `upstream/gh-pages` (see [create a new branch]), it is the last published version.
3. Commit changes to our local branch (see [commit changes]).
4. Push to your `origin` repository when you want (see [push to a remote repo])
5. When you have something nice create a pull request against `upstream/gh-pages`(see [creating a pull request])

# WORK IN PROGRESS

[clone a remote repo]: /migration-to-git/3-working-with-git/clone-remote-repo.html
[fork a remote repo]: /migration-to-git/3-working-with-git/fork-a-repo.html
[configure remotes]: /migration-to-git/3-working-with-git/configure-remotes.html
[fetch remotes]: /migration-to-git/3-working-with-git/fetch-remotes.html
[create a new branch]: /migration-to-git/3-working-with-git/create-a-new-branch.html
[commit changes]: /migration-to-git/3-working-with-git/commit-changes.html
[push to a remote repo]: /migration-to-git/3-working-with-git/push-to-a-remote-repo.html
[creating a pull request]: /migration-to-git/3-working-with-git/creating-a-pull-request.html