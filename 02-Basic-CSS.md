
Basic CSS
=========

Here's how you would set your h2 element's text color to blue:

``` css
<h2 style="color: blue;">CatPhotoApp</h2>
```

Note that it is a good practice to end inline style declarations with a ;

### Style block

``` css
<style>
</style>
```

Inside that style block, you can create a CSS selector for all h2 elements. For example, if you wanted all h2 elements to be red, you would add a style rule that looks like this:

``` css
<style>
  h2 {color: red;}
</style>
```

Note that it's important to have both opening and closing curly braces ({ and }) around each element's style rule(s). You also need to make sure that your element's style definition is between the opening and closing style tags. Finally, be sure to add a semicolon to the end of each of your element's style rules.

### CSS class declaration

Here's an example CSS class declaration:

``` css
<style>
  .blue-text {
    color: blue;
  }
</style>
```

You can see that we've created a CSS class called blue-text within the `<style>` tag.

You can apply a class to an HTML element like this:

``` css
<h2 class="blue-text">CatPhotoApp</h2>
```

Note that in your CSS style element, class names start with a period. In your HTML elements' class attribute, the class name does not include the period.

Classes allow you to use the same CSS styles on multiple HTML elements. You can see this by applying your red-text class to the first p element.

``` css
<style>
  .red-text {
    color: red;
  }
</style>
```

``` html
<h2 class="red-text">CatPhotoApp</h2>
<main>
  <p class="red-text">Click here to view more <a href="#">cat photos</a>.</p>
```

### Fonts

Font size is controlled by the font-size CSS property, like this:

``` css
h1 {
  font-size: 30px;
}
```

You can set which font an element should use, by using the font-family property.

``` css
h2 {
  font-family: sans-serif;
}
```

#### Import a Google Font

import the Lobster font, need to include before the opening style element

``` html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
```

Then can use in the `<style>` block

``` css
<style>
  h2 {
    font-family: Lobster;
  }
</style>
```

#### Specify How Fonts Should Degrade

If you wanted an element to use the Helvetica font, but degrade to the sans-serif font when Helvetica wasn't available, you will specify it as follows:

``` css
p {
  font-family: Helvetica, sans-serif;
}
```

Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.

### Size Your Images

CSS has a property called `width` that controls an element's width.

class larger-iamge

``` css
<style>
  .larger-image {
    width: 500px;
  }
</style>
```

code block with class use

``` html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }
  .smaller-image{
    width: 100px;
  }

 ...
</style>

<h2 class="red-text">CatPhotoApp</h2>
<main>
  <p class="red-text">Click here to view more <a href="#">cat photos</a>.</p>
  <a href="#"><img class="smaller-image" src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>
  <div>
    <p>Things cats love:</p>
    ....
  
  </ol>
  </div>
  
  <form action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
  ......  <button type="submit">Submit</button>
  </form>
</main>
```

### Add Borders Around Your Elements

CSS borders have properties like style, color and width

For example, if we wanted to create a red, 5 pixel border around an HTML element, we could use this class:

``` css
<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>
```

To apply multiple classes

``` html
<img class="class1 class2">
```

### Add Rounded Corners with border-radius

We can round out border corners with a CSS property called `border-radius`

`css .thick-green-border {     border-color: green;     border-width: 10px;     border-style: solid;     border-radius: 10px;   }`

### Make Circular Images with a border-radius

In addition to pixels, we can also specify the border-radius using a percentage.

`css .thick-green-border {     border-color: green;     border-width: 10px;     border-style: solid;     border-radius: 50%;   }`

Your image should have a border radius of **50%**, making it perfectly **circular.**

### Give a Background Color to a div Element

We can set an element's background color with the `background-color` property.

For example, if you wanted an element's background color to be green, you'd put this within your style element:

``` css
.green-background {
  background-color: green;
}
```

### Set the id of an Element

In addition to classes, each HTML element can also have an `id` attribute.

There are several benefits to using id attributes: You can use an `id` to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

`id` attributes should be **unique.** Browsers won't enforce this, but it is a widely agreed upon best practice. So please don't give more than one element the same `id` attribute.

Here's an example of how you give your `h2` element the `id` of `cat-photo-app`:

``` css
<h2 id="cat-photo-app">
```

To give form element the id cat-photo-form

``` css
<form id="cat-photo-form" action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    ...
    <button type="submit">Submit</button>
</form>
```

### Use an id Attribute to Style an Element

-   like classes, we can style them using CSS.

-   `id` is not reusable and should only be applied to one element.
-   An `id` also has a **higher specificity** (importance) than a class.

e.g.

`id` attribute of `cat-photo-element` and give it the background color of green. In your style element

``` css
#cat-photo-element {
  background-color: green;
}
```

### Adjust the Padding of an Element

Three important properties control the space that surrounds each HTML element: `padding`, `margin`, and `border`.

``` html
<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }
  
  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 10px;
  }
</style>
<h5 class="injected-text">margin</h5>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```

Change the padding of your blue box to match that of your red box.

```css

...
  .red-box {  background-color: crimson;
              color: #fff;
              padding: 20px; }

  .blue-box { background-color: blue;
              color: #fff;
              padding: 20px; } 
...

```

### Adjust the Margin of an Element

An element's margin controls the amount of space between an element's border and surrounding elements.

``` html
<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }
  
  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: 20px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
    margin: 10px;
  }
</style>
<h5 class="injected-text">margin</h5>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```

### Add a Negative Margin to an Element

An element's margin controls the amount of space between an element's border and surrounding elements.

negative element margin --&gt; the element will grow larger

``` html
<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }
  
  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: -15px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
    margin: 20px;
  }
</style>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```

### Add Different Padding to Each Side of an Element

adjust properties:

``` css
padding-top 
padding-right 
padding-bottom
padding-left
```

Give the blue box a padding of 40px on its top and left side, but only 20px on its bottom and right side

``` css
...

 .blue-box {
    background-color: blue;
    color: #fff;
    padding-top: 40px;
    padding-left: 40px;
    padding-bottom: 20px;
    padding-right: 20px;
  }
```

### Add Different Margins to Each Side of an Element

control the margin, adjust properties:

``` css
margin-top
margin-right
margin-bottom
margin-left
```

Give the blue box a margin of 40px on its top and left side, but only 20px on its bottom and right side.

``` css
 .blue-box {
    background-color: blue;
    color: #fff;
    margin-top: 40px;
    margin-right: 20px;
    margin-bottom: 20px;
    margin-left: 40px;
  }
```

### Clockwise Notation to Specify the Padding of an Element

``` css
padding: 10px 20px 10px 20px;
```

These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific padding instructions.

### Use Clockwise Notation to Specify the Margin of an Element

Instead of specifying an element's `margin-top`, `margin-right`, `margin-bottom`, and `margin-left` properties individually, we can specify them all in one line, like this:

``` css
margin: 10px 20px 10px 20px;
```

### Use Attribute Selectors to Style Elements

We can use the `[attr=value]` attribute selector to style

``` css
[type="checkbox"]{
    margin-top:10px;
    margin-bottom: 15px;

  } 
</style>
```

### Understand Absolute versus Relative Units

Relative unit: `em`, `rem`

`em` is based on the size of an element's font

example:

``` css

.red-box {
    background-color: red;
    margin: 20px 40px 20px 40px;
    padding: 1.5em
    
  }
  
```

### Style the HTML Body Element

Every HTML page has a body element.

We can prove that the body element exists here by giving it a background-color of black.

```css
<style>
body{
    background-color:black;
}
</style>
```

### Inherit Styles from the Body Element

body element's styles:- color:green, and font-family:monospace, 
other elements will inherit body element's styles.

```html
<style>
  body {
    background-color: black;
    color: green;
    font-family: monospace;
  }

</style>
<h1>Hello World</h1>
```

### Prioritize One Style Over Another

Gives `h1` color **pink**

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text{
    color: pink;
  }
</style>
<h1 class="pink-text">Hello World!</h1>
```
### Override Styles in Subsequent CSS

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
  .blue-text{
    color: blue;    
  }
</style>
<h1 class="pink-text blue-text">Hello World!</h1>

```
Applying multiple class attributes to a HTML element is done with a space 
between them like this:

```css
class="class1 class2"
```

Note: It doesn't matter which order the classes are listed in the HTML element.

However, the order of the class declarations in the `<style>` section 
are what is important. The second declaration will always take precedence over the first. 
Because `.blue-text` is declared second, it overrides the attributes of `.pink-text`

### Override Class Declarations by Styling ID Attributes

Override `pink-text` and `blue-text` classes, 
and make your `h1` element orange, by giving the `h1` element an `id` and 
then styling that `id`.

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
  #orange-text{
    color:orange;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text">Hello World!</h1>

```

### Override Class Declarations with Inline Styles

Use an `inline style` to try to make our `h1` element white. Remember, in line styles look like this:

```html
<h1 style="color: green;">
```

code

```html
<style>
  body {
    background-color: black; 
    font-family: monospace;
    color: green;
  }
  #orange-text {
    color: orange;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 style="color: white;" id="orange-text" class="pink-text blue-text">Hello World!</h1>

```

### Override All Other Styles by using Important

Use keyword `!important` to override all other styles.


```html

<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  #orange-text {
    color: orange;
  }
  .pink-text {
    color: pink !important;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white">Hello World!</h1>

```

### Use Hex Code for Specific Colors

In CSS, we can use 6 hexadecimal digits to represent colors, 
two each for the red (R), green (G), and blue (B) components.

e.g

```css
body {
  color: #000000;
}
```

### Use Hex Code to Mix Colors


```html

<style>
  .red-text {
    color: #FF0000;
  }
  .green-text {
    color: #00FF00;
  }
  .dodger-blue-text {
    color: #1E90FF;
  }
  .orange-text {
    color: #FFA500;
  }
</style>

<h1 class="red-text">I am red!</h1>

<h1 class="green-text">I am green!</h1>

<h1 class="dodger-blue-text">I am dodger blue!</h1>

<h1 class="orange-text">I am orange!</h1>

```

### Use Abbreviated Hex Code

Example:

Red's hex code #FF0000 can be shortened to #F00. 
This shortened form gives one digit for red, one digit for green, and one digit for blue.

```html
<style>
  .red-text {
    color: #F00;
  }
  .fuchsia-text {
    color: #F0F;
  }
  .cyan-text {
    color: #0FF;
  }
  .green-text {
    color: #0F0;
  }
</style>

<h1 class="red-text">I am red!</h1>

<h1 class="fuchsia-text">I am fuchsia!</h1>

<h1 class="cyan-text">I am cyan!</h1>

<h1 class="green-text">I am green!</h1>
```

### Use RGB values to Color Elements

Another way you can represent colors in CSS is by using `RGB` values.

The `RGB` value for black looks like this:
```
rgb(0, 0, 0)
```
The `RGB` value for white looks like this:
```
rgb(255, 255, 255)
```
Instead of using six hexadecimal digits like you do `with hex code, 
with `RGB` you specify the brightness of each color with a number between 0 and 255.

```css
<style>
  body {
    background-color: rgb(0,0,0);
  }
</style>
```

### Use RGB to Mix Colors

```html
<style>
  .red-text {
    color: rgb(255, 0, 0);
  }
  .orchid-text {
    color: rgb(218, 112, 214);
  }
  .sienna-text {
    color: rgb(160, 82, 45);
  }
  .blue-text {
    color: rgb(0, 0, 255);
  }
</style>

<h1 class="red-text">I am red!</h1>

<h1 class="orchid-text">I am orchid!</h1>

<h1 class="sienna-text">I am sienna!</h1>

<h1 class="blue-text">I am blue!</h1>
```

### Use CSS Variables to change several elements at once

CSS Variables are a powerful way to change many CSS style properties at once by changing only one value.

[pengu](pengu.html)

### Create a custom CSS Variable

To create a CSS Variable, you just need to give it a name with two dashes in front of it and assign it a value like this:

```css
--penguin-skin: gray;
```
This will create a variable named `--penguin-skin` and assign it the value of gray.

### Use a custom CSS Variable

After you create your variable, you can assign its value to other CSS properties by referencing the name you gave it.

```css
background: var(--penguin-skin);
```

This will change the background of whatever element you are targeting to gray because that is the value of the --penguin-skin variable.

### Attach a Fallback