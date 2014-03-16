---
layout: default
title: Flows and Branching models
---

### MSF Developer’s Workflow

_A story of too much work and no play, which makes Jack a dull boy._

#### Steps

1. Take items from JIRA
2. Work on them
3. Done: submit for review
4. TL gives feedback
5. Merged. PR closed. Finished.

#### 1. Take items from JIRA

* **Choose an item from the current sprint.** This means that the work is planned and that it is expected to be done soon.
* **If the ticket is already assigned to somebody, check with that person** that he/she has not already started with that work.
* **Assign it to yourself** (JIRA & Google Board), so others know that you’ll be working on that.

#### 2. Work on them

* **Make sure you understand what is expected from the ticket.** This includes what the user will see, what the Quality Analyst will test and what the Product Owner is trying to achieve. Try to understand each point of view and if the ticket does not make sense in any of those, reach out and raise that concern.
* **Depending on the complexity of the item, you may want to discuss with your team or your TL if design is needed** for it. If you’re developing a new functionality that is not similar to any of those implemented before, check as well with your teammates or your TL. In this way, they’ll be able to assist you with a proper design that is maintainable and that will also be useful for future upcoming work.
* Now that you know what needs to be done, **break down your work in tasks** (JIRA). This will help everyone keep track of where the ticket is. The tasks should be created as subtasks of the ticket that you assigned to yourself. Make sure that the title is understandable by someone that is not completely down with the details of the task. For example: “Update configuration values” (title) and “port should be 80” (description) is a good approach, while “set port 80” (title) is not.
* **Make sure your code is up to date:**
    * `git fetch -fpa`
    * `git checkout develop`
    * `git pull`
* **Create a branch of your own to work** on the ticket.
    * Branches should be titled with the following approach: `<itemType>/<date>/<handle>-<description>`
        * `<itemType>` is one of feature, fix, enhancement
        * `<date>` is the current date in yyyymmdd format.
        * `<handle>` is your github username
        * `<description>` is a short text explaining what the story is about. It may optionally contain the ticket number. Lowercase is encouraged. Separation with dashes is encouraged.
        * Examples:
            * `fix/20140401/nfranco-mcp-512-improve-user-workflow`
            * `feature/20131225/mravinale-christmas-module`
            * `enhancement/20140201/ezequiel12-`
    * `git checkout -b <branch-name>`
* **Focus on each task at a time** and work with it until you’re done.
* **Make sure to commit often**, hopefully each time that you have got a working change.
    * Examples: adding a new HTML file, fixing a unit test, etc.
    * Make sure that the first line of the commit message explains what the commit contains. Further lines can be added for details, but the first 80 characters need to be concise about the contents of the commit. Example: “Added feature-new.html”, or “Fixed wrong variable name”.
* **Write unit tests that validate your changes.** If possible, write these before your changes. For more information, you can read more about being [Introduced to TDD](http://www.agiledata.org/essays/tdd.html).
* **Push your changes to GitHub frequently.** In this way your changes will be backed up in the common repository in case somebody needs to see or work with your code. **Make sure to push your branch only.**

#### 3. Done: submit for review

* Once your ticket is finished (not each individual task), **run a quick functional test** to make sure that everything is working as expected in your environment.
* **Make sure that all unit tests are passing.**
* At this point, it is quite likely that your change has fallen behind on the develop branch. To bring it up to date:
    * `git fetch -fpa`
    * `git checkout develop`
    * `git pull`
    * `git checkout <your branch>`
    * `git rebase develop`
    * Git is going to apply your commits one at a time, and will pause if it finds a conflict it cannot resolve. If this is the case:
        * `git status` Git will show which files have conflicts. You’ll be able to open them and choose between your changes and other person’s changes. You’ll see the changes between big <<<<<<< HEAD and <<<<<<<< <your commit> indicators. **Fix the conflict** and make sure that the resulting file is correct and the way it was supposed to be at the end of that commit. If the commits are small, it is less likely that there will be conflicts, and they will be easier to solve too.
    * `git push -f origin <your-branch>:<your-branch>`
    * Visit the BackBone repository in GitHub
    * On the left side of the toolbar, pick your branch
    * Click on the “Compare” green button
    * Make sure that on the comparison screen, “develop” and <your branch> are shown.
    * Make sure that on the comparison screen only your commits are shown.
    * Click on “Click to create a pull request” for this comparison
    * Enter pull request data, including:
        * A descriptive title of the story
        * A reference to the ticket number
        * A general description of the changes that you did
        * Any notes to consider. Example: pending items, issues decided to be left as they are.
    * Click “Send pull request” and notify your TL to review the code.
    * **Update JIRA and Google Board** to make sure that everything is code complete / code review
    
#### 4. TL gives feedback

* The TL will provide feedback to your changes. **Discuss with him/her the best approach to these changes** until you reach an agreement.
* After reaching an agreement, **work to fix all important / urgent items** that had been agreed to fix before including the pull request into the codebase.
* **Push your changes** to the same branch, so that the pull request is updated. You can make as many commits as you like, so you don’t need to do everything at once.
    
#### 5. Merged. PR closed. Finished.

* At this point the TL has given the green light on your changes and has merged them into the codebase.
* Optionally, **you may test your changes into the CI environment.** This is recommended in the case of big changes or complex code. In the case of doubt, talk with your TL.
* **Give the green light to your TL** so that he/she moves everything to the QA bucket.
* The Quality Analyst will test your changes. If he/she find bugs and it is decided on this sprint, just repeat this flow with each bug. (You don’t need to work on these changes, but it’ll be easier for you since you developed it.)

#### General advice

When working on stories think of the full picture, it is usually a good idea to think of the overall design, the user experience and the complete workflow.

When working on bugs, it is usually better to keep changes to a minimum. (Unless the bug comes from a design issue.)
