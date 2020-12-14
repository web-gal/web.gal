---
title: <input type="password">
tags:
  - Element
  - Forms
  - HTML
  - HTML Input Types
  - HTML Inputs
  - HTML Password Input
  - HTML forms
  - HTML input tag
  - Input Types
  - Reference
  - Web
  - password
permalink: html/element/input/password
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password'
browserCompact: html.elements.input.input-password
---
{{ HTMLRef("Input_types") }}

`<input>` elements of type **`password`** provide a way for the user to securely enter a password. The element is presented as a one-line plain text editor control in which the text is obscured so that it cannot be read, usually by replacing each character with a symbol such as the asterisk ("*") or a dot ("•"). This character will vary depending on the [user agent](/glossary/user_agent/) and [OS](/glossary/os/).

{{ EmbedInteractiveExample("pages/tabbed/input-password.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

Specifics of how the entry process works may vary from browser to browser; mobile devices, for example, often display the typed character for a moment before obscuring it, to allow the user to be sure they pressed the key they meant to press; this is helpful given the small size of keys and the ease with which the wrong one can be pressed, especially on virtual keyboards.

**Note:** Any forms involving sensitive information like passwords (e.g. login forms) should be served over HTTPS; Many browsers now implement mechanisms to warn against insecure login forms; see [Insecure passwords](/security/insecure_passwords).

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} representing a password, or empty |
| **Events** | {{ domxref("HTMLElement/change_event", "change") }} and {{ domxref("HTMLElement/input_event", "input") }} |
| **Supported Common Attributes** | {{ htmlattrxref("autocomplete", "input") }}, {{ htmlattrxref("inputmode", "input") }}, {{ htmlattrxref("maxlength", "input") }}, {{ htmlattrxref("minlength", "input") }}, {{ htmlattrxref("pattern", "input") }}, {{ htmlattrxref("placeholder", "input") }}, {{ htmlattrxref("readonly", "input") }}, {{ htmlattrxref("required", "input") }}, and {{ htmlattrxref("size", "input") }} |
| **IDL attributes** | `selectionStart`, `selectionEnd`, `selectionDirection`, and `value` |
| **Methods** | {{ domxref("HTMLInputElement.select", "select()") }}, {{ domxref("HTMLInputElement.setRangeText", "setRangeText()") }}, and {{ domxref("HTMLInputElement.setSelectionRange", "setSelectionRange()") }} |

## Value

The {{ htmlattrxref("value", "input") }} attribute contains a {{ domxref("DOMString") }} whose value is the current contents of the text editing control being used to enter the password. If the user hasn't entered anything yet, this value is an empty string (`""`). If the {{ htmlattrxref("required") }} property is specified, then the password edit box must contain a value other than an empty string to be valid.

If the {{ htmlattrxref("pattern", "input") }} attribute is specified, the content of a `password` control is only considered valid if the value passes validation; see {{ anch("Validation") }} for more information.

**Note:** The line feed (U+000A) and carriage return (U+000D) characters are not permitted in a `password` value. When setting the value of a password control, line feed and carriage return characters are stripped out of the value.

## Additional attributes

In addition to the attributes that operate on all [`input`](/html/element/input/) elements regardless of their type, password field inputs support the following attributes:

| Attribute | Description |
| --- | --- |
| `{{ anch("maxlength") }}` | The maximum length the value may be, in UTF-16 characters |
| `{{ anch("minlength") }}` | The minimum length in characters that will be considered valid |
| `{{ anch("pattern") }}` | A regular expression the value must match in order to be valid |
| `{{ anch("placeholder") }}` | An example value to display in the field when the field is empty |
| `{{ anch("readonly") }}` | A Boolean attribute which, if present, indicates that the field's contents should not be editable |
| `{{ anch("size") }}` | The number of characters wide the input field should be |

### {{ htmlattrdef("maxlength") }}

The maximum number of characters (as UTF-16 code units) the user can enter into the password field. This must be an integer value 0 or higher. If no `maxlength` is specified, or an invalid value is specified, the password field has no maximum length. This value must also be greater than or equal to the value of `minlength`.

The input will fail [constraint validation](/guide/html/html5/constraint_validation) if the length of the text entered into the field is greater than `maxlength` UTF-16 code units long.

### {{ htmlattrdef("minlength") }}

The minimum number of characters (as UTF-16 code units) the user can enter into the password entry field. This must be an non-negative integer value smaller than or equal to the value specified by `maxlength`. If no `minlength` is specified, or an invalid value is specified, the password input has no minimum length.

The input will fail [constraint validation](/guide/html/html5/constraint_validation) if the length of the text entered into the field is fewer than `minlength` UTF-16 code units long.

### {{ htmlattrdef("pattern") }}

{{ page("/en-US/docs/Web/HTML/Element/input/text", "pattern-include") }}

Use of a pattern is strongly recommended for password inputs, in order to help ensure that valid passwords using a wide assortment of character classes are selected and used by your users. With a pattern, you can mandate case rules, require the use of some number of digits and/or punctuation characters, and so forth. See the section {{ anch("Validation") }} for details and an example.

{{ page("/en-US/docs/Web/HTML/Element/input/text", "placeholder", 0, 1, 2) }}

### {{ htmlattrdef("readonly") }}

A Boolean attribute which, if present, means this field cannot be edited by the user. Its `value` can, however, still be changed from JavaScript code that directly sets the value of the {{ domxref("HTMLInputElement.value") }} property.

**Note:** Because a read-only field cannot have a value, `required` does not have any effect on inputs with the `readonly` attribute also specified.

{{ page("/en-US/docs/Web/HTML/Element/input/text", "size", 0, 1, 2) }}

## Using password inputs

Password input boxes generally work just like other textual input boxes; the main difference is the obscuring of the content to prevent people near the user from reading the password.

### A simple password input

Here we see the most basic password input, with a label established using the [`label`](/html/element/label/) element.

```html
<label for="userPassword">Password: </label>
<input id="userPassword" type="password">
```

{{ EmbedLiveSample("A_simple_password_input", 600, 40) }}

### Allowing autocomplete

To allow the user's password manager to automatically enter the password, specify the {{ htmlattrxref("autocomplete", "input") }} attribute. For passwords, this should typically be one of the following:

`on`
: Allow the browser or a password manager to automatically fill out the password field. This isn't as informative as using either `current-password` or `new-password`.

`off`
: Don't allow the browser or password manager to automatically fill out the password field. Note that some software ignores this value, since it's typically harmful to users' ability to maintain safe password practices.

`current-password`
: Allow the browser or password manager to enter the current password for the site. This provides more information than `on` does, since it lets the browser or password manager automatically enter currently-known password for the site in the field, but not to suggest a new one.

`new-password`
: Allow the browser or password manager to automatically enter a new password for the site; this is used on "change your password" and "new user" forms, on the field asking the user for a new password. The new password may be generated in a variety of ways, depending on the password manager in use. It may simply fill in a new suggested password, or it might show the user an interface for creating one.

```html
<label for="userPassword">Password:</label>
<input id="userPassword" type="password" autocomplete="current-password">
```

{{ EmbedLiveSample("Autocomplete_sample1", 600, 40) }}

### Making the password mandatory

To tell the user's browser that the password field must have a valid value before the form can be submitted, simply specify the Boolean {{ htmlattrxref("required", "input") }} attribute.

```html
<label for="userPassword">Password: </label>
<input id="userPassword" type="password" required>
<input type="submit" value="Submit">
```

{{ EmbedLiveSample("Making_the_password_mandatory", 600, 40) }}

### Specifying an input mode

If your recommended (or required) password syntax rules would benefit from an alternate text entry interface than the standard keyboard, you can use the {{ htmlattrxref("inputmode", "input") }} attribute to request a specific one. The most obvious use case for this is if the password is required to be numeric (such as a PIN). Mobile devices with virtual keyboards, for example, may opt to switch to a numeric keypad layout instead of a full keyboard, to make entering the password easier. If the PIN is for one-time use, set the {{ htmlattrxref("autocomplete", "input") }} attribute to either `off` or `one-time-code` to suggest that it's not saved.

```html
<label for="pin">PIN: </label>
<input id="pin" type="password" inputmode="numeric">
```

{{ EmbedLiveSample("Specifying_an_input_mode", 600, 40) }}

### Setting length requirements

As usual, you can use the {{ htmlattrxref("minlength", "input") }} and {{ htmlattrxref("maxlength", "input") }} attributes to establish minimum and maximum acceptable lengths for the password. This example expands on the previous one by specifying that the user's PIN must be at least four and no more than eight digits. The {{ htmlattrxref("size", "input") }} attribute is used to ensure that the password entry control is eight characters wide.

```html
<label for="pin">PIN:</label>
<input id="pin" type="password" inputmode="numeric" minlength="4"
       maxlength="8" size="8">
```

{{ EmbedLiveSample("Setting_length_requirements", 600, 40) }}

### Selecting text

As with other textual entry controls, you can use the {{ domxref("HTMLInputElement.select", "select()") }} method to select all the text in the password field.

#### HTML

```html
<label for="userPassword">Password: </label>
<input id="userPassword" type="password" size="12">
<button id="selectAll">Select All</button>

```

#### JavaScript

```js
document.getElementById("selectAll").onclick = function() {
  document.getElementById("userPassword").select();
}
```

#### Result

{{ EmbedLiveSample("Selecting_text", 600, 40) }}

You can also use {{ domxref("HTMLInputElement.selectionStart", "selectionStart") }} and {{ domxref("HTMLInputElement.selectionEnd", "selectionEnd") }} to get (or set) what range of characters in the control are currently selected, and {{ domxref("HTMLInputElement.selectionDirection", "selectionDirection") }} to know which direction selection occurred in (or will be extended in, depending on your platform; see its documentation for an explanation). However, given that the text is obscured, the usefulness of these is somewhat limited.

## Validation

If your application has character set restrictions or any other requirement for the actual content of the entered password, you can use the {{ htmlattrxref("pattern", "input") }} attribute to establish a regular expression to be used to automatically ensure that your passwords meet those requirements.

In this example, only values consisting of at least four and no more than eight hexadecimal digits are valid.

```html
<label for="hexId">Hex ID: </label>
<input id="hexId" type="password" pattern="[0-9a-fA-F]{4,8}"
       title="Enter an ID consisting of 4-8 hexadecimal digits"
       autocomplete="new-password">
```

{{ EmbedLiveSample("Validation_sample1", 600, 40) }}

{{ htmlattrdef("disabled") }}
: This Boolean attribute indicates that the password field is not available for interaction. Additionally, disabled field values aren't submitted with the form.

## Examples

### Requesting a Social Security number

This example only accepts input which matches the format for a [valid United States Social Security Number](https://en.wikipedia.org/wiki/Social_Security_number#Structure). These numbers, used for tax and identification purposes in the US, are in the form "123-45-6789". Assorted rules for what values are permitted in each group exist as well.

#### HTML

```html
<label for="ssn">SSN:</label>
<input type="password" id="ssn" inputmode="numeric" minlength="9" maxlength="12"
    pattern="(?!000)([0-6]\d{2}|7([0-6]\d|7[012]))([ -])?(?!00)\d\d\3(?!0000)\d{4}"
    required autocomplete="off">
<br>
<label for="ssn">Value:</label>
<span id="current"></span>
```

This uses a {{ htmlattrxref("pattern", "input") }} which limits the entered value to strings representing legal Socal Security numbers. Obviously, this regexp doesn't guarantee a valid SSN (since we don't have access to the Social Security Administration's database), but it does ensure the number could be one; it generally avoids values that cannot be valid. In addition, it allows the three groups of digits to be separated by a space, a dash ("-"), or nothing.

The {{ htmlattrxref("inputmode", "input") }} is set to `numeric` to encourage devices with virtual keyboards to switch to a numeric keypad layout for easier entry. The {{ htmlattrxref("minlength", "input") }} and {{ htmlattrxref("maxlength", "input") }} attributes are set to 9 and 12, respectively, to require that the value be at least nine and no more than 12 characters (the former without separating characters between the groups of digits and the latter with them). The {{ htmlattrxref("required", "input") }} attribute is used to indicate that this control must have a value. Finally, {{ htmlattrxref("autocomplete", "input") }} is set to `off` to avoid password managers and session restore features trying to set its value, since this isn't a password at all.

#### JavaScript

This is just some simple code to display the entered SSN onscreen so you can see it. Obviously this defeats the purpose of a password field, but it's helpful for experimenting with the `pattern`.

```js
var ssn = document.getElementById("ssn");
var current = document.getElementById("current");

ssn.oninput = function(event) {
  current.textContent = ssn.value;
}
```

#### Result

{{ EmbedLiveSample("Requesting_a_Social_Security_number", 600, 60) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/forms.html#password-state-(type=password) | {{ Spec2('HTML WHATWG') }} | Initial definition |
| [**HTML 5.1** The definition of '<input type="password">' in that specification](https://www.w3.org/TR/html51/sec-forms.html#password-state-typepassword) | {{ Spec2('HTML5.1') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.input.input-password") }}

## See also

-   [Compatibility of CSS properties](/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)