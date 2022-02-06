# Day 12: DOM, Project Presentations

## **Overview**

This is the last class meeting!\
\
Mention to the students that this day isn't meant as a full review of the pre-class material. The pre-class material is meant as a look ahead into what is possible with JavaScript given the tools that have already been covered.

### Class Schedule

1. 1:00-2:00pm: Blackjack presentations
2. 2:00-2:15pm: Post-Course Feedback Form and reviews
3. 2:15-2:30pm: LinkedIn Certs
4. 2:30-3:00pm: Closing Ceremony in Main Zoom Room

## **Project Due**

#### [Project 3: Blackjack (More Comfortable)](../coursework/projects/project-3-blackjack.md#more-comfortable)

Deploy Blackjack to the internet with instructions from [Module 12.3: Deployment](broken-reference/)

## Pre-Class Material

Total Video Watch Time: **\~22 mins**

### [12.1: Browser Applications with DOM](../modules/6-document-object-model/6.3-browser-applications-with-dom.md)

#### Q: What is the DOM?

A: The DOM is two variables called `window` and `document`. They are created by the browser and represent everything that's happening in the window and on the page.

#### Q: What can you use the DOM for?

A: Almost every website now uses the DOM to display things on the screen.

Example: Google Sheets: [https://docs.google.com/spreadsheets/d/1LjRxTu0E9lwAPRYc\_WFYsFEAA4WAEjAP65igIHm\_PwY/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1LjRxTu0E9lwAPRYc\_WFYsFEAA4WAEjAP65igIHm\_PwY/edit?usp=sharing)\
\
Google sheets uses the DOM in combination with all of the data in Google's Sheets database to create and update the screen that users see. The data that is displayed on the page is represented as arrays and strings and objects inside the google system (among other representations) and is displayed on the screen of the browser using the DOM.

#### index.html

```markup
<!DOCTYPE html>
<html>
  <head>
    <title>Basics</title>
    <style>
      * {
        box-sizing: border-box;
      }

      body {
        font-family: sans-serif;
        margin-left: 30px;
        margin-right: 30px;
      }

      #header {
        text-align: center;
      }

      #container {
        background-color: pink;
        margin: 40px auto;
        max-width: 800px;
        padding: 38px 31px;
      }

      input {
        font-size: 21px;
        line-height: 33px;
        margin: 0 0 23px 0;
        padding: 0 9px;
        width: 100%;
      }

      button {
        font-size: 21px;
        line-height: 33px;
        margin: 0 0 23px 0;
        padding: 0 6px;
      }

      #output-div {
        background-color: lightgrey;
        margin: 20px auto;
        padding: 20px;
        width: 100%;
      }
    </style>
  </head>

  <body>
    <h1 id="header">Basics! 🚀</h1>
    <div id="container">
      <p>Input:</p>
      <input id="input-field" />
      <br />
      <button id="submit-button">Submit</button>
      <p>Output:</p>
      <div id="output-div"></div>
    </div>
    <!-- Import program logic -->
    <script src="script.js"></script>
    <!-- Define button click functionality -->
    <script>
      var button = document.querySelector("#submit-button");
      button.addEventListener("click", function () {
        // Set result to input value
        var input = document.querySelector("#input-field");
        var result = main(input.value);

        // Display result in output element
        var output = document.querySelector("#output-div");
        output.innerHTML = result;

        // Reset input value
        input.value = "";
      });
    </script>
  </body>
</html>
```

#### script.js

```javascript
var main = function (input) {
  var myOutputValue = 'hello world';
  return myOutputValue;
};
```

Review the starter code for the students- inside a script tag in `index.html` is the heart of how the starter code DOM manipulation works. Here is a concise commented version of the above. Note that this assumes the main function defined above.

```javascript
var button = document.querySelector("#submit-button");

// the function that will run when the submit button is clicked
var handleSubmitClick = function(){
  // put the input field DOM element into a variable
  var input = document.querySelector("#input-field");
  
  // get out the value the user typed
  var userTypedValue = input.value;
  
  // run the main function defined in script.js:
  //   a) pass in the typed value as a parameter
  //   b) capture the returned value in the result variable
  var result = main(userTypedValue);

  // put the grey box element into a variable
  var output = document.querySelector("#output-div");
  
  // set the content of the grey box to
  // the value returned out of main
  output.innerHTML = result;

  // Reset input value to blank
  input.value = "";
}

// set the function to run when the button gets clicked
button.addEventListener("click", handleSubmitClick);
```

#### Q: How does the above code work?

### [12.2: HTML, CSS Review](../modules/6-document-object-model/6.1-html-css-referencing.md)

## In-Class Material

### [Project Presentations](../course-logistics/course-methodology/#project-presentations)

Congratulate everyone on a job well done!! 🎉

Emphasise that for this course it's not about how many features of Blackjack that were completed in the project, it's about what they were able to accomplish and understand about coding.

Ask the students to reflect on their level of knowledge six weeks ago.

### **Course Feedback and Reviews**

#### Review links

1. SwitchUp: [https://www.switchup.org/bootcamps/rocket-academy](https://www.google.com/url?q=https://www.switchup.org/bootcamps/rocket-academy\&sa=D\&source=editors\&ust=1625291865969000\&usg=AFQjCNH39J3LKDV1-38Sls050tRr9zEBXg)
2. Google Business: [https://g.page/rocket-academy-co/review?rc](https://www.google.com/url?q=https://g.page/rocket-academy-co/review?rc\&sa=D\&source=editors\&ust=1625291865970000\&usg=AFQjCNGvwlXotNRLE7I9jMmGmHgWjp76dA)

### **LinkedIn Certificate Presentations**

Invite the RACert Bot into your Slack Channel by mentioning it for the first time: @RACertBot.

Generate certificates for each student by mentioning @RACertBot followed by each student's @username in Slack

Share with students how they can add Rocket Academy's Coding Basics Certificate badge to their LinkedIns. [Instructions here](../course-logistics/post-course/linkedin-certificates.md).

### **Class Photo 🥳**

Please take a screenshot in Zoom gallery view that we can use as the profile photo for the section alumni group chat in Telegram!

After the photo, class is officially over, but please encourage students to use the remaining class time to help RA by sharing feedback and public reviews of our course.
