# Intro to jQuery: **Attributes & Content**
## _Pre-Work for 301_: from [Sololearn](https://www.sololearn.com/Play/jQuery#)

## Getting Attributes

You can select the _attributes_ (`href`, `src`, `id`, `class`) of HTML elements by using the `attr()` method.

```js
$(function() {
    var val = $("a").attr("href");
    alert(val);
});
```

## Setting and Removing Attributes

You can also use the `attr()` method to set a value for an attribute by putting it as the _second_ parameter.

```js
$(function() {
    $("a").attr("href", "http://www.jquery.com");
});
```

To _remove_ attributes, you can use the `removeAttr()` method. For example: `$("table").removeAttr("class");` removes the `class` attribute from the `<table>` element.

## Getting & Setting Content

There are a few ways to get content from the HTML.

1. The `html()` method
    - This method will grab everything out of the HTML, _including the Markup_
    - `$("p").html();`
2. The `text()` method
    - This method will grab only the text content, without the HTML Markup
    - `$("p").text();`
3. The `val()` method
    - This method allows us to get and set values of form fields (including textboxes, dropdowns, and other similar inputs)
    - `$("#name").val();` will grab the value of the input with `id="name"`

The `html()` and `text()` methods can also change the content (or set the value, in the case of `val()`)of the HTML elements by setting the desired content or value as the parameter of the method.

## Adding Content

Some jQuery methods to add new content _without deleting the existing content_ are:
- `append()` | inserts content at the end of the selected elements
- `prepend()` | inserts content at the beginning of the selected elements
- `after()` | inserts content after the selected elements. 
- `before()` | inserts content before the selected elements. 

[Go to Home](README.md)