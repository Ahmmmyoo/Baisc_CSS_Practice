# Baisc_CSS_Practice

CSS (Cascading Style Sheets) is used to style and layout the content of the html page. You can alter font, color, size, and spacing of your content, split it into multiple columns, or add animations and other decorative features.

**CSS Syntax**

` h1 { color:blue; font-size:12px; } `

h1 = selector, color:blue = declaration, color = property, blue = value.

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

