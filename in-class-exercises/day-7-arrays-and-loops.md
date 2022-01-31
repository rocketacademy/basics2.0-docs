# Day 7: Arrays and Loops

## Introduction

Today we will practice arrays with occasional loops through the game of Mad Libs. Note that loops may not be necessary for every exercise.

Mad Libs is a word game where players fill in the blanks with random words, such that the final sentence is usually funny. If you're unfamiliar with Mad Libs, please read the Wikipedia description [here](https://en.wikipedia.org/wiki/Mad\_Libs).

#### Example "Mad Lib" Sentence from Wikipedia

```
"___________! he said ________ as he jumped into his convertible ______ and drove off with his _________ wife."
 exclamation           adverb                                     noun                         adjective
```

## Getting Started

For the 1st exercise, make a copy of the [starter code](https://github.com/rocketacademy/basics-starter-code). For subsequent exercises, feel free to comment out your previous code and create a new `main` function for the current exercise. Please switch driver and navigator each app.



See an example of all problems [**here**](https://rocketacademy.github.io/basics-starter-code/day7/index.html).

## Base

### Mad Libs Adjectives

#### Example Mad Lib in Code

The following code is the above example Mad Lib written in JavaScript, where the exclamation, adverb, and noun have been hard-coded and `randomAdj` refers to the random adjective our program will randomly select to complete the Mad Lib.

```javascript
var madLib =
  '"WOW!" he said EXCITEDLY as he jumped into his convertible PAPAYA and drove off with his ' +
  randomAdj +
  ' wife.';
```

#### Instructions

_Please read all instructions before getting started._

1. When the Basics Starter Code app loads, the user can input 1 adjective at a time to store in the app. Store the user-inputted adjectives in a global array variable.
2. When the user inputs the word "create" the app completes the Mad Lib with a random word from the user-inputted adjectives array and outputs the completed Mad Lib in the grey box.

#### Random Elements from an Array

In order to get a random value from an array we can generate a random integer in the range of: zero to the last index of the array.

```javascript
var getRandomIndex = function (arrayLength) {
  // create a random number from zero to array length minus one.
  // this number is in the range from the first
  // index (zero) to the last index (array length minus one)
  var randomIndex = Math.floor(Math.random() * arrayLength);
  return randomIndex;
};
```

## Comfortable

### Popular Mad Libs

Keep track of which words are selected. Create and allow the user to switch to a new game mode that always shows a completed Mad Lib on Submit using the set of words (verb, adjective, etc.) that the app has (randomly) selected most often so far.

### Input and Create Mode

When the Basics Starter Code app loads it starts in "input", or normal mode. In input mode, the user can add adjectives to their adjectives list with each Submit.

When the user inputs "create", change the game mode to create mode. In create mode, each Submit prompts the app to complete your Mad Lib.

### Input Multiple Words

When the Basics Starter Code app loads, the user can input 1 or more adjectives to store in the app with each Submit. To input more than 1 word for each Submit, the user would give each word separated by a space, e.g., "_green nice silly_". We can use JavaScript's string `split` method to split the input string into an array of substrings. See W3Schools docs [here](https://www.w3schools.com/jsref/jsref\_split.asp) for details.

{% hint style="info" %}
Reminder: There is no need to complete all exercises on this page. Once comfortable with the concepts, feel free to work on Project 2: _Beat That!_ as a pair, or go back and solve / refactor previous _More Comfortable_ exercises like [_Hawker Food Omakase_](day-3-if-statements-boolean-or.md#hawker-food-omakase) with your newly learnt skills.
{% endhint %}

## More Comfortable

### Mad Libs Multiple Word Types

Update our Mad Lib to take additional word types.

```javascript
var madLib = `${randomExclamation}! he said ${randomAdverb} as he jumped into his convertible ${randomNoun} and drove off with his ${randomAdj} wife.`;
```

Create modes to input words from different word types, e.g. exclamation, adverb, noun, and adjective. For each type, prompt the user what type of word they should be entering. If it's too tedious to support 4 word types, considering starting with 2 word types.

### Sets of Mad Libs

Store an array of Mad Lib sentences in your app. For example, Mad Lib 1 might be:

> She asked {adverb} for the {noun} and when they were rude, she said {exclamation} and hung up the {adjective} phone.

Mad Lib 2 might be:

> It was a {adjective}, cold November day. I woke up to the {adjective} smell of {noun} roasting in the {noun} downstairs.

Update create mode to pick a random Mad Lib sentence and set of words and output the completed Mad Lib in the grey box on Submit.

Feel free to see Google results [here](https://www.google.com/search?q=mad+lib+examples\&tbm=isch) for potential Mad Lib inspiration.

## Reference Solution

[Here](https://github.com/rocketacademy/basics-starter-code/tree/day7) is a reference solution for Day 7 exercises. [Here](https://github.com/rocketacademy/basics-starter-code/tree/day7-moreComfortable) is a reference solution for Day 7 More Comfortable exercises. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
