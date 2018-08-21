# Basic CSS

Here's how you would set your h2 element's text color to blue:
```css
<h2 style="color: blue;">CatPhotoApp</h2>
```
Note that it is a good practice to end inline style declarations with a ;

### Style block

```css
<style>
</style>
```

Inside that style block, you can create a CSS selector for all h2 elements. 
For example, if you wanted all h2 elements to be red, you would add a style rule that looks like this:

```css
<style>
  h2 {color: red;}
</style>
```
Note that it's important to have both opening and closing curly braces ({ and }) around each element's style rule(s).
You also need to make sure that your element's style definition is between the opening and closing style tags.
Finally, be sure to add a semicolon to the end of each of your element's style rules.


### CSS class declaration

Here's an example CSS class declaration:

```css
<style>
  .blue-text {
    color: blue;
  }
</style>
```
You can see that we've created a CSS class called blue-text within the `<style>` tag.

You can apply a class to an HTML element like this:
```css
<h2 class="blue-text">CatPhotoApp</h2>
```
Note that in your CSS style element, class names start with a period. In your HTML elements' class attribute, the class name does not include the period.

Classes allow you to use the same CSS styles on multiple HTML elements. You can see this by applying your red-text class to the first p element.
```css
<style>
  .red-text {
    color: red;
  }
</style>
```
```html
<h2 class="red-text">CatPhotoApp</h2>
<main>
  <p class="red-text">Click here to view more <a href="#">cat photos</a>.</p>
```

### Fonts

Font size is controlled by the font-size CSS property, like this:
```css
h1 {
  font-size: 30px;
}
```

You can set which font an element should use, by using the font-family property.

```css
h2 {
  font-family: sans-serif;
}
```

#### Import a Google Font

import the Lobster font, need to include before the opening style element

```html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
```
Then can use in the `<style>` block
```css
<style>
  h2 {
    font-family: Lobster;
  }
</style>
```

#### Specify How Fonts Should Degrade

If you wanted an element to use the Helvetica font, but degrade to the sans-serif font when Helvetica wasn't available, 
you will specify it as follows:

```css
p {
  font-family: Helvetica, sans-serif;
}
```
Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.

### Size Your Images

CSS has a property called `width` that controls an element's width.

class larger-iamge

```css
<style>
  .larger-image {
    width: 500px;
  }
</style>
```
code block with class use

```html
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
```css
<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>
```
To apply multiple classes
```html
<img class="class1 class2">
```
### Add Rounded Corners with border-radius

We can round out border corners with a CSS property called `border-radius`

```css
.thick-green-border {
    border-color: green;
    border-width: 10px;
    border-style: solid;
    border-radius: 10px;
  }
 ```
 
### Make Circular Images with a border-radius

In addition to pixels, we can also specify the border-radius using a percentage.

```css
.thick-green-border {
    border-color: green;
    border-width: 10px;
    border-style: solid;
    border-radius: 50%;
  }
 ```
 
 Your image should have a border radius of **50%**, making it perfectly **circular.**

### Give a Background Color to a div Element

We can set an element's background color with the `background-color` property.

For example, if you wanted an element's background color to be green, you'd put this within your style element:

```css
.green-background {
  background-color: green;
}
```
### Set the id of an Element

In addition to classes, each HTML element can also have an `id` attribute.

There are several benefits to using id attributes: You can use an `id` to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

`id` attributes should be **unique.** Browsers won't enforce this, but it is a widely agreed upon best practice. So please don't give more than one element the same `id` attribute.

Here's an example of how you give your `h2` element the `id` of `cat-photo-app`:
```css
<h2 id="cat-photo-app">
```

To give form element the id cat-photo-form
```css
<form id="cat-photo-form" action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    ...
    <button type="submit">Submit</button>
</form>
```

### Use an id Attribute to Style an Element

* like classes, we can style them using CSS.

* `id` is not reusable and should only be applied to one element. 
* An `id` also has a **higher specificity** (importance) than a class.

e.g.

`id` attribute of `cat-photo-element` and give it the background color of green. In your style element

```css
#cat-photo-element {
  background-color: green;
}
```

### Adjust the Padding of an Element

Three important properties control the space that surrounds each HTML element: `padding`, `margin`, and `border`.

```html
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
.red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
  }
  ...
  
  ```
  
  ### Adjust the Margin of an Element
  
  An element's margin controls the amount of space between an element's border and surrounding elements.
```html  
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

negative element margin --> the element will grow larger

```html
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
```css
padding-top 
padding-right 
padding-bottom
padding-left
```

freecode camp to be cont...


