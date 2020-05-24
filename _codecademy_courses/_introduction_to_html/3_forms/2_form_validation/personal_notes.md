# Class 5: Form validation

## Concepts

Form validation is checking whether an information entered on a form is valid or not before sending it to the server. In this class we will see some concepts on client-side validation.
    The first method is using the attribute `required` on an input. In case the user tries to submit the form with this field empty, the browser will render a message saying that filling the field is mandatory.
    When using numerical inputs, we can also use the `min` and `max` attributes to set a range of valid answers. If the user enters an invalid number, the browser will show a message telling the user so. Similar to `min` and `max`, we have `minlength` and `maxlength`, which validates if a given input has the minimal or the maximum number of characters.

Another powerful tool is the `pattern` attribute, that checks if a given input follows a set of rules. For example, a credit card number has 14 to 16 numbers between 0 and 9. We can set these rules to the attribute in this way:

    <input type='number' pattern='[0-9]{14,16}'>

Another use would be a username registry, where you may want the user to only enter numbers or letters, with no special characters. We can use this:

    <input type='password' pattern='[a-zA-Z0-9]+>

This means that the user can enter any character between lower a-z, upper A-Z, and numbers 0-9. The `+` sign means that are no restrictions on the length of the input.

## Elements saw in this class:

### HTML Attributes

- `required`: Defines that an input field filing is mandatory, and the form submission is not possible without it.

- `min`: Defines a minimum value on numerical input.

- `max`: Defines a maximum value on numerical input.

- `minlength`: Defines a minimum length on an input.

- `maxlength`: Defines a maximum length on an input.

- `pattern`: Defines a character pattern that the input must follow.
