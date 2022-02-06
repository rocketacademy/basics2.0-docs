# 5.2: Cascading Style Sheets (CSS)

## Learning Objectives

By the end of this lesson, you should be able to:

* Define CSS.&#x20;
* Understand Basic CSS Syntax&#x20;
* Use Basic CSS Syntax

### Intro To CSS

In the beginning was html and only html. But programmers wanted to add styling to their web pages to help distinguish themselves from others on the web. Initially, this was not possible. But in October 1994, Håkon Wium Lie introduced Cascading Style Sheets to the world. Today it is better known as CSS.

Built on top of HTML to add more visual control and complexity, CSS specifies styles on an HTML element or set of elements. The CSS code specifies visual properties unrelated to the written content on an HTML page. In practice there are 2 uses for CSS: element styling and layout.

#### Element Styling

CSS helps us change visual properties of HTML elements, such as fonts, background images, or rounded corners on buttons. Together with JS DOM manipulation, we can use CSS to implement visual logic within an application, such as hiding or showing cards and flipping elements 90 degrees.

#### Layout

CSS can help us divide our UI into visual sections. This is one of the most tricky aspects of CSS, because CSS was not originally intended for layout design. CSS content in RA's Bootcamp will focus on implementing UI layouts.

CSS is a declarative language. It doesn't tell the browser what to do but rather describes the rules that the browser then uses to render the page. CSS became popular because it was predictable and forgiving in its syntax. It was also easy to learn.\
The concept of cascading styles is unique to CSS. To cascade means that styles can inherit and overwrite styles through its hierarchy called specificity. More on that in section 2. This concept also allowed for many style sheets to be applied to one page. That is what made CSS so popular.

As a declarative language, CSS uses selectors and declarations to apply styling rules to HTML pages. The syntax for CSS starts with a selector which tells the browser the rules for styling the selected elements. Then a declaration code block is created using open and closing curly braces. Inside the declaration code block rules are created. A rule is made up of a property name followed by a colon and then the value of the property followed by a semi-colon. You can have as many rules as needed. It is the standard to put each rule on its own line in code. The semi-colon tells the browser that the end of the line is reached so be sure to add it at the end of every rule.

#### Sample Syntax

```css
selector{
	property: value;
	property: value;
}
```

In Basics, you will apply CSS styling in two ways:

1. in-line
2. internal

#### In-Line Styling

**In-line styling** is written inside the HTML opening tag as an attribute-value pair. Like this:

```html
<p style=“color: red;”> This text would be red </p>
```

If more than one style declaration is applied:

```html
<p style=“color: red; font-weight: bold;”> This text is red and bold</p>
```

#### Internal Styling

**Internal styling** is placed inside the head tag of the page and is wrapped inside the style tag. In this example, the selector of p is chosen to style all the paragraph tags on the page.

```html
<html>
   <head>
      <title> Page Title </title>
         <style>
            p{			
               color: white;
            }
         </style>
   </head>
   <body>
	<p> This text is white </p>
   </body>
</html>
```

You will be using internal styling in your exercises. **Don't forget to put your CSS declarations between style tags.**

