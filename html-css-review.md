## Basics

**html terms:**
 ![[tags.png]]
 
 **css terms:**
 ![[css_terms.png]]

**the category of selectors:

 _Type_ selectors target elements by their element type.
 `div { ... }
 
_Class_ selectors allow us to select an element based on the element’s `class` attribute value.
`.awesome { ... }

_ID_ selectors are even more precise than class selectors, as they target only one unique element at a time.
`#shayhowe { ... }

When selectors are combined they should be read from right to left. The selector directly before the opening curly bracket, is known as the _key selector_. The key selector identifies exactly which element the styles will be applied to. Any selector to the left of the key selector will serve as a prequalifier:
```css
.hotdog p {
  background: brown;
}
```


**referencing css:
```html
<head>
  <link rel="stylesheet" href="main.css">
</head>
```


**building structure of html:
![[structure.png]]

1. In general, the `<header>` element may include a heading `<h1~6>`, introductory text, and even navigation `<nav>`.
2. The `<nav>` element identifies a section of major navigational links on a page.
3. The `<section>` element is used to identify a thematic grouping of content, which generally, but not always, includes a heading element.
4. The `<article>` element is used to identify a section of independent, self-contained content that may be independently distributed or reused.
5. If the content is being grouped solely for styling purposes and doesn’t provide value to the outline of a document, use the `<div>` element.
6. A `<div>` is a block-level element that is commonly used to identify large groupings of content, and which helps to build a web page’s layout and design. 
7. A `<span>`, on the other hand, is an inline-level element commonly used to identify smaller groupings of text within a block-level element.
8. The `<aside>` element holds content, such as sidebars, inserts, or brief explanations, that is tangentially related to the content surrounding it.
9. The `<footer>` element identifies the closing or end of a page, article, section, or other segment of a page.
10. Hyperlinks are established using the anchor, `<a>`, inline-level element. In order to create a link from one page (or resource) to another, the `href` attribute, known as a hyperlink reference, is required. The `href` attribute value identifies the destination of the link: 
```html
   <a href="index.html">Home</a>
```


## Box Model
**demos:

![[boxmodel_1.png]]

![[boxmodel_0.png]]

**terms:
1. The `margin` property allows us to set the amount of space that surrounds an element. It can be used to help position elements in a particular place on a page or to provide breathing room, keeping all other elements a safe distance away.
2. The `padding` property is used to provide spacing directly within an element.
3. `border` falls between the padding and margin, providing an outline around an element. The `border` property requires three values: `width`, `style`, and `color`.
4. The `border-radius` property accepts length units, including percentages and pixels, that identify the radius by which the corners of an element are to be rounded.
5. The `box-sizing` property allows us to change exactly how the box model works and how an element’s size is calculated:
```css
*,
*::before,
*::after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  /* for compatibility */
  box-sizing: border-box;
}
```
6. the `border-box` value alters the box model so that any `border` or `padding` property values are included within the `width` and `height` of an element. If we add a `margin`, those values will need to be added to calculate the full box size.

## Position
Essentially, the `float` property allows us to take an element, remove it from the normal flow of a page, and [position it](http://www.smashingmagazine.com/2007/05/01/css-float-theory-things-you-should-know/) to the left or right of its parent element.

clearfix:
```css
.container::before,
.container::after {
  content: "";
  display: table;
}

.container::after {
  clear: both;
}

.container {
  clear: both;
  zoom: 1;
}
```
## Forms
### basics
0. Forms are an essential part of the Internet, as they provide a way for websites to capture information from users and to process requests, and they offer controls for nearly every imaginable use of an application.
1. One of the primary elements used to obtain text from users is the `<input>` element, a self-contained element. The `<input>` [element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Input) uses the `type` attribute to define what type of information is to be captured within the control. Along with setting a `type` attribute, it is best practice to give an `<input>` element a `name` attribute as well. The `name` attribute value is used as the name of the control and is submitted along with the input data to the server:
```html
<input type="text" name="username">
```

2. Another element that’s used to capture text-based data is the `<textarea>` element. The `<textarea>` element differs from the `<input>` element in that it can accept larger passages of text spanning multiple lines. The `<textarea>` element also has start and end tags that can wrap plain text. Because the `<textarea>` element only accepts one type of value, the `type` attribute doesn’t apply here, but the `name` attribute is still used.
```html
<textarea name="comment">Add your comment here</textarea>
```
3. To create a drop-down list we’ll use the `<select>` and `<option>` elements. The `<select>` element wraps all of the menu options, and each menu option is marked up using the `<option>` element:
```html
<select name="day">
  <option value="Friday" selected>Friday</option>
  <option value="Saturday">Saturday</option>
  <option value="Sunday">Sunday</option>
</select>
```
### organizing Form Elements
0. Labels provide captions or headings for form controls, unambiguously tying them together and creating an accessible form for all users and assistive technologies. Created using the `<label>` element, labels should include text that describes the inputs or controls they pertain to.
1. The inline element `<label>` may includes a `for` attribute. The value of the `for` attribute should be the same as the value of the `id` attribute on the form control the label corresponds to:
```html
<label>
  <input type="radio" name="day" value="Friday" checked> Friday
</label>
<label>
  <input type="radio" name="day" value="Saturday"> Saturday
</label>
<label>
  <input type="radio" name="day" value="Sunday"> Sunday
</label>
```

```html
<label for="username">Username</label>
<input type="text" name="username" id="username">
```
2. The `<fieldset>` is a block-level element that wraps related elements, specifically within a `<form>` element, for better organization:
```html
<fieldset>
  <label>
    Username
    <input type="text" name="username">
  </label>
  <label>
    Password
    <input type="text" name="password">
  </label>
</fieldset>
```
3. A `<legend>` provides a caption, or heading, for the `<fieldset>` element. The `<legend>` element wraps text describing the form controls that fall within the fieldset. The markup should include the `<legend>` element directly after the opening `<fieldset>` tag:
```html
<fieldset>
  <legend>Login</legend>
  <label>
    Username
    <input type="text" name="username">
  </label>
  <label>
    Password
    <input type="text" name="password">
  </label>
</fieldset>
```
## Semantic Table
```html
<table>
  <caption>Design and Front-End Development Books</caption>
  <thead>
    <tr>
      <th scope="col">Item</th>
      <th scope="col">Availability</th>
      <th scope="col">Qty</th>
      <th scope="col">Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Don&#8217;t Make Me Think by Steve Krug</td>
      <td>In Stock</td>
      <td>1</td>
      <td>$30.02</td>
    </tr>
    ...
  </tbody>
  <tfoot>
    <tr>
      <td>Subtotal</td>
      <td></td>
      <td></td>
      <td>$135.36</td>
    </tr>
    <tr>
      <td>Tax</td>
      <td></td>
      <td></td>
      <td>$13.54</td>
    </tr>
    <tr>
      <td>Total</td>
      <td></td>
      <td></td>
      <td>$148.90</td>
    </tr>
  </tfoot>
</table>
```
## [references](https://learn.shayhowe.com/html-css/writing-your-best-code/)
