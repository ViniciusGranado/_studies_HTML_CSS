# Class 2: CSS visual rules

## Concepts

In this class, we will see some CSS properties to style our pages.

- `font-family`: Changes the font of a text element. The default font on the majority of browsers is Times New Roman. For using another font, it must be installed on the user's computer or imported with the CSS file. An example of use:

        h1{
            font-family: "Courier New";
        }

This changes the font of all `<h1>` tags to Courier New. Note that when the font name has more than one word, it's usually enclosed in quotes.

- `font-size`: Changes the font size of a text element:

        h1{
            font-size: 30px
        }

In this case, all `<h1>` elements will have a font size of 30 pixels.

- `font-weight`: Determines how bold or thin is a text element:

        h1{
            font-weight: bold;
        }

All `<h1>` texts will be bold. The default value is `normal`. Another valid values are: `bolder`, `lighter`, and numeric values: `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, and `900`.

- `text-align`: Represents the alignment of a text element. Its default value is `left`, and can be changed to `center` and `right`:

        h1{
            text-align: center;
        }

All `<h1>` elements will be aligned to the center of the parent element.

- `color`: Changes the color of a text element. Its values can receive color names, hexadecimal values, RGB values, and HSL values. We will see more about these values in the next classes.

        h1{
            color: red;
        }

All `<h1>` elements will be colored red.

- `background-color`: Changes the color of the background of an element. Accepts the same color values as `color` property.

        h1{
            background-color: blue;
        }

All `<h1>` elements will have its background color changed to blue. It's important to say that this property doesn't affect the text inside an element.

- `opacity`: Determines transparency to an element. Its values are numbers between 0 and 1, 1 being totally visible, and 0 totally transparent.

        h1{
            opacity: 0.5;
        }

All `<h1>` elements will have a transparency of 50%. This allows effects like seeing behind an element or keeping the focus on a text above it.

- `background-image`: Put an image as the background of an element. Receives an URL with the image path.

        h1{
            background-image: URL("images/background.png")
        }
