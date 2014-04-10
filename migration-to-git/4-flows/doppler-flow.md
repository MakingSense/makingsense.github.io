---
layout: default
title: Flows and Branching models
---

### Doppler Flow

**_based on [git-flow]_**

In this project we have time boxed sprints and one release for sprint.
We have two environments for QA Control, the Integration which is for continuous integration and QA which is for regressions and demo.
When a story is developed or a bug is fixed, the changes made by the developer, are merged into one of our main branches, named `develop`. 
Our Integration environment is pointing to that branch and it's deployed (manually through Jenkins) with the last changes of `develop` as needed.
When the sprint finish, we create a branch from `develop` with a release number (release candidate). This branch will be pointed by QA environment and the QA Team will run the regression over it. 

1. In a sprint, DEV team develop a set of features or stories. 
2. Before integrate each feature, DEV team made a collaborative review using the [pull request] of github. 
3. During the sprint DEV team deploy regularly to Integration environment to allow QA 
   team to test there in an relatively unstable environment.
4. At the end of the sprint, DEV team deploy to QA environment where a demo is 
   presented and the client suggest some minor changes or fixes. QA team will 
   work on QA branch testing the sprint output in a stable environment and doing 
   a sanity or regression test.
5. DEV Team apply client suggestions and fix the bugs detected by QA team in the 
   next sprint, at the same time that they work on next sprint features.
6. QA environment fixes are deployed regularly. And after some stabilization, 
   it is ready to go to Production.
7. When the regression is finished the changes are deployed on production.

#### Central repository (Upstream)

Our "central" repository path is https://github.com/MakingSense/Doppler, we will call it `upstream` (and suggest to call it upstream in your local clones too).

In the upstream repository we maintain: `develop` branch, _releases_ branches, _hotfixes_ branches, _releases_ tags and optionally _features_ branches.

#### Personal forks

To work in this project we will have personal forks of upstream repository in order to work
freely (we suggest to call it `origin` in your local clones).

In a personal fork are maintained _features_ branches and whatever the 
contributor wants.

You can track the changes of other personal forks (see [configure remotes]), in
that case we suggest to call them as the owner's username.

**Note:** It is allowed to _[rewrite the history]_ in personal branches, but try 
to not do it on branches with _pull request_ associated or shared with other 
users.

#### Our git flow

**Initial configuration:** 

`upstream` repository is created at GitHub (see [repo boilerplate]), team members have cloned it in their local environments (see [clone a remote repo]). Also, they have created personal forks (see [fork a remote repo]) and they have configured their local "remotes" repositories (see [configure remotes]). 

Sprint `N` starts. In the planning we choose a lot features to implement!

**Steps:**

1. A developer chooses a task or feature to implement from sprint board.

    * He updates his local clone with the latest changes (see [fetch remotes]).
    * Based on `upstream/develop` branch, he creates a local branch for the feature (with 
      a representative name) (see [create a new branch]).
	  
2. Our developer works in the task

    * He tries to commit atomic and meaning changes (see [commit changes]).
    * He tries to keep his changes pushed to a remote repository, it could be 
      `upstream` (our central repository) or `origin` (his personal fork) (see [push to a remote repo]).
	  
3. Task is done

    * Our developer commits and push all his changes to the remote and creates 
      a _pull request_ to `upstream/develop` (see [creating a pull request]).
    * Some other developers in the team do a quick code review.
    * After someone else has reviewed and signed off on the feature it could be 
      merged to `upstream/develop` (see [working with pull requests]). 
    * If something is wrong, discussion can continue in the _pull request_ and fixes can be push to the _feature_ branch . When all issues are fixed it could be merged

4. Sprint finishes

    * `upstream/develop` branch is merged to a new release branch_ in `upstream` repository (see  [merge remote branches]).
    * Preparation to production is done in the new _release branch_

5. QA in _release branch_ branch

    * When QA team detect issues on regression stage in _release branch_, they are fixed intermediately
    * In order to fix them, our developer creates a new branch, the steps are like in points `1`, `2` and `3` but based on _release branch_ branch in place of `develop`.
    * _release branch_ is fairly often merged to `develop`.
    * When QA stage finish, _release branch_ is merged to _master_.

6. The release!

    * The release date day has arrived, code on `master` is tagged and deployed to production environment.

7. Hurry! A critical issue in Production!

    * If something goes wrong in production, the process to fix it is similar to steps `5` but in place of using a _release branch_, it is done in a new _hotfix branch_ based on `upstream/master` or in the last release tag.

In this small [tutorial] you can view a part of this flow applied. 

[git-flow]: http://nvie.com/posts/a-successful-git-branching-model/
[repo boilerplate]: /migration-to-git/3-working-with-git/repo-boilerplate.html
[clone a remote repo]: /migration-to-git/3-working-with-git/clone-remote-repo.html
[fork a remote repo]: /migration-to-git/3-working-with-git/fork-a-repo.html
[configure remotes]: /migration-to-git/3-working-with-git/configure-remotes.html
[fetch remotes]: /migration-to-git/3-working-with-git/fetch-remotes.html
[create a new branch]: /migration-to-git/3-working-with-git/create-a-new-branch.html
[commit changes]: /migration-to-git/3-working-with-git/commit-changes.html
[push to a remote repo]: /migration-to-git/3-working-with-git/push-to-a-remote-repo.html
[creating a pull request]: /migration-to-git/3-working-with-git/creating-a-pull-request.html
[working with pull requests]: /migration-to-git/3-working-with-git/working-with-pull-requests.html
[pull request]: /migration-to-git/3-working-with-git/working-with-pull-requests.html
[merge remote branches]: /migration-to-git/3-working-with-git/merge-remote-branches.html
[rewrite the history]: http://git-scm.com/book/ch6-4.html
[tutorial]: /migration-to-git/4-flows/doppler-flow-example.html
