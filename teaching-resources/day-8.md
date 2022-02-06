# Day 8: Objects

## Overview

With objects we get to abstract and create our own definitions of what one value / variable / piece of data can be. In the case of our card example, we can choose to have integers \*and\* strings make up the definition of one card. We're creating an abstraction of what a card is, and also including data in our card that we'll need to calculate and display things. The exercise of defining object keys and data types is fundamentally an exercise in abstraction and encapsulation.

It's also true that an object represents any tabular data- rows in a spreadsheet, names in an address book- most data in the real world that computer programs deal with has this tabular structure.

Students will sometimes be confused about the idea of "holding" different types of data in a single variable value, that is, they won't be sure when to use an array or object. Refer back to the table in 10.1 to decide this.

Sometimes assignment into a given key can look confusing: `card.rank = newRank;` or assigning a new key: `card.newKey = 99;` It may not be totally clear to students that square brackets in objects are different from square brackets for arrays.

## Project Due

[Project 2: Beat That!](../coursework/projects/project-2-beat-that.md)

## Pre-Class Material

Total Video Watch Time: **\~15 mins**

### [10.1: JavaScript Objects](../modules/1-data-structures-and-manipulation/1.4-javascript-objects.md)

```javascript
var cardDeck = ['nine of hearts', 'ten of hearts', 'jack of hearts'];
```

#### Q: For the code example above, what would be the pseudocode for getting the total of the ranks?

A:

```
// loop over the array
    // break apart the string to get the first word
    // evaluate the first word
    // is it "one" add the number 1
    // is it "two" add the number 2
    // etc., until "king"
```

#### Q: What other card-like values could we use to represent the card deck? Are there issues with these other implementations?

A: Array of numbers: `var cardDeck = [9,10,10];` With this array we wouldn't know what the suit or name of the card is.

#### Q: Why does an object solve these issues of representing a "card"?

A: We can keep each individual value that makes up the idea of a card separate, but together in one card value.

```javascript
var cardDeck = [
  {
    rank: 1,
    suit: 'heart',
    name: 'one',
  },
  {
    rank: 2,
    suit: 'heart',
    name: 'two',
  },
];
```

#### Q: (Run the above code to create the array). How can the name of the second card be accessed?

A: `cardDeck[1].name`

#### Q: How can the suit of the first card be changed to diamonds?

A: `cardDeck[0].suit = 'diamonds';`

#### Q: How can we add a '`temperature`' key that equals `99` to the first card? (this is just an example of adding a new random key).

A: `cardDeck[0].temperature = 99;`

```javascript
// Initialise the card deck representation as an array of objects
var deck = [
  {
    name: 'ace',
    suit: 'hearts',
    rank: 1,
  },
  {
    name: '2',
    suit: 'hearts',
    rank: 2,
  },
  {
    name: '3',
    suit: 'hearts',
    rank: 3,
  },
  {
    name: '4',
    suit: 'hearts',
    rank: 4,
  },
  {
    name: '5',
    suit: 'hearts',
    rank: 5,
  },
  {
    name: '6',
    suit: 'hearts',
    rank: 6,
  },
  {
    name: '7',
    suit: 'hearts',
    rank: 7,
  },
  {
    name: '8',
    suit: 'hearts',
    rank: 8,
  },
  {
    name: '9',
    suit: 'hearts',
    rank: 9,
  },
  {
    name: '10',
    suit: 'hearts',
    rank: 10,
  },
  {
    name: 'jack',
    suit: 'hearts',
    rank: 11,
  },
  {
    name: 'queen',
    suit: 'hearts',
    rank: 12,
  },
  {
    name: 'king',
    suit: 'hearts',
    rank: 13,
  },
  {
    name: 'ace',
    suit: 'diamonds',
    rank: 1,
  },
  {
    name: '2',
    suit: 'diamonds',
    rank: 2,
  },
  {
    name: '3',
    suit: 'diamonds',
    rank: 3,
  },
  {
    name: '4',
    suit: 'diamonds',
    rank: 4,
  },
  {
    name: '5',
    suit: 'diamonds',
    rank: 5,
  },
  {
    name: '6',
    suit: 'diamonds',
    rank: 6,
  },
  {
    name: '7',
    suit: 'diamonds',
    rank: 7,
  },
  {
    name: '8',
    suit: 'diamonds',
    rank: 8,
  },
  {
    name: '9',
    suit: 'diamonds',
    rank: 9,
  },
  {
    name: '10',
    suit: 'diamonds',
    rank: 10,
  },
  {
    name: 'jack',
    suit: 'diamonds',
    rank: 11,
  },
  {
    name: 'queen',
    suit: 'diamonds',
    rank: 12,
  },
  {
    name: 'king',
    suit: 'diamonds',
    rank: 13,
  },
  {
    name: 'ace',
    suit: 'clubs',
    rank: 1,
  },
  {
    name: '2',
    suit: 'clubs',
    rank: 2,
  },
  {
    name: '3',
    suit: 'clubs',
    rank: 3,
  },
  {
    name: '4',
    suit: 'clubs',
    rank: 4,
  },
  {
    name: '5',
    suit: 'clubs',
    rank: 5,
  },
  {
    name: '6',
    suit: 'clubs',
    rank: 6,
  },
  {
    name: '7',
    suit: 'clubs',
    rank: 7,
  },
  {
    name: '8',
    suit: 'clubs',
    rank: 8,
  },
  {
    name: '9',
    suit: 'clubs',
    rank: 9,
  },
  {
    name: '10',
    suit: 'clubs',
    rank: 10,
  },
  {
    name: 'jack',
    suit: 'clubs',
    rank: 11,
  },
  {
    name: 'queen',
    suit: 'clubs',
    rank: 12,
  },
  {
    name: 'king',
    suit: 'clubs',
    rank: 13,
  },
  {
    name: 'ace',
    suit: 'spades',
    rank: 1,
  },
  {
    name: '2',
    suit: 'spades',
    rank: 2,
  },
  {
    name: '3',
    suit: 'spades',
    rank: 3,
  },
  {
    name: '4',
    suit: 'spades',
    rank: 4,
  },
  {
    name: '5',
    suit: 'spades',
    rank: 5,
  },
  {
    name: '6',
    suit: 'spades',
    rank: 6,
  },
  {
    name: '7',
    suit: 'spades',
    rank: 7,
  },
  {
    name: '8',
    suit: 'spades',
    rank: 8,
  },
  {
    name: '9',
    suit: 'spades',
    rank: 9,
  },
  {
    name: '10',
    suit: 'spades',
    rank: 10,
  },
  {
    name: 'jack',
    suit: 'spades',
    rank: 11,
  },
  {
    name: 'queen',
    suit: 'spades',
    rank: 12,
  },
  {
    name: 'king',
    suit: 'spades',
    rank: 13,
  },
];

// Shuffle the deck and save it in a new variable shuffledDeck
// to communicate that we have shuffled the deck.
var shuffledDeck = shuffleCards(deck);

var main = function (input) {
  // Draw 2 cards from the top of the deck
  var computerCard = shuffledDeck.pop();
  var playerCard = shuffledDeck.pop();

  // Construct an output string to communicate which cards were drawn
  var myOutputValue =
    'Computer had ' +
    computerCard.name +
    ' of ' +
    computerCard.suit +
    '. Player had ' +
    playerCard.name +
    ' of ' +
    playerCard.suit +
    '. ';

  // Compare computer and player cards by rank attribute
  // If computer card rank is greater than player card rank, computer wins
  if (computerCard.rank > playerCard.rank) {
    // Add conditional-dependent text to the output string
    myOutputValue = myOutputValue + 'Computer wins.';
    // Else if computer card rank is less than player card rank, player wins
  } else if (computerCard.rank < playerCard.rank) {
    myOutputValue = myOutputValue + 'Player wins!';
    // Otherwise (i.e. ranks are equal), it's a tie
  } else {
    myOutputValue = myOutputValue + "It's a tie.";
  }

  // Return the fully-constructed output string
  return myOutputValue;
};
```

#### Q: How does the above code work?

#### Q: What would need to change so that the highest card _**loses**_ instead?

A: Reverse the comparison operators.

#### Q: What would need to be changed so that an emoji (♣️) could be displayed in addition to the suit name?

A: Add each emoji to each card object. (This is inefficient but would make sense if the cards are being created in a loop).

```javascript
{
    name: 'two',
    rank: 2,
    suit: 'clubs',
    suitEmoji: '♣️'
}
```

## In-Class Material

[Day 8: Beat That Redux](../coursework/in-class-exercises/day-9-moar-cards/day-8-beat-that-redux.md)

## Post-Class: Begin Project

### [Project 3: Blackjack](../coursework/projects/project-3-blackjack.md)

This card game is the final project, the accumulation of everything we've learned. The core of this project is a card game that has some complexity to it, so we've given some instructions that should help break it down and make it easier.

With any complex project it's important to break down a large goal into smaller sub-goals. This can be very challenging for new programmers, so this has been done ahead of time. It is _**very, very, strongly recommended**_ to follow the order of work that we've specified in the project page.

Note that we've structures the schedule so that there is a peer-review code session _**before**_ the project deadline, so that you can get some feedback on your work and continue to work on the game.

## Wrap-Up / Look Ahead

This section is the end of the main JavaScript syntaxes we'll cover. There are some others we haven't touched on, but the ones we have covered are the ones present in almost all programming languages, and are the most important. We now have all the most important tools needed to build almost any program.

Moving forward from here we'll be covering more details on how to build our programs, doing some more complex example programs and more on how to debug, but we won't be introducing any new major JavaScript syntaxes.
