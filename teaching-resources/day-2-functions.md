# Day 2: Functions

## Overview

This day introduces two foundational topics: functions and errors.

{% hint style="warning" %}
Before the meeting, ask the students to put their [5.1 Functions](../modules/2-structuring-and-debugging-code/5.1-functions.md) exercise code as a snippet in a thread in the Slack channel. As part of the message, ask them to rate their own understanding 1-5.
{% endhint %}

## Pre-Class Material

Total Video Watch Time: **\~25 mins**

## Review[ Social Rules](../course-logistics/course-methodology/social-rules.md)

In the previous session the students were introduced to the idea of pairing and got to experience it for themselves. Now that they have some context for the experience we want to talk about the optimal pairing experience, and to emphasize how their behaviour is key to the experience for themselves and others.

**To begin, reiterate the big ideas behind pairing because the students only heard them once before:**

* Learning directly from a peer helps with understanding.
* The best way to fully know something is to have to explain it.
* Pairing is a collaborative experience that should involve a lot of communicating and talking.
* Both people are focused on the same task. Not one person typing, another person Googling.

Then, introduce the social rules. Briefly mention each one. No need to read the whole thing. Ask them to read it if they haven't already. Remind students that these are just some pitfalls when working closely with others and are not actually rules, and that they mostly boil down to, be considerate.

The rules are just a reminder because they are behaviors that commonly arise when discussing technical topics.

### Discussion Questions

#### Q: Have you ever felt dumb or uncomfortable or unknowledgeable when speaking with someone who is an "expert" in a topic? Give an example you feel comfortable sharing.

A: In a lot of situations in everyday life people can inadvertently (or sometimes even purposefully) make you feel bad for not understanding something. We hope the social rules can help everyone avoid these kinds of situations by being more kind and thoughtful.

## [5.1: Functions](../modules/2-structuring-and-debugging-code/5.1-functions.md)

### Overview

The Basics curriculum is trying to emphasize functions as the most important unit of computation. Because a game will naturally have some global values we also have to introduce those, but the idea is that when the computer must do something the easiest way to think about it is wrapped in a function.

There are a few key ideas that students should take away:

* functions can be named and the action of computation can also stand in for the value itself. `calcCircleArea(3)` is both an expression of a calculation but is also the value (the return value). Clear naming is key to writing a good function.
* writing code that decomposes into input (parameters) and output (return value) is much easier to reason about than code that deals with multiple global values. Therefore, we should try to emphasize writing functions that take input and return values.

#### Discussion Questions

Prepare the example code in VSCode. Run it in the browser.

```java
var add = function(a,b){
    return a + b;
};
var result = add(1,2);
```

#### Q: What value is inside `result`?

A: The sum of `a` and `b`.

#### Q: What happens when we omit the `return` keyword? (leaving in the addition operation)

A: variable `result` will hold the value `undefined`.

#### Q: Can we change the name of `a` or `b` to something else?

A: Yes, a function parameter _**name**_ is defined, like a variable, inside the function definition parentheses. A function parameter value is defined when the function is executed.

#### Q: What happens when we give a variable to the function? What happens to the variable? `var num = 99; var result2 = add(num,6);`

A: Nothing happens to the variable. We can call a function and pass in any kind of value. In the first example we were passing in **literal** values, we can also pass in variable values. A third option would be to pass in function return values. (_shown in another example below_)

#### Q: What happens if we call the function a second time below line 4? `var result3 = add(5,6);`

```javascript
var main = function(input){
    return "hello " + input;
};
```

#### Q: Can we name the function to something other than `main`?

A: No, that name is set inside of the starter code.

#### Q: Can we change `input` to something else?

A: Yes. A function parameter _**name**_ is defined, like a variable, inside the parentheses. A function parameter value is defined when the function is executed.

Note the function execution of `main` happens in another part of the starter code.

#### Q: What happens when we take out the `return` keyword?

A: The word undefined will be put in the grey box. This is because if there is no return keyword, the value returned by a function is the value `undefined`.

{% hint style="warning" %}
Because functions and return values are an important topic, be sure to emphasize the distinction between function \***values**\* being returned and and a statement like, "_the function returns undefined"_.
{% endhint %}

```javascript
var add = function(a,b){
    return a + b;
};

var main = function(input){
    var userTypedInput = 'input is: ' + input;
    var result1 = userTypedInput + ' plus 5 is: ' + add(input, 5);
    var result2 = userTypedInput + ' plus 6 is: ' + add(input, 6);
    var myOutputValue = result1 + ' ' + result2;
    return myOutputValue;
};
```

#### Q: How many times does the `add` function run?

A: Twice every time the main function runs, and as many times as the user clicks submit. This question will hopefully help clarify that a function is meant to be run multiple times.

#### Q: What happens if the add function is moved below the main function? Will it still work?

A: We haven't covered asynchronous code yet, but the students should still understand that the main function doesn't run until the user clicks submit. The absolute order of line numbers is not important when talking about control flow and functions.

E.g., if the code was synchronous, but was a function called from within another function further above it would still work.

{% hint style="warning" %}
Note that we can avoid opening the **index.html** file so as not to confuse students with the DOM manipulation code. Feel free to answer questions, but the main point of the starter code is that the students can understand it in the context of function execution only and not in terms of asynchronous callbacks yet.
{% endhint %}

```java
var add = function(a,b){
    return a + b;
};
var result = add(1,add(3,4));
```

#### Q: How does this code work? What is the result?

A: 8. First, 3 and 4 are added together. The returned value is given as a second argument to the add function. Then 7 and 1 are added together.

#### Common FAQ

Some common misconceptions around functions:

Q: Students think that the function must be run on the line after it is defined.

A: A function can be called from anywhere. Control flow means that when the function is called it jumps to whatever line it was defined on.

Q: Students think that in order to run more code, they copy the function and use similar lines from the previous operation.

A: Refactoring or recognizing a pattern that repeats itself within the code is something that the students should have in mind to practice.

## [5.2: Errors](../modules/2-structuring-and-debugging-code/5.2-errors.md)

### Overview

A common misconception with coding is that all the time spent learning to code or doing coding is spent actually typing out the code. It is important to emphasize to students that the learning process is 80% about identifying and fixing errors. (And also that the professional coding process is also 80% fixing errors).

In this sense the idea of errors and the strategies for approaching them are as important or more important than any other subject covered in Basics.

{% hint style="warning" %}
Reinforce and continue to reinforce the idea that the students should always **immediately** open the dev tools whenever they open the browser. If you aren't already doing this, always pattern this behavior for students.
{% endhint %}

### Discussion Questions

#### Q: What is the difference between a compile-time error and a run-time error?

A: _Be ready to code out both errors. Have the example code ready._ One happens when the page loads, the other happens when the code is run- that is, a function's code isn't necessarily run right away, for example the code inside the main function.

#### Q: What is the difference between a syntax error and a logical error?

A: A syntax error will result in red text in the dev tools console.

#### Q: What are the different use cases for `console.log`? If there is an error, what order should they be tried in?

A: 1. Control flow check. See if the control flow goes to a given line. 2. Value check. See what value is in a variable.

### Common FAQ

#### Q: Students will neglect to open the dev tools before doing anything else.

A: Opening the dev tools should be the first thing they do when opening the HTML file.

#### Q: Students will have an error but attempt to run their code.

A: Anytime an error occurs in the program, JavaScript stops execution immediately after the error. If an error occurs the student must drop everything and solve that error before moving on.

#### Q: Students won't run their code to check for errors often enough.

A: Related to above, if you don't catch errors one at a time it is impossible to unwind where a series of errors in caused.

## In-Class Material

### [Day 2: Functions](../coursework/in-class-exercises/day-1-basic-file-and-data-manipulation/day-2-functions.md)

The topic of these exercises are very similar to the previous exercises, except they are in the context of functions. Try to encourage the students to break the calculations down into separate helper functions.

Check for understanding by looking for well formed functions that use multiple arguments and return values.

## **Look Ahead / Wrap-up**

After functions are covered students can make basic calculations and format strings. We've introduced another wrinkle into naming things, which is to name functions as action (verb) that also expresses some data value. Clear representation is more important than ever.

It's still early days and the programs are still very simple. Next we add in another kind of control flow, conditions. This is the point at which the code can actually make decisions. When we add in this branching logic things become a lot more complex. In fact logic as a topic on it's own is huge, but we'll be able to apply some simple concepts that are very intuitive for our purposes.
