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
