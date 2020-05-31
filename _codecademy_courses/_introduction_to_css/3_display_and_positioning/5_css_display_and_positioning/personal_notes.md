# Class 5: CSS display and positioning

In this class we will see some properties to change how the browser displays an element on the page.

## Concepts

- `position`: This property defines the behavior of an element's positioning on the screen. There are four main values that we will talk about.

    - `static`: Is the default value. The element is positioned following his position in the document, and can't be moved or placed in another position.

    - `relative`: The element is also positioned following the document order, but can be moved using the properties `top`, `bottom`, `left`, and `right`. This properties move the element on the corresponding direction. 

    - `absolute`: This value makes the page ignore his initial position, and place it in an absolute position relative to it's parent element(if the parent element is with a `position` set to another value other than `static`). Can also me moved with directions properties.

    - `fixed`: Works like the `absolute` value, but fix the element on the screen. It will stay on it's position even if the screen is scrolled. It's usually used on fixed headers or side-bars.

- `z-index`: 
