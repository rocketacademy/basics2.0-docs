---
description: ✂️📃💎🤩
---

# Project 1: Scissors Paper Stone (Part 2)

## Introduction

Part 2 assumes we have learned about global variables, and the More Comfortable section assumes we know how to use [global varaibles](../../../modules/4-scope/8.1-program-lifecycle-and-state.md#global-variables) as game modes. We'll now update our SPS Part 1 to support [game states](../../../modules/4-scope/8.2-program-state-for-game-modes.md#global-state-for-app-modes).

If you completed the [Base features of SPS Part 1](project-1-scissors-paper-stone-part-1.md#base) but didn't finish the More Comfortable section, please complete Base for SPS Part 2 before going back to attempting More Comfortable for both parts.

## Past Projects

Take a look at past projects by previous Basics students to visualise how the full game can look like.

1. [Muk-jji-ppa](https://lim-jiahao.github.io/basics-scissors-paper-stone/)
2. [Regular and Reverse](https://averygan.github.io/basics-scissors-paper-stone/)

## Base

### Win-Loss Record

Add [state](../../../modules/4-scope/8.1-program-lifecycle-and-state.md) to your program such that it keeps track of the number of times the user has won and the number of times the computer has won. Output this win-loss record in a format you like in the program output. You can also output the number of draws and/or each party's winning percentage if you'd like.

### User Name

To make this game more personal, add a feature to collect the user's name as the first input after the page loads. We can prompt the user to enter their name first by adding to the page's HTML. Once the user submits their name, the program can return output to prompt the user to start playing Scissors Paper Stone by entering one of the 3 objects. Use the user's name to personalise win-loss record and other relevant output.

### Formatting

Make the output of your game look nice. You can use the string `'<br>'` to create [new lines](https://www.w3schools.com/TAGS/tag\_br.asp) in the output. Add the user name and the win/loss record. Format a message depending on how well the player is doing:

```
The computer chose scissors ✂️.
You chose paper 🗒.

You lose! Bummer.

So far Kai, you've been winning 5/7 turns. Pretty good!
```

## More Comfortable

There is no need to implement all the different features sequentially in one version of your game. Feel free to choose what you find interesting and appropriately challenging and implement only that.

### Reverse Game Mode

You decide to prank your friends and create an SPS game mode where the rules are reversed: scissors beat stone, stone beats paper, and paper beats scissors. Create _**a game mode**_ where if a user types in "reverse", it reverses the SPS rules.&#x20;

### Korean Scissors Paper Stone

The following is adapted from [Wikipedia](https://en.wikipedia.org/wiki/Rock\_paper\_scissors#Adapted\_rules):

> In Korea, a two-player upgraded version exists by the name [muk-jji-ppa](https://en.wikipedia.org/wiki/Muk-jji-ppa). After showing their hands, the player with the winning throw shouts "muk-jji-ppa!" upon which both players throw again. If they throw differently (for example, rock and paper, or paper and scissors), whoever wins this second round shouts "muk-jji-ppa!" and thus the play continues until both players throw the same item (for example, rock and rock), at which point whoever was the last winner becomes the actual winner.

Update your program state such that it can keep track of the most recent winner, and update the program logic to declare the most recent winner the ultimate winner when there is a draw.

### Versions

Allow the player to select if they want to play normal or Korean versions of the game.

### Computer vs. Computer

Add a mode that lets the computer choose for you on each turn.

### Further Variations

Implement other variations to the game as described [here](https://en.wikipedia.org/wiki/Rock\_paper\_scissors#Variations). The user can select which variation they would like to play.

## Submit

Share your work with your Section mates for peer-learning, and with your SLs for review. In your Section Slack channel:

1. Title a new code snippet "SPS Part 2"
2. Copy code from `script.js` into the code snippet
3. Include the following message, filled in:
   1. How many hours did you spend on this assignment?
      1. What part of the assignment did you spend the most time on?
   2. What is one error and/or error message you received while working on this assignment, and how did you solve the error?
   3. How comfortable did you feel with this assignment? (1-5):
   4. Is there anything in this code that you feel pleased about?
   5. What's one aspect of your code you would like specific, elaborate feedback on?

## Reference Solution

The reference solution implements the Base functionality for both SPS Parts 1 and 2. Please only refer to the reference solution after you have attempted the project. Note that there are many ways to implement the project and the reference solution is only 1 way.

[View the reference solution ](https://github.com/rocketacademy/basics-scissors-paper-stone/tree/part2-inclMoreComfortable)for SPS-Part2 (up till More Comfortable).
