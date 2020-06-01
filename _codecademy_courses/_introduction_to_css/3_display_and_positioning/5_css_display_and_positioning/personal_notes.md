# Class 5: CSS display and positioning

In this class, we will see some properties to change how the browser displays an element on the page.

## Concepts

- `position`: This property defines the behavior of an element's positioning on the screen. There are four main values that we will talk about.

    - `static`: Is the default value. The element is positioned following his position in the document, and can't be moved or placed in another position.

    - `relative`: The element is also positioned following the document order, but can be moved using the properties `top`, `bottom`, `left`, and `right`. This property moves the element in the corresponding direction. 

    - `absolute`: This value makes the page ignore his initial position, and place it in an absolute position relative to its parent element(if the parent element is with a `position` set to another value other than `static`). It can also be moved with directions properties.

    - `fixed`: Works like the `absolute` value, but fix the element on the screen. It will stay in its position even if the screen is scrolled. It's usually used on fixed headers or side-bars.

- `z-index`: This property tells the browser how 'back' or 'forward' an element will appear on the screen. It's used when elements overlap each other, so you can define which one of them appears on top of the other. The `z-index` accepts integers as values. It's important to say that the `z-index` property doesn't work with `static` position.

- `display`: This property dictates how an element's box will behave on its form. This alters whether the element will fill the entire width of the page, if the dev can alter the `width` and `height` properties, or they will just follow the content size, if elements can be put on the same line, among other things. Here we will see three common values used on the `display` property.

    - `inline`: This value tells the browser that the element must have a line behavior. The element acts as a word. It doesn't have fixed width and height, and can be put in the same line of other elements.

    - `block`: Elements with this value fill the entire line by default, but the developer can change the width and height values. 

    - `inline-block`: This value combines features of both `inline` and `block` element. It allows the developer to change the `width` and `height` properties, but also allow elements with this value to be in the same line.

- `float`: Just places the element on the left or right side of its container, allowing text and inline elements to wrap around it.

- `clear`: Sets whether an element must be moved below a floating element. 
