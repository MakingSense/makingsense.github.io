---
layout: default
title: Current Documentation Site Flow
---

### Making Sense GitHub Page Flow

The idea behind this flow, is to allow quickly create a documentation site with useful information for our internal migration, like a wiki. All of us are learning about it, so some content could be wrong, but it is easy to fix it, right?

#### Base branch

The sources of this site are stored on [GitHub repository]({{ site.github.repository_url }}) (I will call it `upstream`). When something is pushed to the branch `upstream/master`, it is automatically published to [the public site]({{ site.github.url }}) by _GiHub Pages_.

#### Simple fixes and permissions

For simple fixes, like typos, errors in references, etc it is allowed to push directly to `upstream/master`, but in general, our flow is based on pull requests, so do not worry if you do not have write access (but if you need it feel free to ask for).

#### Reporting issues

If you do not have time to fix the errors or add content, you can collaborate anyway [reporting an issue]({{ site.github.issues_url }}). Suggestions and comments are welcome.

#### Prepare environment for collaborate

If you want to edit site content (or also layout, styles, etc) we recommend you to fork the repository (see [fork a remote repo]) (I will call it `origin`),  clone it locally and also add a local remote for `upstream` (see [configure remotes]).

To have your own fork is also very useful if you want preview your changes, if you push to `origin/gh-pages` you can preview your version rendered in `https://your-user-name.github.io/makingsense.github.io`.

#### Add and edit content

1. The first is to be sure to have local environment updated fetching remotes (see [fetch remotes]).
2. Then, you can create a new local branch based on `upstream/master` (see [create a new branch]), it is the last published version.
3. Commit changes to our local branch (see [commit changes]).
4. Push to your `origin` repository when you want (see [push to a remote repo])
5. When you have something nice, create a pull request against `upstream/master`(see [creating a pull request])
6. Discuss and fix: after someone else has reviewed and signed off on the feature it could be merged to `upstream/master` (see [working with pull requests]). If something is wrong, discussion can continue in the _pull request_ and fixes can be push to the `origin` related branch. When all issues are fixed it could be merged.

#### Edit quickly in the browser

Another alternative to collaborate, is to made the changes directly in the browser. You can find useful information in the articles [GitHub Flow in the Browser](https://github.com/blog/1557-github-flow-in-the-browser) and [Web-flow editing from Pull Requests](https://github.com/blog/1738-web-flow-editing-from-pull-requests).



[clone a remote repo]: {{ site.github.url }}/migration-to-git/3-working-with-git/clone-remote-repo.html
[fork a remote repo]: {{ site.github.url }}/migration-to-git/3-working-with-git/fork-a-repo.html
[configure remotes]: {{ site.github.url }}/migration-to-git/3-working-with-git/configure-remotes.html
[fetch remotes]: {{ site.github.url }}/migration-to-git/3-working-with-git/fetch-remotes.html
[create a new branch]: {{ site.github.url }}/migration-to-git/3-working-with-git/create-a-new-branch.html
[commit changes]: {{ site.github.url }}/migration-to-git/3-working-with-git/commit-changes.html
[push to a remote repo]: {{ site.github.url }}/migration-to-git/3-working-with-git/push-to-a-remote-repo.html
[creating a pull request]: {{ site.github.url }}/migration-to-git/3-working-with-git/creating-a-pull-request.html
[working with pull requests]: {{ site.github.url }}/migration-to-git/3-working-with-git/working-with-pull-requests.html