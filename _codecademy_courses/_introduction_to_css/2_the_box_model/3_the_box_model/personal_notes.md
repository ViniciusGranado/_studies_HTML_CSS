# Class 3: The box model

In this class, we will learn the concept of the box model in HTML.

## Concepts

All elements on an HTML page are interpreted by the browser as a box. If you apply a background-color to any element, you'll see that they always have a rectangular shape. This influences how elements are positioned and displayed on a website.
The box model is a set of properties that defines an element size, and how much space it will occupy on a page. This set is comprised of width and height, padding, border, and margin. We'll see these properties in detail:

- `width` and `height`: Determines the width and height of the content area. We can set these values using the `width` and `height` properties on CSS. We can also use the properties `min-width`, `max-width`, `min-height`, and `max-height`. They ensure an element will maintain its size in a determined range, even in different sizes of screens.

- `padding`: Specifies the amount of space between the content and the border.

- `border`: Specifies the border surrounding the content area. Borders have three values that can be changed: width, style, and color. Let's see an example of border use:

        div{
            border: 1px solid red;
        }

In this case, we are setting a border with 1 pixel thickness, with a 'solid' style, and red color. There are many border styles we can use, and some of the most commons are `solid`, `dotted`, `dashed`, and many more. We can also modify the corners of a border to give it a round shape using the property `border-radius`.

- `margin`: Specifies the amount of space around the element. One important concept is the margin collapse. If two elements, one on top of the other, are using vertical margins(top and bottom), the effective margin will be the size of the biggest element margin. This doesn't occur to horizontal margins, that add each other to form a new margin.

### The overflow property

If the content of an element gets bigger than the element itself (by using a fixed height or width), the content will flow out of the element. In these cases, we can use the property `overflow` to set the behavior of the spilled content. There are three possible values:

- `visible`: Is the default value. The content outside the box is shown normally, trying to adapt to its surroundings.

- `hidden`: The spilled content is not shown, only the content inside the box will be visible.

- `scroll`: A scroll bar is created on the element, allowing the user to see the spilled content.
