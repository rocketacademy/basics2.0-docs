# Day 1: Data Manipulation and Functions (NEW)

## Introduction

We will now put to use what we have learned so far. Before you attempt a problem, be sure to:

1. Read through the entire problem statement individually.
2. Check your understanding of the problem by **discussing with your partner**:
   1. What the program needs to do.
   2. How it can be implemented.
3. Write or type, in plain English, the instructions you and your partner want your program to follow.

For some problems you may need to google for information. Remember that as pairs, you are also googling together. **Please switch driver and navigator for each problem statement.**

When you run into a bug, talk out loud with your partner what you _expected_ to happen, and what happened instead, before attempting to find a solution.

If needed, use the **'ask host for help'** function in Zoom. You may also find the **"annotate" feature** in Zoom useful when pair programming.

### <mark style="color:red;">INSERT CODESANDBOX INSTRUCTIONS HERE ON HOW TO START ON THE EXERCISE (This is to replace the instructions that we ask students to fork the starter repo)\*\*\*</mark>

## **Base**

### **Fahrenheit to Celsius (Data  Manipulation)**

The user enters a temperature in Fahrenheit. The program should output the conversion to Celsius in the output box.

Format the output nicely.

Write the code inside the main function first, then extract the code into a [helper function](../../modules/2-structuring-and-debugging-code/2.2-functions.md#define-a-function) that accepts Fahrenheit as the input and outputs Celcius.

Formula for Fahrenheit to Celcius: Celcius = (Fahrenheit-32) x 5/9

### **Road Trip Cost (Data  Manipulation and Functions)**

The user will enter the length(**in km**) of a planned road trip in his brand new Ferrari. The program should output the estimated fuel cost(**in $**) of the road trip. A new Ferrari consumes 9miles/litre. Petrol costs $2.20/litre.

Format the output nicely.

**Approach:**&#x20;

1. Create a function to convert kilometers to miles.

```
var convertKmToMiles = function (distanceInKm) {
  var distanceInMiles = distanceInKm * 0.62;
  return distanceInMiles;
};
```

2\. Using the output in 1., create a function to calculate the petrol consumption in litres

```
var milesToLitres = function (distanceInMiles) {
  // Some code that calculates pretrolConsumptionInLitres
  return pretrolConsumptionInLitres;
};
```

3\. Using the output in 2., create a function to calculate the petrol cost in $.&#x20;

```
var LitresToCost = function (pretrolConsumptionInLitres) {
  // Some code that calculates cost
  return cost;
};
```

4\. Use the functions above in the main function to calculate the estimated fuel cost(in $) of the road trip.

## **Comfortable**

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

## Reference Solution

(Fahrenheit to Celcius, Road Trip Cost)

[Here](https://github.com/rocketacademy/basics-starter-code/blob/day1/script.js) is a reference solution for the Data Manipulation exercises above. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.

(Ice Machine, Beer Order, Cost of Cellular Data)

[Here](https://github.com/rocketacademy/basics-starter-code/blob/day2/script.js) is a reference solution for Day 2 exercises. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
