# Day 3: Logic 1

## **Overview**

Logic is the first day that we introduce real serious control flow. Some students will struggle to cope with this increase in complexity, not because the code is hard to understand but because understanding what code to write is much more difficult.

Remember that just logic in and of itself is actually a huge topic. This first day tries to leave out some of the complexities by leaving off certain syntax such as `else` and `else if`. It may be awkward to think about coding without these tools, but it may help the students to tackle the problems with less options and less possible code paths to deal with.

## Pre-Class Material

Total Video Watch Time: **\~40 mins**

### [6.1: Intro to Logic](../modules/3-logic-and-control-flow/3.2-conditionals/)

#### Overview

Introduces one basic conditional if statement with one equivalence operator inside.

We don't introduce things like what else can go in the conditional parens or things like else yet.

The code should be relatively intuitive here.

Students can sometimes get confused that block curly braces for functions work differently from conditional block curly braces (e.g. function scope).

#### Discussion Questions

```javascript
var main = function (input) {
  // Set a default value for myOutputValue
  var myOutputValue = 'hello world';
  // If input is our secret phrase, change the value of myOutputValue
  if (input == 'palatable papaya') {
    myOutputValue = 'hello friend';
  }
  // return myOutputValue as output
  return myOutputValue;
};
```

**Q: Make a change so that I see** _**hello friend**_ **when I type the number 333.**

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

**Q: Make sure students what the code does. No need to go into the details of Math.floor, etc. The most important thing to know is that the random number is from 1-6.**

**Q: How to make the number larger?**

A: Change multiplication on line 3.

```javascript
var main = function (input) {
  // Generate a random dice number
  var randomDiceNumber = rollDice();

  // Default output value is 'you lose'.
  var myOutputValue = 'you lose';

  // If input matches randomDiceNumber, update output.
  if (input == randomDiceNumber) {
    myOutputValue = 'you win';
  }

  // Return output.
  return myOutputValue;
};
```

#### Q: Make a change so that I win, unless I guessed the random number.

### [6.2: Pseudo Code, Boolean Or](../modules/3-logic-and-control-flow/3.3-boolean-operators/3.3.1-boolean-or.md)

#### Overview

Introduces the logical OR operator. Again, here with a single boolean operator there is a lot of inherent complexity, but we leave off a lot so that the code feels relatively intuitive.

This section also introduces _**pseudocode**_ as a way to bridge logical english sentences into running JavaScript code.

#### Discussion Questions

```javascript
if (
  randomDiceNumber + 1 == input ||
  randomDiceNumber == input ||
  randomDiceNumber - 1 == input
) {
  myOutputValue = 'you win';
}
```

**Q: Add the pseudocode comments to this code example.**

**Q: Does it matter what order the individual equivalence checks are in? Can we check for `number - 1 == input` first?**

A: With logical OR it does not matter. In english, \*any\* of the statements can be true in order for the condition block to run.

### [6.3: Boolean And and Not](../modules/3-logic-and-control-flow/3.3-boolean-operators/3.3.3-boolean-and-not.md)

#### Overview

This section covers three important topics: Boolean AND, boolean NOT, error testing conditionals with `console.log`.

#### Discussion Questions

#### Boolean Values

```javascript
var main = function (input) {
  // Generate a random dice number
  var randomDiceNumber = rollDice();

  // Default output value is 'you lose'.
  var myOutputValue = 'you lose';

  // If input matches randomDiceNumber, update output.
  var didUserWin = input == randomDiceNumber;

  console.log('boolean operation result: ' + didUserWin);

  if (didUserWin) {
    myOutputValue = 'you win';
  }

  // Return output.
  return myOutputValue;
};
```

#### Q: What is the difference between the above code and the original dice game example?

A: They both work the same. In this example I can see what is going to happen in the if because I am capturing and `console.log`ing the result of the boolean operation.

#### AND

```javascript
var main = function (input) {
  var randomDiceNumber1 = rollDice();
  var randomDiceNumber2 = rollDice();
  // The default output value is "you lose".
  var myOutputValue = 'you lose';
  // If the input matches both random dice numbers, output value is "you win".
  if (randomDiceNumber1 == input && randomDiceNumber2 == input) {
    myOutputValue = 'you win';
  }
  return myOutputValue;
};
```

#### Q: How would I add a third dice?

#### NOT

#### Q: Given the code above, how would I make it so that I win if I didn't guess correctly?

A: Change the equality `==` operator to not equal `!=`.

#### Snake Eyes

```javascript
var main = function (input) {
  var randomDiceNumber1 = rollDice();
  var randomDiceNumber2 = rollDice();
  // The default output value is "you lose".
  var myOutputValue = 'you lose';
  // If the input matches both random dice numbers, output value is "you win".
  if (
    randomDiceNumber1 == input &&
    randomDiceNumber2 == input &&
    !(randomDiceNumber1 == 1 && randomDiceNumber2 == 1)
  ) {
    myOutputValue = 'you win';
  }
  return myOutputValue;
};
```

#### Q: How can I test to make sure that getting snake eyes causes me to lose?

A: Hard code `rollDice` to return 1.

#### Q: Make a change to the code so I only win when I get snake eyes.

## In-Class Material

[Day 3: If Statements, Boolean Or, And](../coursework/in-class-exercises/day-2-if-statements-boolean-operations.md)

## Look Ahead / Wrap-up

Just the conditionals syntax in this day is a huge amount of possible complexity and the possibility space the code can explore is now exponentially larger compared to the previous day. The code can now decide things based on data. We'll continue to use conditionals to expand what our programs can do. Next is to introduce global values so that the program can evolve over time and can deal with more and more data as the user uses the program. Next time we'll also introduce the GItHub project submission workflow.

## Post-Class: Begin Project

Introduce the project. SPS is split into two parts. The second part will use global variables to keep track of game state.

Make sure everyone understands when the project is due.

[Project 1: Scissors Paper Stone (Part 1)](../coursework/projects/project-1-scissors-paper-stone/project-1-scissors-paper-stone-part-1.md)
