# Day 2: Functions

## Introduction

Today we will write functions to perform data transformations, similar to examples in [3.1: Functions](../../../modules/2-structuring-and-debugging-code/5.1-functions.md). For each exercise, make a copy of the [starter code](https://github.com/rocketacademy/basics-starter-code/archive/refs/heads/main.zip) as per the [recommended folder structure for Basics](broken-reference). For some exercises you may need to google for information.

**Please switch driver and navigator each exercise, and share your solutions with your partner.**

## Knowledge Check

Before you begin, check that you and your partner can answer the following:

* [ ] How do you define a function?
* [ ] How do you execute a function?
* [ ] Where can you execute a function?
* [ ] How many times can you use a function?
* [ ] What is the purpose of the `return` keyword? What happens if we omit the `return` keyword from a function?

## Learning Outcomes

* Practice **writing helper functions** _(and not just solve for the correct calculation)_
* Executing multiple helper functions as part of the overall program.
* Practice creating contextual, meaningful variables.

## Base

_If you have attempted these problems as part of More Comfortable in Day 1, today re-write the code such that all of the logic is in helper functions and not solely in_ `main.`

See an example of all problems [here](https://rocketacademy.github.io/basics-starter-code/day2/).

### Cost of Air Con

The user enters the number of hours of air-con use, and the app tells them the cost.

An aircon machine uses 2 kilowatts of electricity.

Electricity costs $0.20 per kilowatt-hour.

### Screen Time

The user will enter the number of hours spent per day on their favourite app, and the program renders how many days you will spend in your lifetime on this app.

Assume an average life expectancy of 82 years.

On [Android 10](https://wellbeing.google/tools/), [iOS 12](https://support.apple.com/en-us/HT208982), and later versions, we can see how many hours per day we spend on each app. Find the number of hours you spend per day on the app you use most. If you're not able to find this, you can google for common statistics.

For example, if I spend 2 hours per day on WhatsApp and I live an average lifetime, how many total days will I spend on WhatsApp in my lifetime?

### Ice Machine

A hotel uses an ice machine to prepare ice for guests. They want to start the ice machine as close to each event as possible, so that the ice doesn't melt. In order to do this, they need to estimate how long they will need to run the ice machine.

Create a program that estimates the duration the ice machine needs to run. The user will input the number of guests for the event.

Assume each guest needs 2 drinks. Each drink has 4 ice cubes. Each cube weights 1.5 grams. The hotel's American-made ice machine produces 5 pounds of ice per hour.

### Beer Order

Create a program for a bar to calculate how many kegs of beer they will need every day. The user will enter the average number of customers per day, and the app will estimate how many half-barrel-size kegs the bar needs per quarter.

Assume an average customer drinks 2 pints per visit. There are 124 pints of beer in a half-barrel keg.

## More Comfortable

### Cost of Cellular Data

Create a program to calculate how much a user will pay for their the $19.99 50GB post-paid data plan. The user will enter how many GB they use per month, and the app will tell them how much they are paying per GB of data used.

Assume that if the user exceeds 50GB, they will automatically purchase an additional 50GB plan. You may find the built-in function `Math.ceil` helpful for this _(you can google how to use it)_.

For example, if the user only used 1GB this month, the app would calculate $19.99 per GB as the user paid $19.99 for the 50GB plan but only used 1GB. If the user used 2GB this month, the app would calculate $9.98 per GB. If the user used 51GB this month the user would have automatically been billed for 2 plans and the app would calculate $0.78 per GB.

### Mortgage Calculator

Create a mortgage calculator for a bank. This bank is just starting so their loan terms are simple and the same for everyone. The user will enter the loan amount. The interest is 3% APR. The loan duration is 10 years.

Output several values including:

1. How much the customer will pay back in total, including the principal.
2. How much the customer will pay just in interest.
3. How much the customer's monthly payment will be.

{% hint style="warning" %}
**Concatenating Strings and Numbers**

Sometimes when trying to add 2 numbers you may find that your numbers concatenate instead of add. For example, when adding '1' + 1 in your code, the result may be '11' instead of 2. This is because one of your numbers may be represented in JS as a string, most commonly when the number comes from the `input` variable in our programs.

To resolve similar issues, try converting `input` to a number with [JS' built-in Number function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Number) before using it, e.g. `const loanAmt = Number(input)`.

The following is a more detailed breakdown of JS behaviour when concatenating strings and numbers.

1. String + String
   1. 'hello' + 'hi' will return 'hellohi'
   2. '2' + '2' will return '22'
2. Number + Number
   1. 2 + 2 will return 4
3. Number + String
   1. 2 + '2' will return '22'
{% endhint %}

## Reference Solution

[Here](https://github.com/rocketacademy/basics-starter-code/blob/day2/script.js) is a reference solution for Day 2 exercises. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
