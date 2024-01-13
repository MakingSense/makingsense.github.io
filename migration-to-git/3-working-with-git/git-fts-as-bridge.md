---
layout: default
title: Using TFS and Git together
---

If you need continue checking-in to TFS along you work with Git, you can use git-tfs as a bridge.

It supposed that git-tfs supports to check-in in name of another developer, but for some reason (maybe TFS permissions, maybe it is not ready yet, maybe my fault) it didn't work for me, so, in our team we decided that each developer check-in in TFS his changes after merge his pull requests.

### 1. Prepare environment for developers

* Clone GitHub repository <!-- TODO -->
* Bootstrap git-tfs <!-- TODO -->

### 2. Work in a feature

<!-- TODO (fetch remotes, fetch tfs, start a new branch, commit changes) -->

### 3. Create a pull request

<!-- TODO (Rebase or merge upstream changes, create the pull request, discuss) -->

### 4. Merge pull request and check-in in TFS

<!-- TODO (Merga the pull request, fetch remotes, fetch tfs, check-in in TFS, push to upstream) -->