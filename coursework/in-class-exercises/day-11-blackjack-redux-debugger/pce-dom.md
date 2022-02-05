# DOM

## Setup

1. Clone the [DOM starter code](https://github.com/rocketacademy/basics-next-steps-dom).
2. Please refer to [10.2: Browser Applications with DOM](../../../modules/6-advanced/12.1-browser-applications-with-dom.md) if you need a refresher.

## Base

### Creating Elements

#### makeBox

Create an empty function called `makeBox`. `makeBox` will create a new HTML element on screen each time it's called.

If you were to write out the HTML element it would look like the following.

```markup
<div>
    <p>Make Box was Called</p>
    <p>Hello :)</p>
</div>
```

Specifically `makeBox` needs 7 steps.

1. Create the `p` paragraph tag. Something like: `var pOne = document.createElement('p');`
2. Fill the tag with text using `innerText`. Something like: `pOne.innerText = 'haha';`
3. Create a second `p` paragraph tag.
4. Fill the tag with text using `innerText`.
5. Create the `div` tag.
6. Put both `p` tags into the `div` tag using `appendChild`. Something like: `divTag.appendChild( pOne );`
7. Put the `div` tag onto the page with `document.body.appendChild.`

Edit `style.css` so you can clearly identify the box.

```css
div {
  background-color: white;
  border: 2px solid red;
  padding: 10px;
  margin: 10px;
}
```

Call the `makeBox` function inside of `script.js`.

#### makeCard

Create a function `makeCard` that creates card elements with the following HTML structure. See the next code snippet for how to set an `img` tag's `src` attribute in JS.

```markup
<section>
  <p>
    Hello Ducks
  </p>
  <p>
    <img src="https://gblobscdn.gitbook.com/assets%2F-MBhJa4xpezxI4J9lolG%2F-MGrF6rE0CBWVzznQayq%2F-MGrGfwNRi1D6aKWmg4G%2Fducks2.jpeg?alt=media&token=9dff244b-10e8-4fab-ab68-715e09998ff3"/>
  </p>
</section>
```

Here is how we might set an `img` tag's `src` attribute in JS.

```javascript
imgTag.src =
  'https://gblobscdn.gitbook.com/assets%2F-MBhJa4xpezxI4J9lolG%2F-MGrF6rE0CBWVzznQayq%2F-MGrGfwNRi1D6aKWmg4G%2Fducks2.jpeg?alt=media&token=9dff244b-10e8-4fab-ab68-715e09998ff3';
```

Edit `style.css` for `makeCard` to better identify our cards in the UI.

```css
section {
  background-color: grey;
  border: 2px solid blue;
  padding: 10px;
  margin: 10px;
}
```

Call `makeCard` in `script.js`.

### Responding to HTML Events

Update the `makeBox` function to also render a button with the words "Make Card". The corresponding HTML might look like the following, but we will construct it using JS.

```markup
<div>
  <p>Make Box was Called</p>
  <p>Hello :)</p>
  <button>Make Card</button>
</div>
```

Trigger the `makeCard` function when the user clicks the "Make Card" button by calling `addEventListener` on the button with `makeCard` as the callback function.

```javascript
var button = document.createElement('button');
button.innerText = 'Make Card';
button.addEventListener('click', makeCard);
```

## More Comfortable

### Multi-Card Button

Change the `makeCard` function so that it creates multiple cards when the button is clicked. We can create and append elements in a loop inside `makeCard`.

### More Images

1. Get another image URL from the internet
   1. Search for an image
   2. Right click on the image in Chrome
   3. Select "Copy Image Address"
2. Put these images into an array and loop over each image in the array to create the set of cards

### Random Image

Change `makeCard` so that when the user clicks, she gets a single card with a random image.

### Random Number of Images

Add an input to the box created by `makeBox`. The user can fill out a number X in the input. When they click the button, X images appear inside the new card.
