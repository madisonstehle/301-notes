# SMACSS and Responsive Web Design
## Sources:
- [Responsive Web Design](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)
- [All About Floats](https://css-tricks.com/all-about-floats/)
- [Floats Explained](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/)
- [Don't Overthink It Grids](https://css-tricks.com/dont-overthink-it-grids/)
- [SMACSS](http://smacss.com/)

## Responsive Web Design

> Responsive Web Design (RWD) is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.

This type of design has three main components:
1. **Flexible layout**
    - The practice of building the layout of a website with a flexible grid (uses **relative** length units), so that it can dynamically resize to any width
    - Aside from `em` units and percentages, CSS3 has relative viewport lengths: `vw`, `vh`, `vmin`, and `vmax`
    - To help identify proportions: target/context = result
2. Media queries
    - provide the avilit to specify different styles for individual browser and device circumstances
    - One way to do this is by using a separate stylesheet for the `@media` rule
        - When a media type evaluates to `true`, then those styles are applied. Logical operators like `and`, `not`, and `only` can be used
    - Common media types are `all`, `screen`, `print`, `tv`, and `braille`. Although there are more thanks to HTML5
3. Flexible media
    - Images, videos, and other media types need to be scalable, changing their size as the the size of the viewport changes.

## Floats

> While floats can still be used for layout, these days, we have much stronger tools for creating layout on web pages. Namely, Flexbox and Grid. 

There are four values for the float property:
- `left`
- `right`
- `none` | ensures the element will NOT float
- `inherit`| assumes the float value from that elements' parent

An element may **collapse** if it contains nothing but floated elements. This is fixable by clearning the float after the floated elements in the container, but before the close of the container. Sometimes, if you don't have that element, there are a few methods to fix the collapse:
- The Empty Div Method
    - Creates an empty `<div>` and applying the `clear: both;` style to it
- The Overflow Method
    - Sets the `overflow` property to the parent element
- The Easy Clearing Method
    - Sets the selector `:after` to clear both, targeting the parent element with an additional class

[Go to Home](README.md)