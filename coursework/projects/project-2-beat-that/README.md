# 🎲 Project 2: Beat That!

## Introduction

Create a version of the Beat That dice game in your CodeSandbox, where players create the largest number they can by concatenating random dice roll digits. Read the rules for Beat That [here](https://www.activityvillage.co.uk/beat-that).

Have a look a some past student's project to visualise the game - and for inspiration :)

1. [Base](https://eggcodes.github.io/basics-beat-that/)
2. [Comfortable](https://averygan.github.io/basics-beat-that/)
3. [Super Comfortable](https://lim-jiahao.github.io/basics-beat-that/)

## Setup

You can find the project folder under `project2-beat-that` in your CodeSandbox.

## Base

### Requirements

1. There are 2 players and players take turns.
2. When a player clicks Submit, the game rolls 2 dice and shows the dice rolls, for example 3 and 6.
3. The player picks the order of the dice they want. For example, if they wanted the number 63, they would specify that the 2nd dice goes first. You can choose how the player specifies dice order.
4. After both players have rolled and chosen dice order, the player with the higher combined number wins.

### Example

Player 1 rolls 2 dice with dice rolls 3 for Dice 1 and 6 for Dice 2.

```
Welcome Player 1.
You rolled 3 for Dice 1 and 6 for Dice 2.
Choose the order of the dice.
```

Player 1 can pick either Dice 1 or Dice 2 as the first numeral of the combined number.

```
Player 1, you chose Dice 2 first.
Your number is 63.
It is now Player 2's turn.
```

Player 1 picked Dice 2 as the 1st numeral and Dice 1 as the 2nd, thus generating the combined number 63. Player 2 then rolls 2 dice and tries to generate a number greater than 63.

## Walkthrough

If you get stuck, or are unsure on how to start, Bryan will walk you through how to go from breaking down the problem to completion of the Base version of Beat That!

{% embed url="https://www.youtube.com/watch?v=JODUe_H0kmM" %}

## Comfortable

### Add some polish!

Your game is working as intended, now it's time to make it look good! We'll edit index.html to personalise our game.

At line 29 of index.html, try changing `background-color` to any [colour ](https://www.w3schools.com/colors/colors_names.asp)of your choice!

```
      #container {
        background-color: lightblue;
        margin: 40px auto;
        max-width: 800px;
        padding: 38px 31px;
      }
```

Add 1 or more [paragraphs](https://www.w3schools.com/html/html_paragraphs.asp) after line 64 with instructions on how to play Beat That! It can look something like this:

```
...

<body>
    <h1 id="header">Basics: Beat That! 🚀</h1>
    <div id="container">
      <p>Hello! Welcome to Beat That! Click submit to start the game.</p>
      <p>Create a two-digit number by selecting the order of your dice rolls.</p>
      <p>The player with the highest number wins! Good luck!</p>
      <p>Input:</p>
      <input id="input-field" />
      <br />
      <button id="submit-button">Submit</button>
      <p>Output:</p>
      <div id="output-div"></div>
    </div>

  ...
```

Having fun making your game look good? Feel free to explore more HTML and CSS on your own! Here are some resources:

- FreeCodeCamp's [basic HTML](https://www.freecodecamp.org/learn/responsive-web-design/#basic-html-and-html5) and basic [CSS tutorials](https://www.freecodecamp.org/learn/responsive-web-design/#basic-css)
- W3School's CSS [Tutorial](https://www.w3schools.com/css/default.asp) and [Reference](https://www.w3schools.com/cssref/default.asp).

## More Comfortable

Try implementing some, or a combination of, the following feature groups. Feel free to include any other additional features you think of.

{% tabs %}
{% tab title="Score" %}

#### Score

Keep score for each player. The score is the running sum of all numbers that player has generated so far. This means there is no permanent winner, only a temporary leader.

#### Leaderboard

When outputting game results in the output box, also output a leaderboard that lists the 2 players and their scores in decreasing order.
{% endtab %}

{% tab title="Lowest Combined" %}

#### Lowest Combined Number Mode

Add a game mode such that the player with the lowest combined number is the winner.

#### Auto-Generate Combined Number

Update the game to auto-generate the highest (or lowest) combined number from dice rolls. For example, for dice rolls `[6, 3]` in Lowest Combined Number mode, the game would auto-generate the combined number `36`.
{% endtab %}

{% tab title="Variable Dice and Players" %}

#### Variable Number of Dice

1. Create a new version of Beat That that rolls two or more dice per player.
2. At the beginning of each round, ask the players how many dice they would like to play with. Both players will roll the same number of dice each round.
3. Store each player's dice rolls in an array. When each player rolls dice, use a loop to place `n` dice roll values in that player's array, where `n` is the number of dice the players specified at the beginning of the round. Output each player's dice roll values.
4. Auto-generate the optimal combined number based on each player's dice rolls to determine the winner of that round.

#### Variable Number of Players

Allow more than 2 players at a time to play Beat That. At the beginning of the game, ask how many players would like to play. For a variable number of players, feel free to output the leaderboard in any order, because implementing the leaderboard in decreasing order requires advanced logic.
{% endtab %}

{% tab title="Knockout" %}

#### Knockout Mode

Create a mode where if there are more than 2 players, the game can match players against each other 1 at a time until there is 1 final winner. For example, if there are 4 players, the game might first match players 1 and 2. If player 1 wins, the game might then match players 1 and 3. The winner of that match would then play player 4, and the winner of that final round would be the ultimate winner.
{% endtab %}
{% endtabs %}

## Submit

{% content-ref url="../../../logistics/learning-environment/submitting-your-work.md" %}
[submitting-your-work.md](../../../logistics/learning-environment/submitting-your-work.md)
{% endcontent-ref %}

## Reference Solution

Please only refer to the reference solution after you have attempted the project. Note that there are many ways to implement the project and the reference solution is only 1 way.

1. [Base](https://github.com/rocketacademy/basics-beat-that/blob/base/script.js)
2. [Auto-Generate Combined Number](https://github.com/rocketacademy/basics-beat-that/blob/moreComfortable-autoGenerateCombinedNum/script.js) (includes Score, Leaderboard, and Lowest Combined Number Mode)
3. [Variable Number of Dice](https://github.com/rocketacademy/basics-beat-that/blob/moreComfortable-variableNumDice/script.js)
4. [Variable Number of Players](https://github.com/rocketacademy/basics-beat-that/blob/moreComfortable-variableNumPlayers/script.js)
5. [Knockout mode](https://github.com/rocketacademy/basics-beat-that/blob/moreComfortable-knockout/script.js)
