# Class 4: Changing the box model

## Concepts

When we set the size of a box with the `width` and `length` attributes, we expect that the final element has the exact values we assigned, but that not always happen. If we use the `padding` or `border` configurations, their size is added to the element's box model. This makes it difficult to accurately size a box, but we can avoid this problem with a single attribute.

### The 'box-sizing' property

The `box-size` property sets how the box-model's size of an element is calculated. It's default value is `content-box`, which calculates the final size using the content size, plus the border and padding sizes. Let's see an example:

    div{
        height: 200px;
        width: 300px;
        padding: 10px;
        border: 10px;
    }

In this case, we have a `<div>` with 200px height and 300px width, but adding 10px of border in each size, and 10px of padding on each side, we have extras 40px on the final width and height of the element, making it 240px by 340px.

We can overcome this setting the `box-sizing` to `border-box`:

    div{
        box-sizing: border-box;
        height: 200px;
        width: 300px;
        padding: 10px;
        border: 10px;
    }

In this case, using the `border-box` value, the final element's size will be the 200px by 300px that were set, and the content will shrink to fit the box-model. This makes it much easier to size elements with the desired size. Because this method really helps the developer to adjust the elements on the screen, is normal to set this value to all the elements on the page, using this rule:

    * {
        box-sizing: border-box;
    }

PS: The `*` selects all elements on the page and its children.
