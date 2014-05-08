---
layout: default
title: Flows and Branching models
---

### DCA Flow

**_based on [git-flow]_**

In this project we have time boxed sprints and previously defined release dates. 
Also, QA team is not so integrated in development process, there is not a large 
unit test coverage and neither a large automated test coverage yet. So, right 
now, in order to ensure quality we need a relatively large time of manual test 
over a stable environment. 

For these reasons, we cannot follow the git-flow as it is, so we decided to change the meaning of `master` branch to represent all code that have passed all QA stages and it supposed that it is really ready to go to production. Also, we decided to change _release branches_ for _version branches_ which represent the output of a sprint and could be potentially deployable to production. So stabilization stage is done on these _version branches_, when it is stable, it is merged to `master`, when it is deployed to production it is tagged.

This is basically our workflow (without think about version control):

![Sprint template](dca-sprint.png)

1. In a sprint, DEV team develop a set of features or stories. 
2. Before integrate each feature, DEV team made a quick pair code review.
3. During the sprint DEV team deploy regularly to INT environment to allow QA 
   team to test there in an relatively unstable environment.
4. At the end of the sprint, DEV team deploy to QA environment where a demo is 
   presented and the client suggest some minor changes or fixes. QA team will 
   work on QA branch testing the sprint output in a stable environment and doing 
   a sanity or regression test.
5. DEV Team apply client suggestions and fix the bugs detected by QA team in the 
   next sprint, at the same time that they work on next sprint features but 
   without mixing the code. 
6. QA environment fixes are deployed regularly. And after some stabilization, 
   it is ready to go to Production, we do not deploy to production in all sprints.
7. In specific dates, we deploy to production all stable code.


#### Central repository (Upstream)

Our "central" repository path is https://github.com/MakingSense/dca (it does not 
exist yet), we will call it `upstream` (and suggest to call it upstream in your 
local clones too).

In the upstream repository we maintain: `develop` branch, _versions_ branches, _hotfixes_ branches, _releases_ tags and optionally _features_ branches.

#### Personal forks

We animate the team to have personal forks of upstream repository in order to work
freely (we suggest to call it `origin` in your local clones).

In a personal fork are maintained _features_ branches and whatever the 
contributor wants.

You can track the changes of other personal forks (see [configure remotes]), in
that case we suggest to call them as the owner's username.

**Note:** It is allowed to _rewrite the history_ in personal branches, but try 
to not do it on branches with _pull request_ associated or shared with other 
users.

**Note II:** If you do not like to use a personal fork, no problem, you can call `origin` to https://github.com/MakingSense/dca and create your branches there. _If it gets dirty, we will ban this possibility in a future_.

#### Our git flow

**Initial configuration:** 

`upstream` repository is created at GitHub (see [repo boilerplate]), team members have cloned it in their local environments (see [clone a remote repo]). Also, they have created personal forks (see [fork a remote repo]) and they have configured their local "remotes" repositories (see [configure remotes]). 

Sprint `N` starts. In the planning we choose a lot features to implement!

**Steps:**

1. A developer chooses a task or feature to implement from sprint board.

    * If the task is enough large, he can create a sub-task and put it in "in 
      progress" state. 
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

    * `upstream/develop` branch is merged to a new _version branch_ in `upstream` repository (see 
      [merge remote branches]).
    * Preparation to production is done in the new _version branch_ updating meta-data like version number, build dates, etc.
    * Sprint `N+1` starts with a planning.

5. QA in _version branch_ branch

    * When the client and QA team detect issues in _version branch_, they are prioritized and some of them cold be included in current sprint `N+1`
    * In order to fix them, our developer creates a new branch, the steps are like in points `1`, `2` and `3` but based on _version branch_ branch in place of `develop`.
    * _version branch_ is fairly often merged to `develop`.
    * When QA stage finish, _version branch_ is merged to _master_.

6. The release!

    * The release date day has arrived, code on `master` is tagged and deployed to production environment.

7. Hurry! A critical issue in Production!

    * If something goes wrong in production, the process to fix it is similar to steps `5` but in place of using a _version branch_, it is done in a new _hotfix branch_ based on `upstream/master` or in the last release tag.

	  

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
[merge remote branches]: /migration-to-git/3-working-with-git/merge-remote-branches.html
