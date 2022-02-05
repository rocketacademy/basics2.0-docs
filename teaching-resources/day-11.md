# Day 11: Debugger

## **Overview**

Today is the last course day before the final project presentation. Unlike other project submissions this one is meant so that students will be able to review each other's work before they present the finished version.

## **Project Due**

[Project 3: Blackjack](../coursework/projects/project-3-blackjack.md)

## Pre-Class Material

Total Video Watch Time: **\~18 mins**

### [11.1: Advanced Debugging with Sources Tab](../modules/6-advanced/11.1-advanced-debugging-with-sources-tab.md)

We've already seen debugging with the simple tool of `console.log`. Sometimes this is not enough. If the code is behaving in a way that doesn't make sense or there is an error in a loop that runs many times and creates a hard to read console.log output, the next level of control and granularity is to use the debugger.

```javascript
var main = function (input) {
  var myOutputValue = '';
  // sideLength represents the length of each side of the square
  var sideLength = Number(input);
  var outerCounter = 0;
  while (outerCounter < sideLength) {
    var innerCounter = 0;
    while (innerCounter < sideLength) {
      // If current iteration represents a border element, draw ✊ instead.
      if (outerCounter == 0 || outerCounter == sideLength - 1
        || innerCounter == 0 || innerCounter == sideLength - 1) {
        myOutputValue += '✊';
      } else {
        // Add a 👍 to the current row
        myOutputValue += '👍';
      }

      innerCounter += 1;
    }
    // Insert a line break to start a new row
    myOutputValue += '<br>';
    outerCounter += 1;
  }
  return myOutputValue;
};
```

#### Q: At a high level, how does this code work?

A: Two loops create a square emoji figure. The condition evaluates if the loops are at an edge. An edge is defined as: Beginning of either loop. End of either loop.&#x20;

#### Q: (_Enter the number 3_) What is the value of `outerCounter` and `innerCounter` when the program draws the top middle fist? Use the debugger to find that value.

#### Q: (_Enter the number 5_) What is the result of each conditional statement the first time the loop runs? (_Use the debugger to find the value._)

A:&#x20;

```javascript
outerCounter == 0 // true
outerCounter == sideLength - 1 // false
innerCounter == 0 // true
innerCounter == sideLength - 1 // false
```

### [12.3: Project Deployment](broken-reference)

The starter code is setup in such a way that it can easily be put on the real internet. Encourage the students to share their game with their friends.

Use your own project as an example of where to find the GitHub repository settings.\
\
Another example of a deployed project is on the base blackjack repository: [https://rocketacademy.github.io/basics-blackjack/](https://rocketacademy.github.io/basics-blackjack/)

## In-Class Material

### [Day 11: Blackjack Redux and Debugger](../coursework/in-class-exercises/day-11-blackjack-redux-debugger/)

This exercise should prioritize getting those students who are stuck without a basic working game to understand how to move forward with their project.

## Post-Class: Begin Project

### [Project 3: Blackjack (More Comfortable)](../coursework/projects/project-3-blackjack.md#more-comfortable)

There is a bit more time to continue working on the project. It's not required to switch to working on the more comfortable tasks if the base version is not yet done.

## Look Ahead / Wrap-up

The next set of pre-class is a primer to coding outside the starter code. This material won't be reviewed in the next class meeting, but is intended to connect back together JavaScript code that would be written outside the context of the startercode. It also details how the starter code works.
