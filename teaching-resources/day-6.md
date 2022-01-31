# Day 6: Arrays, Loops 1

## Overview

This day is split between two subjects that we will be synthesized in the next meeting.

Arrays express the idea of a value made up of discrete composite values, in the way a week is composed of days, or a book of pages. This section introduces the array as a type of value. It doesn't introduce the code needed to iterate over an arbitrary sized array yet.

Loops are the last form of control flow to cover. It combines conditional syntax with the idea that the block repeats over and over. Note here how the JavaScript syntaxes are still building on each other.

We also cover coding strategies. The reason we don't cover this right away is so that the students get a chance to build programs that have a reasonable level of complexity in them. This section should hopefully allow them to reflect on the code they've written so far and understand how they can improve their process. Feel free here to add any points you struggled with in particular.

### Project

[Beat That](../projects/project-2-beat-that.md)

Remind the students to continue working on the Beat That project and submit a pull request before next Saturday's meeting.

## Pre-Class Material

Total Video Watch Time: **\~41 mins**

### [Coding Strategies](../course-logistics/tips-and-tricks/coding-strategies.md)

#### Discussion Questions

#### Q: What are the three ways to approach a problem? Describe which step you get stuck on the most so far.

A: 1) Understand the problem through language. 2) Strategize to prioritize problems. 3) Translate problem to JavaScript, use pseudocode.

#### Q: Describe one time that fixing an error updated your mental model / helped you understand your code and/or JavaScript better.

#### Q: What does deliberate practice mean to you? How are you implementing it in this course?

### [9.1: Arrays](../6-arrays-and-iteration/9.1-arrays.md)

#### Discussion Questions

#### Q: What is an array for?

A: Storing lists of data of the same kind or type.

#### Q: Do arrays always have to store the same data type?

A: It is valid syntax to put any kind of type into an array. But the concept of storing a list of data means that it should always be the same type.

```javascript
var letters = ['a', 'b', 'c'];
```

#### Q: (Paste the above code into the console). How would we access 'b'?

```javascript
letters[9];
```

#### Q: After defining letters as the previous example, what happens when we try to access an element that doesn't exist?

A: Trying to access an index that doesn't exist will give back the value `undefined`.

```javascript
// Store guesses in a global array that persists across Submits.
var guesses = [];
var main = function (input) {
  // Add the user's guess to the guesses array.
  guesses.push(input);
  // Generate a random dice number.
  var randomDiceNumber = rollDice();
  // Initialise output to communicate loss.
  // Output the record of all guesses regardless of loss or win.
  var myOutputValue = 'You lose. Your guesses: ' + guesses;
  // If the guess matches the dice roll, change output to communicate win.
  if (randomDiceNumber == input) {
    myOutputValue = 'You win. Your guesses: ' + guesses;
  }
  // Return output value.
  return myOutputValue;
};
```

#### Q: What does this code do?

(Note this code doesn't do a lot yet without a loop to get the data back out. Remind the students we'll be doing this next).

#### Q: `push` is the way we can put values in the array. How do we take them out?

A: `pop`

### [9.2: Loops](../6-arrays-and-iteration/9.2-loops.md)

```javascript
// Initialise a counter to 0.
var counter = 0;
// Set the while loop condition to continue when counter is less than 10.
while (counter < 10) {
  // Log hello with each iteration of the loop.
  console.log('hello ' + counter);
  // Increment the counter by 1 at the end of each loop iteration.
  counter = counter + 1;
}
```

#### Q: What does the above code do? (Have the student answer before pasting this code into the dev tools console).

```javascript
var main = function (input) {
  var myOutputValue = '';
  var counter = 0;
  // Continue the loop while counter is less than the input value
  while (counter < input) {
    // Add 1 "yes" to the output for every loop iteration.
    myOutputValue = myOutputValue + 'yes';
    counter = counter + 1;
  }
  return myOutputValue;
};
```

#### Q: What does the above code do?

#### Q: How can we have the above code example run the `console.log` 100 times?

#### Q: (Starting from the original code) What if we set the starting value of `counter` to two instead of zero? What happens if the user types in a value above two?

#### Q: (Starting from the original code) What if we increment the value of `counter` by three instead of one? On line 8: `counter = counter + 3;`

```javascript
var main = function (input) {
  var myOutputValue = '';
  var counter = 0;
  // Continue the loop while counter is less than the input value
  while (counter < input) {
    // If counter is less than 5, add "yes" to output
    if (counter < 5) {
      myOutputValue = myOutputValue + 'yes';
      // Otherwise, add "no" to output
    } else {
      myOutputValue = myOutputValue + 'no';
    }
    counter = counter + 1;
  }
  return myOutputValue;
};
```

#### Q: What does the above code do?

#### Q: What happens if the comparison is reversed? `if (counter > 5) {`

```javascript
var main = function (input) {
  var myOutputValue = '';

  var counter = 0;
  while (counter < input) {
    // If counter is even, add "yes" to output
    // The modulus (%) operator returns the remainder after division
    // If a number divided by 2 equals 0, we consider it even.
    if (counter % 2 == 0) {
      myOutputValue = myOutputValue + 'yes';
      // Otherwise, add "no" to output
    } else {
      myOutputValue = myOutputValue + 'no';
    }
    counter = counter + 1;
  }

  return myOutputValue;
};
```

#### Q: What does the above code do?

#### Q: What is the result of: `4 % 2`? What about `5 % 2`?

A:0,1.

#### Q: How can we detect even numbers from the `% 2`?

A: `x % 2 == 0` means it's divisible by 2 and therefore even.

**Q: Can we call a function inside a loop? (refer to the example code)**

A: Yes. All the control flow syntax is combinable. A loop can call a function. A function can have a loop inside. A conditional can be inside a loop.

The most difficult part is deciding which to use!

## In-Class Material

[Day 6: Loops](../in-class-exercises/day-6-loops.md)

## **Look Ahead / Wrap Up**

Next we'll put the loop and array together. The integer location of the index and the counter in the loop match up perfectly to allow us to process _every_ item in an array. This allows us to further expand the amount of data our programs can deal with.

_We want to plant the idea of the equivalence of the loop counter and the array index in students minds so that they have some time to wrap their head around the ideas. If students are struggling with the idea of their code manipulating data, this concept of a loop that adjusts dynamically for the size of the array is one of the more difficult concepts for them to use in their code._

In the next meeting we'll also review the completed dice project.
