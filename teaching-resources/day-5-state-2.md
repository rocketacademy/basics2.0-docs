# Day 5: State 2

## Overview

Many students ask the natural question, how can I write my program to deal with the case that the user types in something that doesn't make sense? In this section we reviewed using some conditionals to help deal with some of these cases. We introduced the important JavaScript topic of language _**data types**_ and how to _**type cast**_ a value (change it from one value type into another).

This day adds a new way to use globals together with conditionals to create "modes". Note this isn't a programming or computer science topic, but just a way to describe this use of globals and conditionals together. Modes then allow the program to accept totally different data depending on the global game mode, i.e, the `input` variable can represent a string when the mode says `input` is the user's name, and it can represent a dice roll number when the mode says `input` represents a number. This is another expansion of the _volume_ of data our programs can deal with.

For this day, instead of an in-class exercise that explicitly deals with the pre-class material the students will review each other's code. When learning to code (or generally to increase your coding knowledge) it is important to read code in addition to writing code.

## Project Due

[Project 1.5: Scissors Paper Stone 2](../coursework/projects/project-1-scissors-paper-stone/project-1-scissors-paper-stone-part-2.md)

## Pre-Class Material

Total Video Watch Time: **\~17 mins**

### [8.3: Input Validation](../modules/3-logic-and-control-flow/8.3-input-validation.md)

### Number

```
'444';
444
```

#### Q: What is the difference between line 1 and 2?

A: One is a string type, the other is a number type.

#### Q: What things can we do with line 1 (string) values that we can't do with line 2 (number) values and vice versa?

A: Numbers can do math operations. Strings can be combined together `"cats" + "dogs"`. Strings can be changed to upper and lowercase `"papaya".toUpperCase()`

### NaN

```
444 * 'papaya';
444 * 2;
```

#### Q: (Run these in the dev tools console). What value is the result of each of these statements?

A: 1) NaN. 2) 888

#### Q: Why do we get these values?

A: We wrote code for a math operation that does not result in a number. The other is a number value so multiplication works fine.

```javascript
var main = function (input) {
  var miles = Number(input);

  console.log('is NaN: ' + Number.isNaN(miles));

  if (Number.isNaN(Number(input))) {
    return 'sorry please enter a number.';
  }

  var kilometers = miles * 1.6;
  var myOutputValue = 'Your input in kilometers is: ' + kilometers;
  return myOutputValue;
};
```

#### Q: What does the above code do?

A: Checks what the user typed to make sure they typed a number. If they didn't, let them know.

#### Q: Is there anything better in the above code about doing return on line 8 instead of doing else?

A: This "early return" code might be easier to read because the logical flow of the program doesn't progress below the condition if it's true.

In the version with the else you have to indent the main part of the program. In general it's easier to read code that is refactored to be less indented (for instance in an extreme example you might have to nest 10 times. one condition inside another, inside another, etc.)

### [8.2: Program State for Game Modes](../modules/4-scope/8.2-program-state-for-game-modes.md)

#### Example 1

```javascript
var mode = 'green';

var main = function (input) {
  if (input == 'greenmode') {
    mode = 'green';
  } else if (input == 'bluemode') {
    mode = 'blue';
  }

  var myOutputValue =
    'A fool sees not the same tree that a wise man sees. -William Blake';

  if (mode == 'blue') {
    myOutputValue =
      'The sea, once it casts its spell, holds one in its net of wonder forever. -Jacques Cousteau';
  }

  return myOutputValue;
};
```

#### Q: What are program "modes"?

A: Modes are a way we can write code so that the `main` function can do more than one set of things.

#### Q: When we run the above program and only click submit (don't type anything), what appears in the grey box? Which part of the code runs?

A: "A fool sees not the same tree that a wise man sees. -William Blake" appears in the grey box. None of the other conditions is true.

#### Q: If `bluemode` is typed in (and submit clicked), what gets displayed in the grey box? Which lines of code run?

A: 'The sea, once it casts its spell, holds one in its net of wonder forever. -Jacques Cousteau' appears in the grey box. The condition on line 6 is true. This sets the global mode variable. Then the condition on line 13 is true as well. Then the Jacques Cousteau quote appears.

#### Q: (switch modes a few more times). Ask the students to predict what the mode value will be when typed in the console before the submit button is clicked.

#### Q: (refresh the page) What happens if 'blue' is typed in and submitted?

A: This is a trick question because the code does not look to match the value 'blue' to the user input. It does look for that value in the global variable, though.

#### Q: Right now an english description of what the program does might be: "When the button gets clicked show the appropriate quote. If the mode switching word is typed in, change the mode and show that mode's quote."

#### What change would we make to the code if we wanted the behaviour to be: "When the button gets clicked show the appropriate quote. If the mode switching word is typed in, change the mode. Show that mode's quote the next time the button gets clicked."

A: We can move the conditions that check the user input to _**after**_ the condition that looks for the mode global. The pseudo code might look like:

```javascript
// set the default green message

// if the mode is blue
// set the blue message

// see if we are changing to green mode
// change mode
// see if we are changing to blue mode
// change mode

// return the message
```

#### Example 2

```javascript
var currentGameMode = 'waiting for user name';
var bankRoll = 10;
var userName = '';

var rollDice = function () {
  var randomDecimal = Math.random() * 6;
  var randomInteger = Math.floor(randomDecimal);
  var diceNumber = randomInteger + 1;
  return diceNumber;
};

var playDiceGame = function (userName, userGuess) {
  var message = '';

  // dice game logic
  var randomDiceRoll = rollDice();
  message =
    userName +
    ' you lost! you guessed: ' +
    userGuess +
    'you rolled: ' +
    randomDiceRoll +
    ' current bank roll: ' +
    bankRoll;

  if (userGuess == randomDiceRoll) {
    bankRoll = bankRoll + 1;
    message =
      userName +
      ' you won! you guessed: ' +
      userGuess +
      'you rolled: ' +
      randomDiceRoll +
      ' your current bank roll: ' +
      bankRoll;
  }

  return message;
};

var main = function (input) {
  var myOutputValue = '';

  if (currentGameMode == 'waiting for user name') {
    // set the name
    userName = input;

    // now that we have the name, switch the mode
    currentGameMode = 'dice game';

    myOutputValue = 'Hello ' + userName;
  } else if (currentGameMode == 'dice game') {
    myOutputValue = playDiceGame(userName, input);
  }

  return myOutputValue;
};
```

#### Q: (Run the above in the browser). For the above code begin with the `main` function and describe how the code works. (Type in a name and prompt the student to describe what happens in the second and third click as well).

#### Q: What are the reasons why the code has a `playDiceGame` function?

A: Rearranging the code so that the mode conditions are more readable, abstracting away a functionality of one game mode into its own named part.

## In-Class Material

### [Day 5: Scissors Paper Stone Redux](../coursework/in-class-exercises/day-6-loops/day-5-scissors-paper-stone-redux.md)

## Code Review - Individual Review

### Setup

#### 0) Have all the code pushed up to GitHub

For this section, especially because it's the first time students have done a pull request, they may not all be on the same page.

The ideal case would be to have everyone ready to begin the exercise, but it may take some students a few minutes to complete the push. (For this exercise, they don't need to complete the pull request, only the push).

Ideally the timer for the reading section would start after everyone is able to clone. But maximum total time for this should be around 25 mins.

If the students want help to fix something in their code, just tell them to push their broken version so that they can work on it together in pairs. Try not to fix any student's code during this silent reading time.

If there is a single person have them read one person in a pair's code (don't have anyone in the pair read their code). Put all three in a breakout room to discuss. When they are done discussing, move the single person into their own room. This is because it is difficult for three people to actually code together.

### Read (Individual) (Up to 25 mins Incl. Step 0)

1\) Clone Partner's Code

2\) Run Partner's Code

3\) Read Partner's Code

4\) Edit Partner's Code

Encourage the students to use all the tools at their disposal to investigate and understand the code. Reiterate that this is just a copy so don't be afraid of making changes that break things in order to figure out how something works.

### Breakout Rooms

Put the students in their breakout room pairs.

5\) Discuss

6\) Work on Features

## Post-Class: Begin Project

[Project 2: Beat That!](../coursework/projects/project-2-beat-that.md)

## Look Ahead / Wrap Up

Next we're moving on to arrays, which further expand the data we'll use. We'll also see loops control flow, which execute code a given number of times. The meeting after that, we'll combine the two together.
