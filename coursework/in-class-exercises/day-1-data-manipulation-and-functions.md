# Day 1: Data Manipulation and Functions

## Introduction

We will now put to use what we have learned so far. Before you attempt a problem, be sure to:

1. Read through the entire problem statement individually.
2. Check your understanding of the problem by **discussing with your partner**:
   1. What the program needs to do.
   2. How it can be implemented.
3. Write or type, in plain English, the instructions you and your partner want your program to follow.

{% content-ref url="../../course-logistics/learning-environment/pair-programming-instructions.md" %}
[pair-programming-instructions.md](../../course-logistics/learning-environment/pair-programming-instructions.md)
{% endcontent-ref %}

For some problems, you may need to search the web for information. Remember that as pairs, you are also brainstorming together. **Please switch driver and navigator for each problem statement.**

When you run into a bug, talk out loud with your partner what you _expected_ to happen, and what happened instead, before attempting to find a solution.

If needed, use the **'ask Host for help'** function in Zoom. You may also find the **"annotate" feature** in Zoom useful when pair programming.

## Knowledge Check

Before you begin, check that you and your partner can answer the following:

* [ ] Use mathematical operators _****_ to perform mathematical operations in the console of your browser.
* [ ] Describe what a variable is and how to assign it a value or expression.
* [ ] Use the `var` **keyword** to declare a new JavaScript variable.
* [ ] Explain how to achieve _accurate representation_ of your program with suitable variable names.
* [ ] Use the camelCase naming convention for your JavaScript variable names.
* [ ] Understand what a function is and why we use functions.
* [ ] Declare and define a function as a block of code.
* [ ] Understand how to pass input to a function.
* [ ] Understand how to store the output of a function.
* [ ] Understand the purpose of the return keyword.
* [ ] Execute a function.

## **Base**

### **Fahrenheit to Celsius**

The user enters a temperature in Fahrenheit. The program should output the conversion to Celsius in the output box.

Write the code inside the main function first, then extract the code into a [helper function](../../modules/2-structuring-and-debugging-code/2.3-functions/2.3.1-functions.md#define-a-function) that accepts Fahrenheit as the input and outputs Celcius.

{% hint style="info" %}
Formula for Fahrenheit to Celcius: `Celcius = (Fahrenheit-32) x 5/9`
{% endhint %}

### **Road Trip Cost (Base)**

The user will enter the length (**in km**) of a planned road trip in his brand new Ferrari. Write a program that outputs the total fuel cost (**in $**) of the road trip.

A new Ferrari is able to travel 9 miles/litre of fuel. Fuel costs $2.20/litre. Use the approach below to solve the problem.

**Approach:**&#x20;

1. Create a function that accepts distance (in km) as an input parameter and returns distance (in miles). Use the function in the `main` function to test if it works. (The answer is provided below)

```javascript
var convertKmToMiles = function (distanceInKm) {
  var distanceInMiles = distanceInKm * 0.62;
  return distanceInMiles;
};
```

2\. Create a function that accepts a trip length(in miles) as an input parameter and returns the total fuel cost(in $). Use the function in the `roadTripCostBaseMain` function to test if it works. You can use this format below as a guide.

```javascript
var calculateTotalFuelCost = function (tripLengthInMiles) {
  // Some code that calculates total fuel cost
  return fuelCost;
};
```

3\. Now using both functions above, execute them inside the `roadTripCostBaseMain` function to solve the problem.

```javascript
var roadTripCostBaseMain = function (input) {
  // Some code that calculates total fuel cost from distance in km
  return totalCost;
};
```

## **Comfortable**

### **Road Trip Cost (Comfortable)**

The user enjoyed his road trip so much that he decided to do another road trip again but he wishes to compare the cost of travelling via train against the cost of travelling via his Ferrari.&#x20;

The user will enter the length (**in km**) of the road trip. Write a program that outputs the savings in fuel cost (**in $**) of the road trip if he were to travel via train compared to using his Ferrari.

The Ferrari and train are both able to travel 9 miles/litre of fuel. Fuel for the Ferrari costs $2.20/litre. Fuel for the train costs $2.00/litre. Use the approach below to solve the problem.

**Approach:**

1. Make a copy of the `calculateTotalFuelCost` function in the **Road Trip Cost (Base)** section and rename it `calculateTotalFuelCostForComfortable` to use it for **Road Trip Cost (Comfortable)**.&#x20;
2. Change the logic in the `calculateTotalFuelCostForComfortable` function to accept cost per litre of fuel as a 2nd input parameter. Together with the `convertKmToMiles` function in **Road Trip Cost (Base),** write a program that outputs the total fuel cost of travelling **via train** if the user inputs length (**in km**) of the road trip. Use the format below:

```
var convertKmToMiles = function (distanceInKm) {
  var distanceInMiles = distanceInKm * 0.62;
  return distanceInMiles;
};

var calculateTotalFuelCostForComfortable = function (tripLengthInMiles, costPerLitreOfFuel) {
  // Some code that calculates total fuel cost
  return fuelCost;
};

var roadTripCostComfortableMain = function (input) {
  // Some code that calculates total fuel cost using the 2 functions above
  return totalCost;
};
```

2\. Using the new `calculateTotalFuelCostForComfortable` above, add additional code into the `roadTripCostComfortableMain` function to solve the problem.

## More Comfortable

This section contains optional questions for you to attempt. You can practice what you have learnt in Modules 1 and 2 by:

1. First writing pseudocode for the problem, and your proposed solution.
2. Writing all the logic and operations within the provided main functions for each exercise, without any helper functions. This helps you
   1. test that you understand the problem.
   2. test the logic of your proposed solution.
3. Now that we know the solution works, we can abstract away the logic into _helper functions_ that are executed by the exercises' main functions. This keeps our code neat and clean.

This build-test-abstract cycle is common when approaching complex problems. The final step of cleaning up our code is known as **refactoring**.

### Ice Machine

A hotel uses an ice machine to prepare ice for guests. They want to start the ice machine as close to each event as possible, so that the ice doesn't melt. In order to do this, they need to estimate how long they will need to run the ice machine.

Create a program that estimates the duration the ice machine needs to run. The user will input the number of guests for the event.

Assume each guest needs 2 drinks. Each drink has 4 ice cubes. Each cube weights 1.5 grams. The hotel's American-made ice machine produces 5 pounds of ice per hour.

### Beer Order

Create a program for a bar to calculate how many kegs of beer they will need every day. The user will enter the average number of customers per day, and the app will estimate how many half-barrel-size kegs the bar needs per quarter.

Assume an average customer drinks 2 pints per visit. There are 124 pints of beer in a half-barrel keg.

### Cost of Cellular Data

Create a program to calculate how much a user will pay for their the $19.99 50GB post-paid data plan. The user will enter how many GB they use per month, and the app will tell them how much they are paying per GB of data used.

Assume that if the user exceeds 50GB, they will automatically purchase an additional 50GB plan. You may find the built-in function `Math.ceil` helpful for this _(you can google how to use it)_.

For example, if the user only used 1GB this month, the app would calculate $19.99 per GB as the user paid $19.99 for the 50GB plan but only used 1GB. If the user used 2GB this month, the app would calculate $9.98 per GB. If the user used 51GB this month the user would have automatically been billed for 2 plans and the app would calculate $0.78 per GB.

## Reference Solution

[Here](https://github.com/rocketacademy/basics-starter-code-2.0/blob/day1/day01-data-manipulation-and-functions/in-class/script.js) is a reference solution for the Data Manipulation and Function exercises above. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
