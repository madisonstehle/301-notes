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

## Event Handling

### The Basics

There are a number of specific jQuery methods designed to handle events in a shorter and more efficient way. For a list of those from Sololearn, click [here](jqueryeventhandling.PNG).

Another way to handle events in jQuery is by using the `on()` method, and naming the event in the parameter. For example: 

```js
$("p").on("click", function() {
    alert("clicked");
    });
```

You can remove event handlers using the `off()` method.

### The Object

The handler functions can receive event _objects_, which contain properties and methods related to the event, as an argument to the function. Some of those could be:
- `page X, pageY` | the mouse position (X and Y coordinates) at the time the event occurred, relative to the top left of the page
- `type` | the type of event (like 'click')
- `which` | the button or key that was pressed
- `data` | any data that was passed in when the event was bound
- `target` | the DOM element that initiated the event
- `preventDefault()` | prevents the default action of the event
- `stopPropagation()` | stop the event from bubbling up to other elements

The events can also be triggered without the user actually triggering them by using the `trigger()` method.

[Go to Home](README.md)