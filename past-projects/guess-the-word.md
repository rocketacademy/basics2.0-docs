# Guess the Word

This is a game where the player must guess a secret word.‌

Begin the app by **forking** this repo: [https://github.com/rocketacademy/basics-guess-the-word](https://github.com/rocketacademy/basics-guess-the-word)​‌

For each wrong guess the program adds to the figure: (凸 ಠ 益 ಠ)凸 ‌

The player can only guess wrong 7 times before the game ends. (the number of characters in the figure)‌

Before you start read through the advice on how to start and the more comfortable sections to see what the basic and advanced versions of the game include.‌

## How to Start <a href="#how-to-start" id="how-to-start"></a>

The first version of this game you can have a single, hard-coded secret word- `cat`.‌

The data structure you need to represent the game that guesses each individual letter in a word is an array of individual letters.‌

This will allow you to guess letters and find each letter guessed and the position of those letters in the word.‌

A word array would look like this: `var word = ['c','a','t'];`.‌

### Game Play <a href="#game-play" id="game-play"></a>

When the user guesses a letter, you have to have the program look through the word array and determine if the user guessed correctly.

> "Looking through" means looping over the word array and comparing it to the letter the user has inputted.

When the user guesses there are two possibilities:‌

1. The user guesses incorrectly. Add a character to the figure that marks when they lose the game.
2. The user guesses correctly, add the letter to the word they are trying to complete.

(In the first version you can just do basic output like how many guesses the user has left, and how many letters they have correct.)‌

After checking the guess for the individual user guess, check for the state of the entire game:‌

If the user has guessed all the letters in the word, tell them they have won.‌

If the user has completed the figure tell them they lost.‌

## More Comfortable <a href="#more-comfortable" id="more-comfortable"></a>

### Output Formatting <a href="#output-formatting" id="output-formatting"></a>

When the user types a correct guess show the correct guess in the location of the secret word. Show the number of letters in the secret word.‌

### Easier / Harder Mode <a href="#easier-harder-mode" id="easier-harder-mode"></a>

Add different modes to the game. Change the secret word to a word with the same letter more than once.‌

The easy mode is when the word is like "guess" and the user guesses 's', then the game fills in both 's'.‌

The hard mode is where the user has to guess each letter.‌

### Name <a href="#name" id="name"></a>

Let the user enter their name at the beginning of the game.‌

### More words <a href="#more-words" id="more-words"></a>

Add a list of words to the game. When it starts the game selects one random word.‌

### Continue Play <a href="#continue-play" id="continue-play"></a>

When the user has played one game with one word, allow them to continue playing with another word.‌

## Reference Solution <a href="#reference-solution" id="reference-solution"></a>

Please only refer to the reference solution after you have attempted the project. Thank you!‌

Note that there are many ways to implement the project and the reference solution is only 1 way.‌

​[https://github.com/rocketacademy/basics-guess-the-word/pull/5/files](https://github.com/rocketacademy/basics-guess-the-word/pull/5/files)​
