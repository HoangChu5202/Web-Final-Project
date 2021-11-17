# Final Project
This is the final project for my CIS-207 Fundamentals of Web Programming course at Kirkwood Community College.

## Introduction
This is the first time I learn about **GitHub**, **Git**, **Visual Code** and **Markdown**.

This is what I learned in **GitHub**:
- Create a new project
- How to add a file from my computer to GitHub
- How to pull and push a file to GitHub

I also learn some basic thing in markdown too.

## Chapter 1 - Introduction to web development
In this chapter I learned about how internet work, how web application work.

I started to learned about HTML and CSS. 
-  I learn some basic stuff in HTML, relationship between \< html \>, \< head\> and \< body \>
-  In CSS I learn how to change color of background, fornt-size, font-family, margin, padding and boder.

I also learned Five web development issues:
-   Users and usability
-   Cross-browser compatibility
-   User accessibility
-   Search engine optimization
-   Resopsive Web Design

I also learn how to use Figma.


## Chapter 2 - Code, Test, and Validate a Web page
In this chapter I learned about HTML syntax: how to code elements and tags, how to code attributes and how to code comments and whitespace.
In CSS syntax I learned about: How to code CSS style rules and comments and how to code basic selectors.

To test and debug a web page we should Open with Live Sever.
Short cut to indentation on Windows: Shift + alt + F.
‘ is different from '.
To validate a HTML file: [W3C Markup Validation Service](https://validator.w3.org/).
To validate a CSS file: [ W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).


## Chapter 3 - HTML to structure a web page
In this chapter I learned about: How to code the head section.
The <meta> tag can used to:
- Identify the character set used (It will always be utf-8 for html5 documents).
- Provide a description to summarize the contents (It will be displayed in search engine results)
- Provide a list of keywords related to the page content (To possibly help with search engine optimization)
- Aid in the adjustment of content between desktop and mobile screens.
- Assist is
A recommend line to add in head section of all html file is:
```html
<meta name="viewport" content="width=device-width">
```
It will make it easier to adjust content between desktop and mobile screens.

I learned about special blocks of text. It is:
```html
- <pre> tag.
- <blockquote> tag.
- <address> tag.
```

I also learned how to use Google fonts, `<sub>` and `<sup> `tag and how to code character entities.

Using `<div>` tags whenever I need a parent element to group together a bunch of child elements. The <span> tag acts the same but is an inline element. 

Whenever linking to another website I should add the target="_blank" attribute to open the link in a new tab.

## Chapter 4 - CSS to format elements
**Three ways to provide CSS styles for web pages**
- You can use as many external style sheets that you want by link it to your HTML file.
```html
    <link href="styles/base.css" rel="stylesheet">
    <link href="styles/layout.css" rel="stylesheet">
```
- You can also style it in the `<head></head>` section by using <style></style> tags.
```html
<head>
    <link href="styles/main.css" rel="stylesheet">
    <style>
        h1 { color: blue; }
    </style>
</head>
```
- Finally, styles can be applied directly to any element using the style attribute. These are called inline styles.
```html
<h1 style="color: red;">Text</h1>
```
- Absolute measurements: These units are of fixed size. They do not change according to screen size or anything else.
- Relative measurements: These measurements will change based on the screen size. In most browsers, the default font size is 16px.
- Viewport Units: These measurements are relative to the browser’s viewport size. The viewport is the user's visible area of a web page.
**CSS style rule with relational selectors**
- Descendant: A CSS selector for descendants of a specific parent are written as parent child with a space between the element names.
```css
ul a {
    box-sizing: border-box;
}
```
- Adjacent siblings: A CSS selector for adjacent siblings can be written with a plus sign separating their names.
```css
h2 + p {
    font-weight: bold;
}
```
- Child: A CSS selector child selector is written with a greater than sign between two elements.
```css
main > p { font-size: 80%; }
```
- General sibling: A CSS selector for sibling elements is written with a tilde symbol between two elements.
```css
h2 ~ p { margin-left: 2em; }
```
**How the cascade rules work**
- <u>*Specificity*</u> is the means by which browsers decide which CSS property values are the most relevant to an element and, therefore, will be applied. 

The following list of selector types increases by specificity:

- (+0) Universal selector (`*`) and combinators (`+, >, ~`) have no effect on specificity.
- (+1) Type selectors (like `h1`) and pseudo-elements (like `::before`) have a low effect  on specificity.
- (+10) Class selectors (like `.example`), attributes selectors (like `[type="radio"]`) and pseudo-classes (like `:hover`) have a medium effect on specificity.
- (+100) ID selectors (like `#example`) have a high effect on specificity.
- (Highest) Inline styles added to an element always overwrite any styles in external stylesheets, and thus can be thought of as having the highest specificity.
- (Ultimate) The `!important`rule can be used on any style declaration to override any other declarations. Using `!important` should be avoided because it makes debugging more difficult by breaking the natural cascading in your stylesheets.


## Chapter 5 - CSS Box Model
**Box model**

The CSS box model consists of 4 components:

- The content: which may include text and images.
- `padding`: the space between the content and the border.
- `border`: the division between the padding and margin.
- `margin`: the space outside of the border (the space between elements).

Current versions of all browsers use  “width or height + padding + border = actual width or height” box model.
Using `box-sizing: border-box` to make the calculate correct.

**Margin and Padding**
```
padding/margin: 5px 10px 15px 20px;
```
It will go in order: top, right, bottom, left.

Padding, margin, and border can be controlled on all four sides: top, right, bottom, and left.

- `padding-top, margin-top, border-top`
- `padding-right, margin-right, border-right`
- `padding-bottom, margin-bottom, border-bottom`
- `padding-left, margin-left, border-left`

**CSS reset**
Some developers will just use a [CSS reset file](https://meyerweb.com/eric/tools/css/reset/) to clear default margin and padding so they can define their own values.

OR you can go to CSS file and set in wild card selector:
```css
* {
    margin: 0;
    padding: 0;
}
```

**Border**

`border`: This property sets the width, style and color of all four sides on one line. Or it can be written as separate properties.
- `border-width`
- `border-style`
- `border-color`

`border-radius`: applies rounded corners to a box. Individual corners can also be modified.
- `border-top-left-radius`
- `border-top-right-radius`
- `border-bottom-right-radius`
- `border-bottom-left-radius`

`box-shadow`: applies a drop shadow to a box.

**Background**

`background`: allows you to change the background color, image, repeat, attachment, and position all on one line.
Or it can be written as separate properties.
- `background-color`: specifies a color as the background.
- `background-image`: specifies an image as the background.
- `background-repeat`: specifies if and how an image repeats horizontally and veritcally.
- `background-attachment`: determines if a background is scrollable or fixed.
- `background-position`: the horizontal and vertical position of a background image.

`linear-gradient()`: a special property that works with background or background-image to set a multi-colored background.

## Chapter 6 - CSS for Page Layout

**How to float and clear elements**

- When `float: right;` is added to the aside selector, both main and footer will wrap to the left of the aside.
- If you do not want a sibling element to wrap, add a `clear: both;` statement to its selector.
- For a two-column layout where the main content is fluid and the aside is fixed, you use CSS to set the parent container width to a percent and don't set the main width

**CSS Properties for creating text columns**

- You can use `column-count`, `column-gap`, and `column-rule` CSS properties to make the text easier to read on desktop devices. A fourth property `column-span` is not supported by every browser.

**Ways to position an element**

- Position takes in five values: `static`, `relative`, `absolute`, `fixed`, and `sticky`.
- The default position of every element is `static`.
- To modify the position, you'll need to apply the top, bottom, right, and left properties and in that way specify where and how much you want to move the element.

**z-index**

- The z-index CSS property can be added to any positioned element to create a stack order. Elements with higher values will be positioned on top of elements with smaller values.
- The default value is 0. Negative number will be placed behind them.

## Chapter 7 - Lists, Links, Navigation

**How to code list**

- There are two common list in html is `<ol>` and `<ul>`.
- There is a third one called description lists `<dl>`.
- To create a nested list, you nest a `<ul>` or `<ol>` element within an `<li>` element.
- You can use the CSS `list-style-type` and `list-style-image` properties to change the bullet or number style in an unordered or ordered list.

**How to link to another page**

- Note the accesskey and tabindex attributes. An access key is a keystroke combination that can be used to activate a link. The tab order is the sequence that the links will be tabbed to when the user presses the Tab key.

**How to create links to placeholders**

To create a placeholder, simply add an id attribute to any element on the page. Headings are usually a good place to put them.
```html
<h2 id="reason1">Our modular book organization gives the trainer flexibility</h2>
```
To create a link that goes to a placeholder on the same page, you code the href attribute as # followed by the id attribute of the placeholder element
```html
<a href="#reason1">Modular book organization</a>
```


