# Day 1: Coding Tools

## Overview

The first meeting of the course sets the tone for the rest of the sessions.

This day has a heavier section of content than the other days so be prepared for the review portion to take a bit longer. There may also be setup questions.

### **Some things to keep in mind overall for the first meeting:**

**Repeatedly encourage questions from the students.**

**Running on time is important.** Respect people's time- begin the session on time and don't end after 9.

**Sorting out setup problems from students (with VSCode or the terminal or folders) will be an issue on the first meeting.** Unless you know for sure that it is a quick fix, don't spend any time in front of everyone to fix one person's problem. Either wait until the pairing or, even better, wait to meet with them after the session.

{% hint style="warning" %}
Before the meeting, ask the students to put their [4.2 Our First Program](../modules/2-structuring-and-debugging-code/4.2-our-first-program.md) exercise code as a snippet in a thread in the Slack channel. As part of the message, ask them to rate their own understanding 1-5.
{% endhint %}

## Pre-Class Material

Total Video Watch Time: **\~48 mins**

### [1.1: What is Coding?](../modules/0-introduction/0.1-what-is-coding.md)

#### Overview:

This section is to get the students thinking about the high level context of what the course is about.

#### Discussion questions:

#### Q: Name a piece of software that you use on a daily basis that you don't access through a personal digital device such as a phone, tablet, or laptop.

#### Q: For that software, define what that input is, what the output is and what the software in this computer is responsible for.

Possible answers:

AirPods

Input: Opening the case. Output: starting to play sound.

An office building

Input: a change of temperature inside. Output: run AC at higher or lower level.

Car engine

Input: Readings from engine sensors. Output: instructions to the engine parts (i.e., fuel injectors, etc.)

### [1.2: Web Browsers](../modules/0-introduction/0.2-web-browsers.md)

#### Overview

This section moves one level lower in the context of how the course runs. The students should understand that the only way to run the `script.js` file is to run the HTML file.

#### Discussion questions:

#### Q: What is HTML and how does HTML relate to Browsers?

A: HTML is a file with words and characters in it. HTML specifies what appears in the screen of the browser.

#### Q: How does HTML relate to JavaScript?

A: After HTML is loaded by the browser, if the HTML contains JavaScript or a reference to some JavaScript, that JavaScript code is run in the context of that page.

### [2.1: Command Line](broken-reference/)

#### Overview

We are mainly doing the command line so that the students can use Git. The students also get some benefit from understanding how to use the computer in a more strict, programmer-focused interface.

#### Discussion questions:

#### Q: What is the command line?

A: It is an interface to the computer. Contrary to the GUI, it only displays things using words.

#### Q: Is there anything that we can't do in the command line that we can do in a GUI, or vice-versa?

A: Some programs only run in the context of either, for example, the Git program we installed only runs in the command line. Photoshop can only run in the GUI.

#### Q: Why are we learning the command line?

A: We need to use the command line to use Git. The command line is the most programmer-focused way to interact with your computer.

### [2.2: Git](broken-reference/)

#### Overview

Using Git is important for the students to do their work. At this stage is some are a bit confused this is ok, some understanding will come through practicing the commands.

#### Discussion questions:

#### Q: What is Git for?

A: Git is used to save all the different versions of the program we are going to create..

#### Q: How would you define the difference between Git and the terminal?

A: Git is a program you use \*inside\* the terminal. The terminal is the computer interface where you \*run\* programs.

#### Student FAQ

#### Q: How do I get a previous version back?

A: There are specific Git commands for that, but it is out of the scope of the course. When we cover the section [7.2 on browsing GitHub](broken-reference/) we'll see how we can navigate and copy and paste a previous version.

### [3.1: Operations](broken-reference)

#### Overview

This section is relatively intuitive. It is important to establish here that an **operation** is the smallest bit of computation we can start with. All other code we'll write stems from doing operations, though they may not all be with integers.

### [3.2: Variables](../modules/1-data-structures-and-manipulations/3.2-variables.md)

#### Overview

From operations we add in variables. Here it is important to re-emphasise the concept of accurate representation vs correct calculation.

#### Q: Why is variable naming important?

A: Accurate representation is just as important as correct calculation.

### [4.1: Intro to GitHub](broken-reference/)

#### Overview

It is a common misconception to confuse what Git and GitHub are responsible for. To help, we separate the two sections explicitly.

#### Discussion Questions

#### Q: What is the difference between Git and Github?

A: Git is a version control program. GitHub is a web application for keeping Git repos on the internet.

#### Q: What does a GitHub fork do?

A: It copies a cloud (remote) repo from one GitHub account into your own account.

### [4.2: Our First Program](../modules/2-structuring-and-debugging-code/4.2-our-first-program.md)

#### Overview

This is the first introduction on the starter code. Some students will have some questions about what the main function is, but keep in mind that functions will be covered in the next section.

Be ready to demonstrate this code for the students and have it setup in case you need to demonstrate anything related to their questions.

#### Discussion Questions

```javascript
console.log('papaya');

var main = function (input) {
  var myOutputValue = 'hello world';
  return myOutputValue;
};
```

#### Q: When I type something in the input in the browser how do I get it to display in the grey box?

A: Use input as part of the `myOutputValue` variable, or assign input directly to `myOutputValue`.

#### Q: I want to write a program so that I can type a number in the input and then click the submit button and see that number multiplied by 12 in the grey box. For example, I type in 2, I see 24 in the grey box.

A:

```javascript
var main = function (input) {
  var myOutputValue = input * 2;
  return myOutputValue;
};
```

#### Q: To add on to the previous question, I also want to see the number I typed in inside the grey box, in a full sentence. Example: I type in 2. I click submit. In the grey box I see: "_You typed in 2. The result is: 24."_

```javascript
var main = function (input) {
  var result = input * 2;
  var myOutputValue = "You typed in " + input + ". The result is: " + result;
  return myOutputValue;
};
```

## In-Class Material

### [Day 1: Basic File and Data Manipulation](../coursework/in-class-exercises/day-1-basic-file-and-data-manipulation/)

#### Overview

_**This is the first pairing exercise the students will do.**_ Set the tone for the exercise because this is the first time students have heard of pairing. It's important to emphasize the ideal pairing culture we want to build in Basics.

#### You might touch on the following points:

* Pairing only works when both people are willing to commit to the experience and be open to learning from the other person and / or patiently explaining what the other person may not be familiar with.
* Be coachable. Make an effort to listen well when someone wants to explain something.
* Teaching is the best way to understand something deeply. Try to give the clearest explanations possible. This can be very difficult but will really cement a concept.

#### Things to look out for in the pairing session:

It's important that everyone is on the same page with the setup and command line / Git sections. Some will not be completely setup yet. It is better to spend the pairing time to clear up any misconceptions or setup errors now so the students can move forward easily.

Look out for people who don't have things setup according to the guidelines, such as:

* no folder structure setup ahead of time
* using a browser other than chrome
* using some other setup besides the starter code like codepen.io

Be clear with the students that it's important to follow along with the setup as outlined so that in pairing everyone begins with the same context.

Keep note of any students who already seem lost or confused.

## **Look Ahead / Wrap-up**

Our code doesn't do too much yet, we've named some values and done some calculations. This is just the beginning. Next we'll see functions- which is a kind of control flow- a way to specify which groups of lines of code runs. We'll use this to build up our programs in pieces. After that we'll begin to talk about program logic with conditionals.
