# 5.2: Cascading Style Sheets (CSS)

## Learning Objectives

By the end of this lesson, you should be able to:

* [ ] Define CSS.&#x20;
* [ ] Understand and use CSS Syntax&#x20;
* [ ] Add styles to HTML with CSS.
* [ ] Understand what the cascade does.

### Intro To CSS

Built on top of HTML to add more visual control and complexity, CSS specifies styles on an HTML element or set of elements. The CSS code specifies visual properties unrelated to the written content on an HTML page. In practice there are 2 uses for CSS: element **styling** and **layout**.

#### Element Styling

CSS helps us change visual properties of HTML elements, such as fonts, background images, or rounded corners on buttons. Together with JS DOM manipulation, which we will learn in Module 6, we can use CSS to implement visual logic within an application, such as hiding or showing cards and flipping elements 90 degrees.

#### Layout

CSS can help us divide our UI into visual sections. This is one of the most tricky aspects of CSS, because CSS was not _originally_ intended for layout design. CSS content in Rocket's Bootcamp will focus on implementing UI layouts.

CSS is a declarative language. It doesn't tell the browser what to do but rather describes the rules that the browser then uses to render the page. CSS became popular because it was predictable and forgiving in its syntax. It was also easy to learn.

The concept of cascading styles is unique to CSS. To cascade means that styles can inherit and overwrite styles through its hierarchy called _specificity_.&#x20;

## CSS Syntax

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

**Internal styling** allows us to define the style for elements, or groups of elements centrally.&#x20;

#### Sample Syntax

```css
selector {
	property: value;
	property: value;
}
```



As a declarative language, CSS uses selectors and declarations to apply styling rules to HTML pages. The syntax for CSS starts with a selector: the HTML element(s) we want to define style rules for. Then a declaration code block is created using open and closing curly braces. Inside the declaration code block are the style rules, in a similar syntax as in-line styling. You can have as many rules as needed. It is conventional to put each rule on its own line in code.&#x20;

All CSS rules are placed inside the `<head>` tag of the page and is wrapped inside the `<style>` tag. In this example, the selector of p is chosen to style all the paragraph tags on the page.

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
	<p> This text is also white! </p>
   </body>
</html>
```

#### ****

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
