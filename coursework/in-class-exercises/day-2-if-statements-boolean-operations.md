# Day 2: If Statements, Boolean Operators

## Introduction

Today we will practice if statements and logical OR operators.

See an example of all problems [**here**](https://rocketacademy.github.io/basics-starter-code/day3/index.html).

**Please switch driver and navigator each exercise, and share your solutions with your partner.**

## Knowledge Check

Before you begin, check that you and your partner can answer the following:

* [ ] Why use logic in our programs?
* [ ] What is an if statement?
* [ ] What is a code block? What marks the start and end of a block of code?
* [ ] What is a Boolean value? What is a Boolean variable?
* [ ] What is a Boolean operator? What are the different kinds of Boolean operators?

## Base

### Lucky 11

Create a dice game that allows a user input a guess number and roll 2 dice when the Submit button is clicked. The user wins if:

1. One of the dice roll matches their guess, or
2. If the total dice roll is 11.

Otherwise the user loses.

{% hint style="info" %}
To test your winning logic, consider using [code control logic](../../modules/3-logic-and-control-flow/3.3-boolean-operators/3.3.3-boolean-and-not.md#code-control), where we temporarily return a fixed number at the start of our random number generator function.
{% endhint %}

### Hawker Food Categorisation

Hawker food is a convenient and affordable food option in Singapore. To help educate non-Singaporeans about hawker food, create an app that takes a hawker dish name as input, and tells users whether the dish has a "rice", "noodle", or "other" base. Some sample dishes are: "chicken rice", "roti prata", "nasi lemak", "hokkien mee", "bak kut teh", and "laksa".

For example, if a user enters "laksa", the program should output "noodle". If a user enters "roti prata", the program could output "other".

Please use the `||` operator.

## Comfortable

{% tabs %}
{% tab title="4D" %}
**4D with Single-Digit Comparison**

[4D](http://www.singaporepools.com.sg/en/rules/Pages/4d-game-rules-general.html) is a popular betting game in Singapore run by Singapore Pools. Rocket Academy does not endorse gambling.

Create a version of 4D where the player wins if their guess matches **any** of the 4 digits. The player will input a **single** digit, and the computer generates 4 random digits between 0 and 9. If the player-inputted digit matches **any** of the randomly-generated digits, the player wins.

In addition to the win/loss result, output the player guess and all randomly-generated digits so the player can see how close they were.

**4D with Winning Range**

Create a version of 4D where the player wins if they guess within 1000 (above or below) of the winning 4-digit number. Consider using comparison operators such as less than (`<`) and greater than (`>`).
{% endtab %}

{% tab title="Hawker Food" %}
**Hawker Food Randomness**

The uncle at your favourite hawker stall has decided to challenge himself and serve a random hawker dish to each customer. The dishes in his repertoire are: "chicken rice", "roti prata", "nasi lemak", "hokkien mee", "bak kut teh", and "laksa". Customers that correctly guess Uncle's dish receive a free meal.

Create an app that uses random numbers to help Uncle decide which dish to cook. The customer can only input dish names. If the customer correctly guesses Uncle's dish, let her know that she gets a free meal!

**Hawker Food Omakase**

{% hint style="danger" %}
Hawker Food Omakase is hard! It took Kai about 45 minutes to create the reference solution.
{% endhint %}

Uncle has decided to serve an omakase option, and output a menu based on customer input.

1. Customers can input either "rice" or "noodle", and Uncle will choose either 2 random rice or 2 random noodle dishes for them. Assume Uncle's rice dishes are "chicken rice", "nasi lemak", and "bak kut teh", and Uncle's noodle dishes are "hokkien mee", "laksa", and "beef hor fun".
2. Roti prata is neither rice nor noodle, but Uncle can randomly choose to include it as one of the two dishes if he feels like it.
3. Uncle charges more for omakase and uses premium descriptions for his dishes. Feel free to get creative. To create a new line in the output box you can use the string `'<br>'`, which generates a new line in HTML output.
4. Output at the end if sambal is included. Not all dishes come with sambal, for example roti prata and bak kut teh don't come with sambal.

**Sample Output**

The customer inputs "rice" and the app chooses 2 random rice dishes, nasi lemak and bak kut teh. Roti prata is randomly not chosen. Sambal is included because nasi lemak typically comes with sambal.

```
Uncle has prepared a selection of dishes for you!

To begin, Nasi Lemak, a fragrant coconut rice. Accompanied by Korean-style fried chicken wing, organic ikan bilis and free-range egg.

This will be followed by Bak Kut Teh, a simmered pork rib broth with fatty pork rib. Accompanied by braised peanuts, you tiao crullers and freshly-blanched chai sim.

Chilli sambal will be included.
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Reminder: There is no need to complete all exercises on this page. Once comfortable with the concepts, feel free to move on to [Project 1: Scissors Paper Stone](../projects/project-1-scissors-paper-stone/). You can always come back and attempt the additional problems when you are feeling _more comfortable_
{% endhint %}

## Reference Solution

[Here](https://github.com/rocketacademy/basics-starter-code-2.0/blob/day2/day02-if-statements-boolean-operators/in-class/script.js) is a reference solution for Day 2 exercises. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
