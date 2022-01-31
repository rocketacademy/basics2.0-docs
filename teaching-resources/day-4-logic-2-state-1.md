# Day 4: Logic 2, State 1

## Overview

Total Video Watch Time: **\~41 mins**

This day introduces the boundaries of the lifecycle of the starter code. Specifically at the beginning when the JavaScript file loads until the refresh button gets clicked.

Within this time span we introduce the idea of global values that are manipulated again and again as the user clicks the submit button.

We are also introducing the idea that the code can deal with more dynamic values other than the `input` variable.

This day also introduces the GitHub project submission workflow.

## [7.1: GitHub Fork and Pull Request](../8-github/7.1-github-fork-and-pull-request.md)

### Overview

This section introduces the workflow for submitting the projects. This is also the first time we mention a flow of the repo from the local computer to GitHub. (Before it was always from GitHub to the local computer.) This section mixes together functionality from the GitHub webapp (fork, pull request) and the Git command line version control system (push).

### Fork

A fork is when GitHub makes a copy of a repo into the user's GitHub account. By default the copy is frozen at the point at which it was copied and from within Git is no longer connected to the other GitHub account original repo. Remember that in this context _**repo**_ means the code and the record of all it's versions, not just the code itself.

#### Discussion Questions

#### Q: What does a fork do?

A: It copies a repo from one account into another.

#### Q: How do you fork?

A: Click the button on a repo's page in GitHub.

#### Q: Can you fork a repo more than once?

A: No, GitHub will only make one copy from one account to another.

### Git Push

`push` is a Git command that takes changes from a local repo and puts them on a remote repo. `push` is not a GitHub functionality.

#### Discussion Questions

#### Q: What does `push` do?

A: `push` puts the new changes to the repo onto the GitHub copy of the repo.

#### Q: I committed changes to my code twice. How many times do I run the push command?

A: A Git push is to bring all commits over to the remote repo. The command will transfer all the commits over.

#### Q: Can I `push` the changes I made to GitHub if I didn't fork the repo?

A: No, without forking it means the code you cloned belongs to Rocket Academy. You cannot give back your own changes to a repo owned by Rocket Academy.

### Pull Request

A pull request is a GitHub web application feature that allows communication between people working on code.

#### Discussion Questions

#### Q: What is the difference between a Pull Request and `git pull`?

A: `git pull` is a Git command line command. We won't be using `git pull` during basics. A pull request is a feature of the GitHub web app that enables collaboration between people working on code.

#### Q: What are the sequence of steps needed to submit a pull request for Basics?

A: 1) Fork the project repo. 2) Clone the project repo. 3) Make local changes to the project repo. 4) Push changes. 5) Go to github.com and create the pull request.

#### Q: I made new changes and pushed them to my repo. Do I need to create another pull request?

A: No. All the changes you pushed to your repo will appear in your original pull request.

## [7.2: GitHub Navigation](../8-github/7.2-github-repo-browsing.md)

### Overview

This section finishes the full workflow that was described when Git was introduced. So far students have been storing the set of changes they make to their code, but they have never been able to view every set of changes.

This section shows students how to navigate the GitHub website to see a record of any and all changes they made to the code.

There are Git command line commands that will get back any version from a commit, but in the case that a student wants to get back any older version of the code, they can simply navigate to it in GitHub and copy/paste it back and make a new commit.

**Q: Ask a student to share screen and navigate to a repo they have pushed changes to. They should have a least one if they followed the exercise in 7.1. Ask to see the list of commits. Ask to see the diff of a single commit by clicking into the single commit.**

## [8.1: Program Lifecycle and Global State](../5-managing-state-and-input-validation/8.1-program-lifecycle-and-state.md)

### Overview

This section introduces dynamic global variables.

#### Discussion Questions

```javascript
var papayaCount = 0;
var main = function (input) {
  papayaCount = papayaCount + 1;
  var myOutputValue = 'You have ' + papayaCount + ' papayas';
  return myOutputValue;
};
```

#### Q: What does this code do?

#### Q: What is the difference between line 1 with the `var` keyword and line 3 without?

A: `var` keyword is for variable _**creation**_. Without the `var` keyword we are reassigning a value to the variable.

#### Q: What behaviour would we see if we moved line 1 inside the main function?

A: Defining the variable inside the function means that it is created brand new each time the function runs.

Putting the variable on line 1 means that it is created at the beginning of the life of the program.

#### Q: What would happen if we moved line 1 below line 6?

A: It wouldn't affect anything. This is because, even though the definition of `papayaCount` is on a later line, it is still defined _**before**_ the main function is run. Line number and the order of code running are not necessarily the same thing.

#### Q: Will moving line 4 above line 3 make a difference in how the program behaves?

A: This does change the behaviour. The original version of this code adds a papaya every time the button gets clicked. Then it displays the value. (You see 1 after the first click). The suggested change displays the current number of papayas when the button gets clicked, then adds one papaya. (You see 0 after the first click) The order in the code depends on which behaviour you want.

## In-Class Material

1. [Day 4: Boolean And, GitHub, Program State](../in-class-exercises/day-4-boolean-and-program-state.md)

## **Wrap-up / Look Ahead**

In this section we added onto the total amount of values our programs deal with by writing a new variable for each global value. We then put back in our conditionals to use the two together in a dice game. Next, we'll use global values and conditionals together to represent different modes of the game. This will give us the ability to ask the user for different kinds of input.

### **Post-Class: Begin Project Part 2**

This part of SPS uses global state to build in more features of the game. To do the more comfortable you may have to read ahead to the game mode sections.

In the next meeting we'll be doing peer review of the SPS code.

[Project 1: Scissors Paper Stone (Part 2)](../projects/project-1-scissors-paper-stone/project-1-scissors-paper-stone-part-2.md)
