# Baisc_CSS_Practice

CSS (Cascading Style Sheets) is used to style and layout the content of the html page. You can alter font, color, size, and spacing of your content, split it into multiple columns, or add animations and other decorative features.

### How does CSS work?

1. The browser loads the HTML.
2. Converts it into DOM (Document Object Model). It represents the document in computer memory.
3. Browser then fetches the related/linked resources as embedded images, videos, linked CSS, etc.
4. Browser parses the CSS, sorts all rules by their sector type into different buckets, based on this it finds out which rules should be applied to which node in the DOM, then attaches the style to them as required. (this process is also known as render tree)
5. Then the render tree is laid out in the structure as it should appear.
6. The visual display of the page is shown. (also knwon as painting)

**CSS Syntax**

` h1 { color:blue; font-size:12px; } `

h1 = selector, color:blue = declaration, color = property, blue = value.

### 3 ways to add styling to an HTML
- external css
- internal css
- inline css

**situation 1**: if both interal and external styles are present
- internal style will apply if it is defined after the external link.
- external style will apply if its link is defined after the internal css.

**Cascading Order of CSS**

Priority:
1. Inline style
2. External and Internal style sheets
3. Browser default

### CSS Comments

```
/* This is a single line comment */
```

```
/* This is 
a multi-line
comment */
```

## 1. CSS Selector

- Simple selectors
- Combinator selectors
- Pseudo-class selectors
- Pseudo-element selectors
- Attribute selectors

### CSS element selector

`p { -styling- }` here p is an element on the page

### CSS id selector

to select an element with a specific id, write hash(#) character, followed by the id of that element.

`#para { -styling- }` here para is an id 

<span style= color:orange>id name cannot start with a number!</span>

### CSS class selector

to select an element with a specific class, write a period(.) character, followed by the class name.

`.cent { -styling- }` here cent is a class

<span style= color:orange>class name cannot start with a number!</span>

**Specific element with that class**

`p.cent { -styling- }`

here only p element with class cent will be selected.

**Element refer to more than one class**

`<p class="center large"> -paragraph- </p>`

here p element will be styled according to class center and large.

### CSS Universal selector

the universal selector asterisk(*) selects all the HTML elements on the page.

`* { -styling- }`

this will affect every element on that HTML page.

### CSS grouping selector

grouping selector selects all the HTML elements with the same style definitions.

`h1, h2, p { -styling- }`

### Styling based on location in the document

**element inside an element (descendant of)**

`li em { -styling- }`

this will select any em that is inside an li.

**element directly after an element (same hierachy)**

`h1 + p { -styling- }`

this will select any p that comes direcly after an h1

### Styling based on state

link: `a:link {--}`

visited: `a:visited {--}`

hover: `a:hover {--}`

active: `a:active {--}`

## 2. CSS Properties

**Some basic CSS properties**

- font-style
- width 
- background-color
- color
- border

### Functions 

some values take the form of a function

**math function** used to do simple math within CSS.

- calc()

**transform functions**

- rotate() 

### @rules

**@import** imports a stylesheet into another CSS stylesheet

**@media** used to create media queries, 

`@media (min-width: 30em) {--}` this example changes the styles based on the viewport width. 

### Shorthands

- font
- background
- padding
- border
- margin

shorthand properties set several values in a single line.

```
padding: 10px 15px 15px 5px
```

is equal to

```
padding-top: 10px;
padding-right: 15px;
padding-bottom: 15px; 
padding-left: 5px;
```

### CSS Box Model 

- Content: The content of the box (text and images)
- Padding: Clears an area around the content (it is transparent)
- Border: A border that goes around the padding and content
- Margin: Clears an area outside the border (it is transparent)

**margin affects the total space that the box will take, but is is not included in the actual size of the box**

### Display property

The display property is used to specify how an element is shown on a web page. The default display value for most elements is block or inline.

**Block-level Elements**

A block-level element ALWAYS starts on a new line and takes up the full width available.

Examples:

- `<div>`
- `<h1>` - `<h6>`
- `<p>`
- `<form>`
- `<header>`
- `<footer>`
- `<section>`

**Inline Elements**

An inline element DOES NOT start on a new line and only takes up as much width as necessary.

Examples:

- `<span>`
- `<a>`
- `<img>`

**Display property values**

- inline
- block
- contents
- flex
- grid

### Position property

The position property specifies the type of positioning method used for an element.

- **static**: The element is positioned according to the normal flow of the document. top, right, bottom, and left properties have no effect. <span style="color:orange;">All elements are positioned static by default</span>.
- **relative**: The element is positioned according to the normal flow of the document, and then adjusted based on the top, right, bottom, and left properties. This means the element can be moved relative to its original position.
- **fixed**: The element is removed from the normal document flow and positioned relative to the viewport. It stays in the same place even when the page is scrolled.
- **absolute**: The element is removed from the normal document flow and positioned relative to its nearest positioned ancestor (i.e., the nearest ancestor with a position other than static). If there is no such ancestor, it is positioned relative to the initial containing block (usually the `<html>` element).
- **sticky**: The element is positioned based on the user's scroll position. It toggles between relative and fixed, depending on the scroll position. It is treated as relative until it crosses a specified point (using top, right, bottom, or left), after which it is treated as fixed.

