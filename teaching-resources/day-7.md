# Day 7: Loops 2

## Overview

This is the day that combines two key syntaxes, the array and the loop.

We moved from functions, which can process a set amount of data based on parameters we write, to global variables, which are another. possibly larger set of values our programs can also deal with depending on the circumstances.

Combining arrays with loops allows another expansion of the volume of data the program can deal with, and we can write the code in such a way that deals with processing all or every item in an array.

Students who had a difficult time understanding the action of loops repeating over a block may also have a difficult time implementing a loop that runs over an array.

## Pre-Class Material

Total Video Watch Time: **\~11 mins**

### [9.3: Loops with Arrays](../modules/3-logic-and-control-flow/3.5-looping-over-an-array.md)

```javascript
var main = function (input) {
  var myOutputValue = '';
  var counter = 0;

  while (counter < 3) {
    console.log(counter);
    myOutputValue = myOutputValue + 'yes';
    counter = counter + 1;
  }
  return myOutputValue;
};
```

#### Review questions:

#### Q: What is the value of `counter` over the the life of the loop?

A: 0,1,2,3

```javascript
var letters = ['a', 'b', 'c', 'd', 'e', 'f'];

var main = function (input) {
  var myOutputValue = '';
  var counter = 0;

  while (counter < 3) {
    console.log(counter);
    myOutputValue = myOutputValue + 'yes';
    counter = counter + 1;
  }
  return myOutputValue;
};
```

#### Q: How can we change this loop code to `console.log` letters **a**,**b** and **c** in the `letters` array? How and why does this code work?

A: `console.log( letters[counter] );`

#### Q: How can we change the loop so that it will console.log every letter in the array?

A: `while (counter < 6)`

#### Q: Is there a way to refactor this code to directly link the loop condition and the array?

A: `while (counter < letters.length)`

```javascript
// Initialise an empty names array
var names = [];

var main = function (input) {
  names.push(input);

  // Return the full array of names
  var myOutputValue = 'All names: ' + names;
  return myOutputValue;
};
```

#### **Q: What does the above code do?**

A: Puts a name into the list and displays the list.

#### **Q: Before we look at the solution below, how could we stop duplicate names from getting into the list?**

```javascript
// Initialise an empty names array
var names = [];

var main = function (input) {
  // Set a boolean value found to a default value of false
  var found = false;

  // Loop over the names array, and set found to true if the input name already
  // exists in the names array
  var index = 0;
  while (index < names.length) {
    var currentName = names[index];
    if (currentName == input) {
      found = true;
    }
    index = index + 1;
  }

  // If no duplicate name was found, add the input name to the names array
  if (!found) {
    names.push(input);
  }

  // Return the full array of names
  var myOutputValue = 'All names: ' + names;
  return myOutputValue;
};
```

#### **Q: The above set of code makes sure that we are not putting in a duplicate name. How does it work?**

## In-Class Material

### [Day 7: Loops and Arrays](../coursework/in-class-exercises/day-5-arrays-and-loops.md)

## Wrap-Up / Look Ahead

Each new syntax and concept we see the amount of data our progams are capable are handing grows. Next we'll see the last new JavaScript syntax we'll cover in Basics. This is a new kind of data that, similar to arrays is a collection of single pieces of data- objects. Objects are special because they are a collection of _**different**_ types of data.
