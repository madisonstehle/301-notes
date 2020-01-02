# Intro to jQuery: **Manipulating CSS and the DOM**
## _Pre-Work for 301_: from [Sololearn](https://www.sololearn.com/Play/jQuery#)

## CSS

There are several methods for CSS manipulation through jQuery:

### Adding and Removing Classes
- The `addClass()` method
    - adds one or more classes to the selected elements as the parameter. To add multiple classes, separate class names with spaces.
    - `$("div").addClass("header");`
- The `removeClass()` method
    - removes one or more classes from the selected elements. To remove multiple classes, separate class names with spaces.
    - `$("div").removeClass("red");`
- The `toggleClass()` method
    - "toggles" between adding/removing classes from the selected elements, meaning that if the specified class exists for the element, it is removed, and if it does not exist, it is added.
    - `$("p").toggleClass("red");`

### Properties
- The `css()` method
    - can be used to get and set CSS property values
    - `$("p").css("background-color", "blue");` selects the `background-color` property and sets its value to `blue`
    - **to set multiple properties, this method uses JSON syntax**
        - `css({"property":"value","property":"value",...});`
- The `width()` and `height()` methods
    - used to set the width and height of HTML elements **without padding, borders, and margins**
    - `$("div").width(100);` or `$("div").height(100);`
- The `innerWidth()` and `innerHeight()` methods
    - used to set the width and height of HTML elements **including padding**
- The `outerWidth()` and `outerHeight()`
    - used to set the width and height of HTML elements **including padding and borders**

## DOM

### Traversal
- The `parent()` method
    - returns the direct parent element of the selected element. It can only traverse a _single_ level up the DOM tree.
    - `$("p").parent();`
- The `parents()` method
    - returns all ancestors of the selected element

For more traversal methods, click [here](jquerydomtraversal.PNG) for an image from Sololearn. 

### Removing
- The `remove()` method
    - removes selected elements from the DOM, as well as its child elements, if any.
- The `empty()` method
    - used to remove the child elements of the selected element(s)

[Go to Home](README.md)