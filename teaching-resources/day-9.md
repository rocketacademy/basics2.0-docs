# Day 9: Card Logic

## Overview

This day ties together everything we've learned to create a data structure that should feel intuitive to the students- a deck of cards. The main concept is the connection of the idea of the deck _**pattern**_ and the syntax choices that have to be made in order to get the code to run.

The `makeDeck` function takes the specific patterns in a deck of cards- 4 repeating suits, 15 ranked numbers, and the special exception of face card names instead of numbers- and turns them into loops, conditionals and arrays of objects.

This idea of connecting together a pattern and data representation (a deck of cards) and JavaScript data structures and syntax (arrays, object, conditionals and loops) is at the heart of coding and writing algorithms. In this example code we've created a card deck creation algorithm. Certainly there are many more possible card deck creation algorithms that will give us the same result.

Remind the students that in order to move forward with the blackjack game, it's not strictly necessary to implement the `makeDeck` function or write it from scratch. Making a deck is just a demonstration of how to put together all the syntaxes we've seen so far.

## Pre-Class Material

Total Video Watch Time: **\~16 mins**

### [10.2: Card Deck Generation with Loops](../modules/3-logic-and-control-flow/10.2-card-deck-generation-with-loops.md)

```javascript
var makeDeck = function () {
  // Initialise an empty deck array
  var cardDeck = [];
  // Initialise an array of the 4 suits in our deck. We will loop over this array.
  var suits = ['hearts', 'diamonds', 'clubs', 'spades'];

  // Loop over the suits array
  var suitIndex = 0;
  while (suitIndex < suits.length) {
    // Store the current suit in a variable
    var currentSuit = suits[suitIndex];

    // Loop from 1 to 13 to create all cards for a given suit
    // Notice rankCounter starts at 1 and not 0, and ends at 13 and not 12.
    // This is an example of a loop without an array.
    var rankCounter = 1;
    while (rankCounter <= 13) {
      // By default, the card name is the same as rankCounter
      var cardName = rankCounter;

      // If rank is 1, 11, 12, or 13, set cardName to the ace or face card's name
      if (cardName == 1) {
        cardName = 'ace';
      } else if (cardName == 11) {
        cardName = 'jack';
      } else if (cardName == 12) {
        cardName = 'queen';
      } else if (cardName == 13) {
        cardName = 'king';
      }

      // Create a new card with the current name, suit, and rank
      var card = {
        name: cardName,
        suit: currentSuit,
        rank: rankCounter,
      };

      // Add the new card to the deck
      cardDeck.push(card);

      // Increment rankCounter to iterate over the next rank
      rankCounter += 1;
    }

    // Increment the suit index to iterate over the next suit
    suitIndex += 1;
  }

  // Return the completed card deck
  return cardDeck;
};
```

#### Q: Write some pseudocode for how to make a deck. There are no wrong answers.

A:

```javascript
// make each suit (loop 1)
//   make each card type (inner loop 2)

//     if it's a face card, change the name
//     add a single card to the deck array
```

#### Q: How does the above code work?

#### Q: What change would need to be made to create 104 cards? i.e., a double deck?

A:

```javascript
var card1 = {
  name: cardName,
  suit: currentSuit,
  rank: rankCounter,
};

// Add the new card to the deck
cardDeck.push(card1);

var card2 = {
  name: cardName,
  suit: currentSuit,
  rank: rankCounter,
};

// Add the new card to the deck
cardDeck.push(card2);
```

#### Q: For this code how would an emoji be added for each suit? (Don't change the suit name- add onto the object so it also has a `suitEmoji` key).

A:

```javascript
if (currentSuit === 'hearts') {
  var emojiSuit = '♥️';
} else if (currentSuit === 'diamonds') {
  var emojiSuit = '♦️';
} else if (currentSuit === 'spades') {
  var emojiSuit = '♠️';
} else if (currentSuit === 'clubs') {
  var emojiSuit = '♣️';
}

var card = {
  name: cardName,
  suit: currentSuit,
  rank: rankCounter,
  emojiSuit: emojiSuit,
};

// Add the new card to the deck
cardDeck.push(card);
```

## In-Class Material

### [Day 9: Moar Cards](../coursework/in-class-exercises/day-9-moar-cards/)

This in-class exercise creates different variations of high card. This will hopefully help the students warm-up to working on card games so that they are better prepared for doing the blackjack project.

## Wrap-up / Look Ahead

Day 10 pre-class material is a longer video (\~60 minutes)- a walk through of building a simple card game, and how to think through all of the logic involved with moving the cards around given the game rules. Hopefully hearing some of the syntax and logic decisions needed to implement a game will help refine the students' own decision making process. Encourage students to watch it at half or double speed or more than once if it helps.
