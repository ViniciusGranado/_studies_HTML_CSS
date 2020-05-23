# Class 4: HTML forms

## Concepts

In web pages, forms are the structures we write information into. Just like in real life, form usually has multiple spaces that we can fill with information. Forms are everywhere on the web, in registration pages, login services, and even search engines.

Forms in HTML are represented with the tag `<form>`. Inside of it, we need an element so that the information can be entered, and for this, we use the `<input>` tag. Inputs can be of various types: text, e-mail, telephone, number, and many more. To select the type of input we want, we use the attribute `type`. See some examples below:

    <input type='text'> <!-- Input of type text -->
    <input type='number'> <!-- Input of type number -->
    
    Note that the `<input>` tag doesn't have a closing tag.

The code above will render two fields in the browser, one for entering text, and another for entering numbers.

For a complete list of input types, you can click [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input).

There are two more important attributes that are used on inputs: `id` and `name`, along with the `<label>` tag. Let's each one in detail:

- `id` and `<label>`: They are used together, to link the input to its description. Let's see some example:
    
<label for='text_form'>Name:</label><input type='text' id='text_form'>

    <label for='text_form'>Name:</label><input type='text' id='text_form'>
    
Here we have an input with the `id`=`text_form`. We must enter some description to the input, so the user can know what kind of information he must enter on the field, so we use the tag `<label>`, with the content `Name:` inside of it. This is enough for the user to know what to type, but the browser still doesn't understand that the `<label>` and the `<input>` are linked together. For this, we use the attribute `for`, using the input's `id` as its value, in this case, `text_form`. This way, the browser knows that the label belongs to this determined input. This is really important for a semantic code(we will talk more about semantic in the next classes).

- `name`: The name attribute is a sort of label to the input, but unlike the `<label>` tag, it's used to link the input itself, to the content that the user entered. For example, let's say we have a text input, so the user can enter his name:

        <input type='text' name='user_name'>

When the user clicks the send button, the information sent to the server will be the name attribute, and the content typed by the user, like this:


    "user_name=John Davis"    

To better understand this process, we need first to understand the function of the HTTP protocol, but you don't need to worry about this right now, we will be covering this aspect on future classes. It's important to say that using the `name` attribute is considered good practice, and must be used even if your form will not be submitted.

## Elements saw in this class:

### Tags

- `<form>`: Represents a form. Determines where the form starts and ends.

- `<input>`: Represents an input, an area where the user can enter information. It's used along with the attribute `type`, to determine what type of information will be entered(this also affects the visual aspect of the element). Here are the most common types:

    #### Input types:

    - `text`: Creates a text box, where the user can enter any character.
    - `number`: Creates a number box. The user can only enter with number related characters, such as numbers itself and operators(`+`, `-`, etc.)
    - `password`: It's like a text type, but when information is typed, the content is shown in `*` characters.
    - `range`: Creates a range bar, where the user can drag, and select a value from a determined range.
    - `checkbox`: It's a box that can be checked with a click, It's used with binary answers(yes or no, true or false).
    - `radio`: It's similar to the checkbox, but used when only one option can be selected(an example would be selecting a shirt color).
    - `submit`: It's a button the submit the form content to the server.

- `<select>` and `<option>`: Represents a dropdown list, with options (determined by the `<option>` tag), that the user can select. Its use is similar to the radio button, but used in situations with a big number of options(selecting a city from a state for example).

- `<datalist>`: It's used along with the text input. Uses the `<option>` tag to determine suggested answers. To link a text input and the datalist, the input must have the `list` attribute, and the datalist, the `id` attribute, both with the same value.

- `<textarea>`: Determines a text area. Used when a big amount of text needs to be typed, like a 'suggestions' area of the page. Its size can be determined with the `rows` and `cols` attributes(see more below).

### HTML Attributes

- `action`: Determines where the form will be sent to. It usually contains an URL or a server path.

- `method`: Determines which will be the method used on sending the form. The most common are `POST`, `GET`, `DELETE`, and `PUT`. We will see more about this in future classes.

- `type`: Determines which type an input is gonna be. See more on the `<input>` tag above.

- `name`: It's the name of an element. It's used to identify an element on the form.

- `value`: It's the value entered on an input. Works differently for each type of input.

- `list`: Used in text type inputs, to link the input and a datalist element.

- `rows` and `cols`: Used to determine the number of rows and columns of a `<textarea>`.
