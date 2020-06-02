# Class 7: CSS typography

In this class, we will explore CSS typography, the text formatting on the page.

## Concepts

We can use some properties to change how a text will appear on the screen:

- `font-family`: This property changes the type of font of a text.

        h1{
            font-family: Garamond;
        }

In this case, the font of all `<h1>` elements is set to 'Garamond'. To work, the font must be installed on the user's computer, or be imported on the CSS document(using Google fonts services for example). The default font is 'Times New Roman'. It's good practice to limit the numbers of fonts used to 2 or 3.

- `font-weight`: Changes the text boldness.

        h1{
            font-weight: bolder;
        }

In this case, all `<h1>` elements are presented with 'bolder' text. The default value is `normal`.

- `font-style`: Changes the text to italic.

        h1{
            font-style: italic;
        }

It can also be used with the value `normal`, to return the font to its original style.

- `word-spacing`:  Changes the space between the words. The default value is usually 0.25em.

        h1{
            word-spacing: 0.5em;
        }

- `letter-spacing`: Changes the space between the letters.

        h1{
            letter-spacing: 0.02em;
        }

- `text-transform`: Changed the capitalization of the text. There are three common values: `capitalize`, that changes all first letters to upper case, `uppercase`, that changes all letters to upper case, and `lowercase`, that changes all letters to lower case.

        h1{
            text-transform: uppercase;
        }

- `text-align`: Align the text to the given direction. Valid values are `left`, `right`, and `center`.

        h1{
            text-align: center;
        }

- `line-height`: Change the height of the text box, modifying the spaces between the lines. It is important to say that this property doesn't change the font height itself, but the box-model of this font.

        h1{
            line-height: 1.5;
        }
