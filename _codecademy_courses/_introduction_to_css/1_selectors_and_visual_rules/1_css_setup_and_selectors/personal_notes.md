# Class 1: CSS setup and selectors

## Concepts

CSS is the language used to style an HTML document. It's responsible for modifying colors, sizes, fonts, shadows, positions, etc. In short, HTML contains the content of the page, and CSS, the style of this content. In this class we will know more about CSS and it's setup.

### The CSS file

A CSS file has the `.css` extension. To connect an HTML file to a CSS, we use the tag `<link>`:

    <link rel='stylesheet' href='css/style.css'>

The attribute `rel` tells the browser what type of file we are linking, in this case, a stylesheet. The `href` is the CSS file path. The path is written using the HTML file directory as reference. In this case, the CSS file(called `style.css`) is in a directory called `css`, which is in the same folder that the HTML file. You can also use a web URL for the file path.

PS: Although they are ways to write CSS code on the HTML file, this is not recommended at all, and it's considered bad practice. If you wanna know more about these methods, you can search for 'inline CSS' and the tag `<style>`.

### CSS basic syntax

The basic CSS syntax looks like this:

    h1{
        font-size: 15px;
        color: blue;
    }

There are three mainly important elements on a css code, the selectors, the properties, and the values. On the example above, the elements are:

    h1: selector
    font-size, color: properties
    15px, blue: values

Basically, the selector chooses which element we will style, in this case, an `<h1>` tag. The properties and values are always put inside curly brackets, which indicates that the given content belongs to a determined selector. The properties (as its name suggests), select the property that will be changed on the given tag. On the example above, we chose to change the font-size and the color of the `<h1>` tag. The value is what will be applied to that property. `font-size` will receive 15 pixels in size, and the `color` will be changed to blue. Numerous properties that can be changed, and we will be talking about them in the next classes.

### CSS selectors

We can select an element on the HTML file by just writing the tag name, as seen above, but if, for example, we write a selector for a `<p>` tag, this will select all paragraphs on the page. This can be a problem if we want to select a single paragraph element. For these cases we can use a variety of element selectors to help us chose the specific element we want to style. Here we will see some of them:

- Class selector: We can add the attribute `class` to an HTML element. This allows us to individually select an element, and add style to it without changing other elements with the same tag. Let's see an example:

        <h1 class='blue_title'>Title Here</h1>

The class selector on CSS is represented by a dot `.`:

        .blue_title{
            color: blue;
        }

We can add the same class to more than one element. This helps us style a group of tags without selecting each of them individually.

- Id selector: Id selector is similar to class selector, but an ID can be used only in one element, becoming more specific. Instead of a dot, we use the hashtag (`#`) character to select an element.

HTML:

        <h1 id='bold_text'>Title here</h1>

CSS:

        #bold_text{
            text-transform: bold;
        }

We can also specify elements with classes or ID's like this:

Consider this code:

    <h1 class="bold_text>Title Here</h1>
    <h2 class="bold_text">Subtitle</h2>

If, for some reason, we want to apply a property only to the `<h1>` that has the `class='bold_text'`, we can select it like this:

    h1.bold_text{
        text-transform: bold;
    }

This style won't be applied to the `<h2>`, even it's have the same class.

- Nested selector:

Another scenario would be if we want a specific tag inside another tag, like this:

    <header>
        <h1>Title</h1>
        <h2>Subtitle</h2>
        <p>Description text</p>
    </div>

    <main>
        <p>Text</p>
        <p>More text</p>
    </main>

If we want to select only the `<p>` inside the `<header>` tag, we can do it like this:

    header p{
        font-size: 15px;
    }

Using a space between the selectors indicates that they are nested, and the browser will look for a paragraph tag inside a header tag. Lets see another example:

    header div.title h2{
        font-size: 15px;
    }

This will look for a `<h2>` that it's inside a `<div>` with the class `title`, that itself is inside a `<header>`. Like this we can really specify an element inside an HTML document.

- Multiple selector:
At last, if we want to add the same styling to different tags, we can use multiple selectors using the comma, like this:

        h1, h2, p{
            color: red
        }

This will and the `color:red` property to all `<h1>`, `<h2>`, AND `<p>` elements. It's important to notice the difference between multiple selectors and nested selectors(that use a space between elements, not a comma).
