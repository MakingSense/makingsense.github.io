---
layout: default
title: Trick
---

### Remove a file in all branch commits

<!-- @easla when you have time, please, illustrate it with the scenario and anecdote behind this -->

```
    git filter-branch --tree-filter 'rm -rf Blocks.csv' HEAD
```