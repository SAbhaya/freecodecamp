# Applied Visual Design

Basic tools developers use to 
create their own visual designs.

### Create Visual Balance Using the text-align Property


| text-align    | text output           |
| ------------- |-----------------------|
| justify       | justify the text      |
| center        | centers the text      |
| right         | right-aligns the text |
|left           |(the default) left-aligns the text.|


**usage**

```css
text-align: justify; 

text-align: center;

text-align: right; 

text-align: left;

```
### Adjust the Width of an Element Using the width Property

We can specify the width of an element using the width property in CSS. 
Values can be given in relative length units (such as em), 
absolute length units (such as px), or as a percentage of its containing parent element. Here's an example that changes the width of an image to 220px:

```css
img {
  width: 220px;
}
```


### Adjust the Height of an Element Using the height Property

We can specify the height of an element using the height property in CSS,
similar to the width property. Here's an example that changes the height of an image to 20px:

```css
img {
  height: 20px;
}
```

### Use the strong Tag to Make Text Bold

To make text bold, you can use the `strong` tag. This is often used to draw attention to text and symbolize that it is important. With the `strong` tag, the browser applies the CSS of `font-weight: bold;` to the element.


Example:

```html

<p>Google was founded by Larry Page and Sergey Brin while they were Ph.D. students at <strong>Stanford University</strong>.</p>

```
### Use the u Tag to Underline Text

To underline text, you can use the `u` tag. This is often used to signify that a section of text is important, or something to remember. With the `u` tag, the browser applies the CSS of `text-decoration: underline;` to the element.

> Note
Try to avoid using the u tag when it could be confused for a link. Anchor tags also have a default underlined formatting.

```html
<p>Google was founded by Larry Page and Sergey Brin while they were <u>Ph.D. students</u> at <strong>Stanford University</strong>.</p>
```

### Use the em Tag to Italicize Text

To emphasize text, you can use the `em` tag. This displays text as *italicized*, as the browser applies the CSS of `font-style: italic;` to the element.


**HTML**
```html
<p><em>Google was founded by Larry Page and Sergey Brin while they were <u>Ph.D. students</u> at <strong>Stanford University</strong>.</em></p>

```
**Output**
<div><p><em>Google was founded by Larry Page and Sergey Brin while they were <u>Ph.D. students</u> at <strong>Stanford University</strong>.</em></p></div>

### Use the s Tag to Strikethrough Text

To strikethrough text, which is when a horizontal line cuts across the characters, you can use the `s` tag. It shows that a section of text is no longer valid. With the `s` tag, the browser applies the CSS of  to the element.


**HTML**
```
<s>strikethrough</s>
```

**CSS**
```css
text-decoration: line-through;
```
**Output**
<div><s>strikethrough</s></div>

