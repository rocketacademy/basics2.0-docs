# Day 10: Coding Strategies

## Overview

This day is a sample implementation of a complete game, again, without adding any new syntax, this section models how to actually code something using all the syntaxes already covered. This section talks about faking cards, debugging and, at the beginning of a project, how to start thinking about the code that needs to be written.

Reiterate to the students how important the process and approach to the code and what was covered in [Coding Strategies](../course-logistics/tips-and-tricks/coding-strategies.md) is important.

## Pre-Class Material

Total Video Watch Time: **\~60 mins**

### [10.3: War Card Game Sample Implementation](../9-javascript-objects/10.3-card-game-example-war.md)

#### Q: Why do we want to control which cards get dealt from the deck?

A: Because we would never be able to test all the code if it was random.

#### Q: Name another project or exercise where controlling the outcome is _necessary_ in order to test the code.

A:

* The Lucky 11 exercise from day 2.
* Testing if cards are equal in High Card.
* Getting Blackjack.

#### Q: What are the two things to look for with console.log?

A:&#x20;

1. Does the program reach that line?
2. What is the value at that line?

#### Q: What does `unshift` do?

A: Puts something at the front of an array.

#### Q: How would this rule change be implemented in the code? When there is a war, if any of the players gets a 6, they win the war.

A: From line 186:

```javascript
if (playerFaceUp.rank == 6) {
  playerHand = addArray(warCards, playerHand);
} else if (computerFaceUp.rank == 6) {
  computerHand = addArray(warCards, computerHand);
} else if (playerFaceUp.rank > computerFaceUp.rank) {
  // Set cardsEqual to false to end the loop.
  cardsEqual = false;
  // Add all war cards to bottom of player hand.
  playerHand = addArray(warCards, playerHand);
} else if (playerFaceUp.rank < computerFaceUp.rank) {
  // Set cardsEqual to false to end the loop.
  cardsEqual = false;
  // Add all war cards to bottom of computer hand.
  computerHand = addArray(warCards, computerHand);
}
```

#### Q: What would happen if we moved the condition around, would the code still work the same? Why or why not?

```javascript
if (playerFaceUp.rank > computerFaceUp.rank) {
  // Set cardsEqual to false to end the loop.
  cardsEqual = false;
  // Add all war cards to bottom of player hand.
  playerHand = addArray(warCards, playerHand);
} else if (playerFaceUp.rank < computerFaceUp.rank) {
  // Set cardsEqual to false to end the loop.
  cardsEqual = false;
  // Add all war cards to bottom of computer hand.
  computerHand = addArray(warCards, computerHand);
} else if (playerFaceUp.rank == 6) {
  playerHand = addArray(warCards, playerHand);
} else if (computerFaceUp.rank == 6) {
  computerHand = addArray(warCards, computerHand);
}
```

A: It would only look at those conditions if the cards were equal, so it wouldn't work. The last condition would never be executed, because the player card is always the same as the computer card.

#### Q: How would the rule be stated for the code the way it currently is above?

A: If, during a war, both players draw a six, the human player wins.

## In-Class Material

### [Day 10: Chat Bot](../in-class-exercises/day-10-chat-bot.md)

This exercise introduces one new object syntax that will be needed in order to complete it. Demonstrate this for the students.

#### Object Square Bracket Syntax

```javascript
var person = {
  name: 'Fred',
  height: 1.7,
};

// these are equivalent
console.log(person.name);
console.log(person['name']);
```

#### Object Key Substitution

```javascript
var person = {
  name: 'Fred',
  height: 1.7,
};
var keyName = 'height';

// these are equivalent
console.log(person.height);
console.log(person[keyName]);
// this wont work!
console.log(person.keyName);
```

#### Dynamic Object Key

```javascript
var person = {
  name: 'Fred',
  height: 1.7,
};

var main = function (input) {
  var myOutputValue = person[input];
  return myOutputValue;
};
```

#### Q: What value will be in the grey box if "apples" is typed in?

A: `undefined`.

### Wrap-Up / Look Ahead

We've gone deeper with cards, coding processes and objects. Next we'll cover one last thing, which is the ability to see _**into**_ our code with the Chrome dev tools with the debugger. The debugger is the most granular tool we can use to analyze what our code is doing. As we covered in [Coding Strategies](../course-logistics/tips-and-tricks/coding-strategies.md), building a correct mental model of how the code works during debugging is the key task to fixing errors. Sometimes we may need to look at a particular value in order to do that.
