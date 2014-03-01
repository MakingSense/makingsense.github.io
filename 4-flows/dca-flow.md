---
layout: default
title: Flows and Branching models
---

### DCA Flow

<!-- I am not sure to include the complete Project and Client name here -->

**_based on [git-flow]_**

In this project we have time boxed sprints and previously defined release dates. 
Also, QA team is not so integrated in development process, there is not a large 
unit test coverage and neither a large automated test coverage yet. So, right 
now, in order to ensure quality we need a relatively large time of manual test 
over a stable environment. 

This is basically our workflow:

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


#### Origin repository

Our "central" repository path is https://github.com/MakingSense/dca (it does not 
exist yet), we will call it **origin** (and suggest to call it origin in your 
local clones).

In the origin repository we store develop branch, stabilization branch, releases
branches, hotfixes branches, releases tasks and optionally features branches.

#### Personal forks

We animate the team to have personal forks of origin repository in order to work
freely (we suggest to call it with your username in your local clones).

In a personal fork are stored features branchs and whatever the contributor wants.

It is allowed to _rewrite the history_ in personal branches, but try to not do 
it on branches with pull request associated or shared with other users.

#### The worflow

1. Sprint starts. In the planning we choose a lot features to implement!
2. Developers create features branches based on develop branch. These branches 
   could be stored on origin if some of them plan to work together, or it could 
   be stored on his personal forks.
3. When a feature is done, developers create a pull request using GitHub tool.
4. After some pair review, the feature branch is merged to develop.
5. When the sprint finish, we merge develop branch to stabilization branch. It 
   is a modification over [git-flow].
6. Work in progress


[git-flow]: http://nvie.com/posts/a-successful-git-branching-model/