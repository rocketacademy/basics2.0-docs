# Day 3: Program State

## Introduction

Today we will practice using global variables to store and change the state of the program..

See an example of all problems [**here**](https://rocketacademy.github.io/basics-starter-code/day4/index.html).

**Please switch driver and navigator each exercise, and share your solutions with your partner.**

{% content-ref url="../../logistics/learning-environment/pair-programming-instructions.md" %}
[pair-programming-instructions.md](../../logistics/learning-environment/pair-programming-instructions.md)
{% endcontent-ref %}

## Knowledge Check

Before you begin, check that you and your partner can answer the following:

* [ ] Why use global variables?
* [ ] What is the difference between global and local variables?
* [ ] Can a global variable be accessed or manipulated within a function?
* [ ] Can a variable declared in `main` be accessed or manipulated in a different helper function?

## Base

{% tabs %}
{% tab title="Secret Word" %}
**Secret Word**

Create a game where a player must correctly guess secret words to win.

The computer chooses a random word from a set of three words. Feel free to use whatever words you'd like, but we will be using the words _"banana"_, _"chisel"_, and _"faucet"_.

To win the game the player must guess correctly **twice** in **total;** but is allowed to guess wrongly in between their two correct guesses.

For each guess, output all information such as the guessed word, the secret word, and how many correct guesses the player still needs until she wins.

#### Comfortable

**Secret Word Twice in a Row**

Update Secret Word with an additional rule: The player must guess correctly twice _in a row_ to win.

**Secret Word X in a Row**

Update Secret Word game such that the number of times the player needs to guess correctly in a row changes between rounds.

We define "round" as all gameplay until a player wins. The number of times the player needs to guess correctly is a number from 2 to 4, randomly chosen at the start of the round.

When the player wins, the computer updates the number of times the player needs to guess correctly in a row for the next round.

Consider using [input control ](../../modules/3-logic-and-control-flow/3.3-boolean-operators/3.3.3-boolean-and-not.md#code-control)to test your logic.

#### More Comfortable

**Secret Word Twice in a Row 2**

Update Secret Word with the following additional rules.

1. The player must guess correctly twice in a row to win
2. Secret words cannot be repeated 2 guesses in a row. E.g. the secret word cannot be "banana" for 2 player guesses in a row. If the secret word for the 1st guess were "banana", the secret word for the 2nd guess would have to be either "chisel" or "faucet".
{% endtab %}

{% tab title="Dice" %}
**Dice Within**

Create a new version of our Coding Basics dice game (where the player guesses the dice roll) that randomly becomes easier or harder. At the beginning of the game and each time the player wins, the computer selects a random number from 1 to 3, which we call the "within number". If any of the player's guesses fall within the dice roll plus or minus the within number, the player wins.

For example: the app randomly chooses 3 as the within number. The player can guess within 3 of the dice roll to win the game. The player guesses 2 and the dice roll is 5. The guess is within 3 of the dice roll so the player wins the game. At this point, the computer adjusts the difficulty of the game by choosing a new within number.

**Dice Within with 2 Dice**

Update our dice game to include an additional dice. With each player guess, the computer rolls 2 dice. If the player guess is within either of the 2 dice rolls plus or minus the within number, the player wins.

**Dice 4D**

Update our dice game to allow the player to play a round of 4D every 2 times the player wins the dice roll guess. Use [input control ](../../modules/3-logic-and-control-flow/3.3-boolean-operators/3.3.3-boolean-and-not.md#code-control)to verify our 4D game logic, that it is possible to win this 4D game.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Reminder: There is no need to complete all exercises on this page. Once comfortable with the concepts, feel free to move on to [Scissors Paper Stone: Part 2](../projects/project-1-scissors-paper-stone/project-1-scissors-paper-stone-part-2.md) You can always come back and attempt the additional problems when you are feeling _more comfortable._
{% endhint %}

## Reference Solution

[Here](https://github.com/rocketacademy/basics-starter-code-2.0/blob/day3/day03-program-state/in-class/script.js) is a reference solution for Day 3 exercises. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
