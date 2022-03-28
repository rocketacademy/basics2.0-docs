# 5.2: Cascading Style Sheets (CSS)

## Learning Objectives

By the end of this lesson, you should be able to:

* [ ] Define CSS
* [ ] Understand and use CSS syntax&#x20;
* [ ] Add styles to HTML with CSS
* [ ] Understand the cascading property of CSS

### Intro To CSS

Built on top of HTML to add more visual control and complexity, CSS specifies styles on an HTML element or set of elements. The CSS code specifies visual properties unrelated to the written content on an HTML page. In practice there are 2 uses for CSS: element **styling** and **layout**.

#### Element Styling

CSS helps us change visual properties of HTML elements, such as fonts, background images, or rounded corners on buttons. These properties can be defined statically, meaning that they are hard-coded and unchanging, and can be dynamically manipulated, e.g.  hiding or showing elements and flipping elements 90 degrees. We will learn how to implement visual logic by altering CSS properties in [Module 6.](../6-document-object-model/)

#### Layout

CSS can help us divide our UI into visual sections. This is one of the most tricky aspects of CSS, because CSS was not _originally_ intended for layout design. We will **not** be covering layout extensively in Coding Basics, Rocket's Bootcamp will focus on implementing UI layouts.

![CSS Layout](https://media3.giphy.com/media/13FrpeVH09Zrb2/giphy.gif?cid=ecf05e47swzkw8loxavmvqrz317zbr7wnkc8l0m5t9s7ls85\&rid=giphy.gif\&ct=g)

## CSS Syntax

CSS is a declarative language. It doesn't tell the browser what to do but rather describes the rules that the browser then uses to render the page.&#x20;

CSS styling can be applied in three ways:

1. In-line styling.
2. Internal styling.
3. External styling.

### In-line Styling

We have already seen in-line styling: it **** is written inside the HTML opening tag as an property-value pair.  This is the simplest and most direct way of defining the style of a HTML element:

```html
<p style = “color: red;”> This text would be red </p>
```

If more than one style declaration is applied:

```html
<p style = “color: red; font-weight: bold;”> This text is red and bold </p>
```

However, applying, tracking, and managing styles of individual HTML elements in a complex, large HTML file can quickly get messy. Perhaps we wanted to apply a certain style to all the paragraph elements on a page, and define it once. It would make it much easier to manage, and ensure that style changes applied to all the necessary elements, without having to proofread each line of the HTML file.

### **Internal Styling**

**Internal styling** allows us to define the style for elements, or groups of elements centrally. These rules are defined within the HTML document, hence internal styling.

#### Sample Syntax

```css
selector {
	property: value;
	property: value;
}
```



As a declarative language, CSS uses selectors and declarations to apply styling rules to HTML pages. The syntax for CSS starts with a selector: the HTML element(s) we want to define style rules for. Then a declaration code block is created using open and closing curly braces. Inside the declaration code block are the style rules, in a similar syntax as in-line styling. You can have as many rules as needed. It is conventional to put each rule on its own line in code.&#x20;

All CSS rules are placed inside the `<head>` tag of the page and is wrapped inside the `<style>` tag. In this example, the selector of `p` is chosen to style all the paragraph tags on the page.

```html
<html>
  <head>
    <title>Page Title</title>
    <style>
      p {
        color: white;
      }
    </style>
  </head>
  <body>
    <p>This text is white</p>
    <p>This text is also white!</p>
  </body>
</html>
```

### **External Styling**

**External styling** is when the styles are defined in a _separate file_ and is referenced by index.html. In Basics, you would have noticed a file called `styles.css` where the styles for various HTML elements are defined. This allows for better neatness and organisation, and for a styles to be centrally defined in a single _stylesheet_ and applied across various HTML files, if necessary.

When defining styles in a `.css` file, it is not necessary to have opening and closing `<style>` tags. Rather, the entire file is **linked** into the `.html` file using a link tag, in the `<head>` of the document:

```html
<html>
    <head>
    ...
    <link rel="stylesheet" href="styles.css">
    ...
<html>
```

`rel="stylesheet"` specifies the relationship of the file that we are linking, in this case the linked file defines the styles of the current HTML file, and it is known as the stylesheet. `href` stands for hyperlink reference, which defines the location of the file to be linked. If `styles.css` is in the same folder as the HTML file, we can simply provide the name of the file as the location.

## CSS Selectors: HTML, Classes and IDs

### HTML Selectors

The Internal Styling example also illustrates the use of HTML selectors. Using HTML selectors targets all HTML elements with the specified HTML tag.

### Classes

Previously, we used HTML elements as selectors when defining CSS rules, either internally or externally. This makes things neater and easier to manage, but does not provide a lot of flexibility. Perhaps we want to apply a certain styling to a group of elements in our web page, but not all `<p>` elements. This can be achieved by using CSS classes, and assigning the relevant HTML element that class as an attribute.&#x20;

A class in a CSS file comprises several characteristics that can be applied to any HTML element to define its visual identity. More than one class can be applied to an element and more than one element can be assigned a class. When defining a set of rules for a class, the selector is prefixed with a period, followed by the user-defined class name, as so:

```css
.card {
  background-color: pink;
}

.face-up {
  font-size: 20px;
}
.face-down {
  font-size: 0px;
}

.page-link {
  font: 'comic-sans';
}
```

```markup
// This is the HTML File

<p class="card face-down">ace of spades</p>
<p class="card face-up">ace of clubs</p>
```

### IDs

We can also define CSS rules for IDs. In this case, the prefix is #. As IDs should be unique, these CSS rules should only be applying to a single HTML element:

```css
#player-card-one {
  border: 3px solid red;
}

#save-button {
  color: green;
}
```

```html
// This is the HTML File

<div id="player-card-one">ace of spades</div>
<button id="save-button">Save!</button>
```

When defining HTML elements in `index.html`, we can initially assign them an ID or a class. IDs are unique, and should not be applied to multiple elements (just like your ID number), but multiple HTML elements can share classes, and HTML elements can belong to multiple classes. Not all HTML elements need to have an ID or a class.

## Cascade

Why _Cascading_ Style Sheets? With so many different ways to define CSS rules, it is not difficult to imagine a situation where there are conflicting rules applying to a single HTML element. The cascade is what determines which rules actually get applied to our HTML. There are 3 main factors in determining the cascade:

1. Specificity,
2. Inheritance, and
3. Rule order.

For Coding Basics, we will only focus on 3. Rule Order. You are free to read up on the rest. Rule order simply means that all the rules are applied sequentially, and in order. So if there 2 or more rules that governed the colour of a `<p>` element, the rule that is applied last will be the one that is preferred.&#x20;

```javascript
<html>
    <head>
    ...
    <link rel="stylesheet" href="styles.css">
      <title> Page Title </title>
         <style>
            p{			
               color: white;
            }
         </style>
   </head>
   <body>
	<p> This text is white </p>
	<p style="color: red;"> This text is RED! </p>
	<p> This text is back to white :) </p>
   </body>
<html>
```

## Common CSS properties

Now that you are familiar with the general syntax:



|                                 Property                                |                       Description                       |
| :---------------------------------------------------------------------: | :-----------------------------------------------------: |
|      [colo](https://www.w3schools.com/cssref/pr\_text\_color.asp)r      |                 Sets the color of a text                |
|       [font](https://www.w3schools.com/cssref/pr\_font\_font.asp)       |     Sets all the font properties in one declaration     |
|        [border](https://www.w3schools.com/cssref/pr\_border.asp)        |        Sets border properties in one declaration        |
| [background](https://www.w3schools.com/cssref/css3\_pr\_background.asp) | Set different background properties in one declaration. |



[Here is a list](http://web.simmons.edu/\~grabiner/comm244/weekthree/css-basic-properties.html) of basic CSS properties you can start experimenting with.

## Basics Starter Code

Take a look at `index.html` from the `basics-starter-code`.&#x20;

Look for the code from `<body>` onwards, and notice that some HTML elements have IDs associated with them.

```html
<h1 id="header">🚀 Basics Day 1: In-Class Exercises 🚀</h1>

<!-- 
  The <div> tag defines a division or a section in an HTML document, 
  and is commonly use as a "container" for nested HTML elements. 
-->

<div class="container">

  <!-- The <p> tag defines a paragraph element. -->
  <p>Input:</p>
  
  <!-- 
    The self-closing <input /> tag represents a field for a user 
    to enter input. 
  -->
  
  <input id="input-field" />
  
  <!-- 
    The self-closing <br /> tag represents a line break - 
    a line's worth of spacing before displaying the next element. 
  -->
  
  <br />
  
  <!-- The <button> tag represents.. you guessed it! a button. -->
  
  <button id="submit-button">Submit</button>
  
  <p>Output:</p>
  
  <div class="output-div" id="output-div"></div>
  
</div>
```

The code within `<script>` tags reference some of these HTML elements, and define the logic that has been associating the Submit button and input/output fields to the main function. We will soon take a closer look at the syntax and concepts that make this work.

### If you skipped to the end

Here's the video that demonstrates a quick way to change the colors on your page.&#x20;

## Exercise

1. <mark style="color:red;background-color:yellow;">Be creative!</mark> <mark style="color:blue;">Explore!</mark> <mark style="color:blue;background-color:red;">Express yourself!</mark>
