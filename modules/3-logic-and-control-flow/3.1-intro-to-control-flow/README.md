# 3.1: Intro to Logic and Control Flow

## Learning Objectives

By the end of this lesson, you should be able to:

* [ ] Understand that code does not always execute linearly and why.
* [ ] Explain what Control Flow is in your own words.
* [ ] Identify statements and operators we can use to manipulate control flow.
* [ ] Know how logic is used to make programs more complex.

{% embed url="https://www.youtube.com/watch?v=5Oz3bV-m78s" %}

## Introduction

### What is Control Flow?

In programming, "[control flow](https://en.wikipedia.org/wiki/Control\_flow)" refers to the order functions and statements are executed in a computer program.

Code is usually run sequentially from the first line in the file to the last line. However, certain structures such as [functions](../../2-structuring-and-debugging-code/2.3-functions/2.3.1-functions.md), [conditionals](../3.2-conditionals/) and [loops](../3.4-loops/3.4.1-while-loops.md) may alter this sequential flow, affecting the order of execution.

### What is Logic?

So far our apps have always performed the _same operations_, no matter the input. The next level of complexity is to create programs that perform _different_ operations, depending on the input.

Programming logic is the ability of the computer to **make decisions** based on input data. \
\
We'll be using the JavaScript logic syntax, the `if, else if, else` conditions. \
This allows us selectively run different blocks of logic under different conditions.

This can be used to test values that the users are typing in. Depending on what the user types, we can program different outputs to be displayed in the grey box.

## Random Dice Rolls

Let's recap Module 2: Functions by building a program that generates random dice numbers. We will be using this Dice Rolling function as a base to explore Logic and Control Flow for the rest of this Module.

### Random Number Generation

To simulate dice rolls, we first need random number generation. JavaScript can produce random numbers using a built-in "**library**" called [`Math`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Math) (case-sensitive). `Math` contains functions that perform common and helpful math operations. One of those functions is `Math.random`.

```
var myRandomValue = Math.random();
```

Calling `Math.random` returns a random decimal number between 0 and 1, inclusive of 0 and exclusive of 1. Note that `Math.random()` is a function that does not take in any input. Since we wish to simulate dice with numbers between 1 to 6 inclusive, we have to manipulate the randomly-generated number to get what we want.

To convert our random number to a valid dice roll value, we'll use another `Math` function: `Math.floor`. We will follow the random integer generation example [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Math/random) to use `Math.floor` to convert decimals to integers.

With `Math.random` and `Math.floor`, we can make a function that produces any random integer from 0 to a provided `max` number:

```javascript
var getRandomInteger = function (max) {
  // Generate a decimal from 0 through max + 1.
  // This decimal will be inclusive of 0 and exclusive of max + 1.
  var randomDecimal = Math.random() * (max + 1);

  // Remove the decimal with the floor operation.
  // The resulting integer will be from 0 through max, inclusive of 0 and max.
  var resultInteger = Math.floor(randomDecimal);

  return resultInteger;
};
```

### Dice Roll Program Logic

Since we wish to build a program that generates random dice numbers, we can customise `getRandomInteger` to always return an integer from 1 to 6. We call the new function `rollDice`.

```javascript
var rollDice = function () {
  // Generate a decimal from 0 through 6, inclusive of 0 and exclusive of 6.
  var randomDecimal = Math.random() * 6;

  // Remove the decimal with the floor operation.
  // This will be an integer from 0 to 5 inclusive.
  var randomInteger = Math.floor(randomDecimal);

  // Add 1 to get valid dice rolls of 1 through 6 inclusive.
  var diceNumber = randomInteger + 1;

  return diceNumber;
};
```

Let's put this together with our `main` function, and personalise our output. Whenever the Submit button is clicked, we will print the most recent dice roll number.

```javascript
var main = function (input) {
  // Generate a random dice number
  var randomDiceNumber = rollDice();

  // Personalise the output
  var myOutputValue = 'You just rolled a ' + randomDiceNumber + '!';

  // Return and print output.
  return myOutputValue;
};
```

### ****
