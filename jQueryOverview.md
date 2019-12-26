# Intro to jQuery: **Overview**
## _Pre-Work for 301_: from [Sololearn](https://www.sololearn.com/Play/jQuery#)

Extremely simply put, jQuery is a JavaScript **library** that, well, makes it easier to manipulate HTML from within js.

It selects (queries) HTML elements and perform "actions" on them.

## Set-Up

You can either download a copy of the jQuery library from [the website](https://jquery.com/) or use a CDN:
```html
<html>
    <head>
        <script src="https://code.jquery.com/jquery-3.4.1.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>
    </head>
</html>
```

## Use

> To access jQuery, a `$` is used.

When using jQuery, best practice is to ensure that the HTML fully loads _before_ working with it. This is done by using:
```js
$(document).ready(function(){
    // jQuery code goes here
});
```
Because this is run so often, there is a shorthand version:
```js
$(function(){
    // jQuery code goes here
});
```

### Some Syntax

Basic syntax is `$("selector").action()`, where
- `$` accesses jQuery
- `("selector")` finds the HTML elements
- `action()` is then performed on the element(s)

Basic CSS selectors can be used to target elements in jQuery:
- `$("p")` selects all `<p>` elements
- `$(".demo")` selects all elements with `class="demo"`
- `$("#demo")` selects the `id="demo"` element
- `$("div.menu")` selects `<div>` elements with `class="menu"`
- `$("h1, p")` selects all `<h1>` and `<p>` elements
- `$("div p")` selects all `<p>` elements that are descendants of a `<div>` element
- `$("*")` selects all elements of the DOM

_a list of more selectors can be found [here](jqueryselectors.PNG) courtesy of [sololearn](https://www.sololearn.com/Play/jQuery#)_

### An Example of jQuery's Power

In the below example, the jQuery in the JavaScript will alter the `div` tag to say "Go!" instead of "Start".

#### HTML
```html
<body>
    <div id="start">Start</div>
</body>
```
#### JavaScript
```js
$(function(){
    $("#start").html("Go!");
});
```

[Go to Home](README.md)