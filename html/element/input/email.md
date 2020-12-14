---
title: <input type="email">
tags:
  - Email
  - Forms
  - HTML
  - HTML forms
  - Input Type
  - Reference
permalink: html/element/input/email
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email'
browserCompact: html.elements.input.input-email
---
{{ HTMLRef }}

[`input`](/html/element/input/) elements of type `**email**` are used to let the user enter and edit an e-mail address, or, if the `[multiple](/html/attributes/multiple)` attribute is specified, a list of e-mail addresses.

{{ EmbedInteractiveExample("pages/tabbed/input-email.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The input value is automatically validated to ensure that it's either empty or a properly-formatted e-mail address (or list of addresses) before the form can be submitted. The {{ cssxref(":valid") }} and {{ cssxref(":invalid") }} CSS pseudo-classes are automatically applied as appropriate to visually denote whether the current value of the field is a valid e-mail address or not.

On browsers that don't support inputs of type `email`, a `email` input falls back to being a standard [`input/text`](/html/element/input/text/) input.

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} representing an e-mail address, or empty |
| **Events** | {{ domxref("HTMLElement/change_event", "change") }} and {{ domxref("HTMLElement/input_event", "input") }} |
| **Supported Common Attributes** | {{ htmlattrxref("autocomplete", "input") }}, {{ htmlattrxref("list", "input") }}, {{ htmlattrxref("maxlength", "input") }}, {{ htmlattrxref("minlength", "input") }}, {{ htmlattrxref("multiple", "input") }}, {{ htmlattrxref("name", "input") }},{{ htmlattrxref("pattern", "input") }}, {{ htmlattrxref("placeholder", "input") }}, {{ htmlattrxref("readonly", "input") }}, {{ htmlattrxref("required", "input") }}, {{ htmlattrxref("size", "input") }}, and {{ htmlattrxref("type", "input") }} |
| **IDL attributes** | `list` and `value` |
| **Methods** | {{ domxref("HTMLInputElement.select", "select()") }} |

## Value

The [`input`](/html/element/input/) element's {{ htmlattrxref("value", "input") }} attribute contains a {{ domxref("DOMString") }} which is automatically validated as conforming to e-mail syntax. More specifically, there are three possible value formats that will pass validation:

1.  An empty string ("") indicating that the user did not enter a value or that the value was removed.
2.  A single properly-formed e-mail address. This doesn't necessarily mean the e-mail address exists, but it is at least formatted correctly. In simple terms, this means `username@domain` or `username@domain.tld`. There's more to it than that, of course; see {{ anch("Validation") }} for a [regular expression](/glossary/regular_expression/) that matches the e-mail address validation algorithm.
3.  If and only if the {{ htmlattrxref("multiple", "input") }} attribute is specified, the value can be a list of properly-formed comma-separated e-mail addresses. Any trailing and leading whitespace is removed from each address in the list.

See {{ anch("Validation") }} for details on how e-mail addresses are validated to ensure that they're formatted properly.

## Additional attributes

In addition to the attributes that operate on all [`input`](/html/element/input/) elements regardless of their type, `email` inputs support the following attributes:

| Attribute | Description |
| --- | --- |
| `{{ anch("list") }}` | The id of the <datalist> element that contains the optional pre-defined autocomplete options |
| `{{ anch("maxlength") }}` | The maximum number of characters the input should accept |
| `{{ anch("minlength") }}` | The minimum number of characters long the input can be and still be considered valid |
| `{{ anch("multiple") }}` | Whether or not to allow multiple, comma-separated, e-mail addresses to be entered |
| `{{ anch("pattern") }}` | A regular expression the input's contents must match in order to be valid |
| `{{ anch("placeholder") }}` | An exemplar value to display in the input field whenever it is empty |
| `{{ anch("readonly") }}` | A Boolean attribute indicating whether or not the contents of the input should be read-only |
| `{{ anch("size") }}` | A number indicating how many characters wide the input field should be |

{{ page("/en-US/docs/Web/HTML/Element/input/text", "list", 0, 1, 2) }}

### {{ htmlattrdef("maxlength") }}

The maximum number of characters (as UTF-16 code units) the user can enter into the `email` input. This must be an integer value 0 or higher. If no `maxlength` is specified, or an invalid value is specified, the `email` input has no maximum length. This value must also be greater than or equal to the value of `minlength`.

The input will fail [constraint validation](/guide/html/html5/constraint_validation) if the length of the text value of the field is greater than `maxlength` UTF-16 code units long. Constraint validation is only applied when the value is changed by the user.

### {{ htmlattrdef("minlength") }}

The minimum number of characters (as UTF-16 code units) the user can enter into the `email` input. This must be an non-negative integer value smaller than or equal to the value specified by `maxlength`. If no `minlength` is specified, or an invalid value is specified, the `email` input has no minimum length.

The input will fail [constraint validation](/guide/html/html5/constraint_validation) if the length of the text entered into the field is fewer than `minlength` UTF-16 code units long. Constraint validation is only applied when the value is changed by the user.

### {{ htmlattrdef("multiple") }}

A Boolean attribute which, if present, indicates that the user can enter a list of multiple e-mail addresses, separated by commas and, optionally, whitespace characters. See {{ anch("Allowing multiple e-mail addresses") }} for an example, or [HTML attribute: multiple](/html/attributes/multiple) for more details.

**Note:** Normally, if you specify the {{ htmlattrxref("required", "input") }} attribute, the user must enter a valid e-mail address for the field to be considered valid. However, if you add the `multiple` attribute, a list of zero e-mail addresses (an empty string, or one which is entirely whitespace) is a valid value. In other words, the user does not have to enter even one e-mail address when `multiple` is specified, regardless of the value of `required`.

### {{ htmlattrdef("pattern") }}

{{ page("/en-US/docs/Web/HTML/Element/input/text", "pattern-include") }}

See the section {{ anch("Pattern validation") }} for details and an example.

{{ page("/en-US/docs/Web/HTML/Element/input/text", "placeholder", 0, 1, 2) }}

{{ page("/en-US/docs/Web/HTML/Element/input/text", "readonly", 0, 1, 2) }}

{{ page("/en-US/docs/Web/HTML/Element/input/text", "size", 0, 1, 2) }}

## Using email inputs

E-mail addresses are among the most frequently-inputted textual data forms on the web; they're used when logging into web sites, when requesting information, to allow order confirmation, for webmail, and so forth. As such, the `email` input type can make your job as a web developer much easier since it can help simplify your work when building the user interface and logic for e-mail addresses. When you create an email input with the proper `type` value, `email`, you get automatic validation that the entered text is at least in the correct form to potentially be a legitimate e-mail address. This can help avoid cases in which the user mistypes their address, or provides an invalid address.

It's important, however, to note that this is not enough to ensure that the specified text is an e-mail address which actually exists, corresponds to the user of the site, or is acceptable in any other way. It simply ensures that the value of the field is properly formatted to be an e-mail address.

**Note**: It's also crucial to remember that a user can tinker with your HTML behind the scenes, so your site _must not_ use this validation for any security purposes. You _must_ verify the e-mail address on the server side of any transaction in which the provided text may have any security implications of any kind.

### A simple email input

Currently, all browsers which implement this element implement it as a standard text input field with basic validation features. The specification does, however, allow browsers latitude on this. For example, the element could be integrated with the user's device's built-in address book to allow picking e-mail addresses from that list. In its most basic form, an `email` input can be implemented like this:

```html
<input id="emailAddress" type="email">
```

{{ EmbedLiveSample('A_simple_email_input', 600, 40)  }}

Notice that it's considered valid when empty and when a single validly-formatted e-mail address is entered, but is otherwise not considered valid. By adding the {{ htmlattrxref("required", "input") }} attribute, only validly-formed e-mail addresses are allowed; the input is no longer considered valid when empty.

### Allowing multiple e-mail addresses

By adding the `[multiple](/html/attributes/multiple)` Boolean attribute, the input can be configured to accept multiple e-mail addresses.

```html
<input id="emailAddress" type="email" multiple>
```

{{ EmbedLiveSample('Allowing_multiple_e-mail_addresses', 600, 40)  }}

The input is now considered valid when a single e-mail address is entered, or when any number of e-mail addresses separated by commas and, optionally, some number of whitespace characters are present.

**Note**: When `multiple` is used, the value _is_ allowed to be empty.

Some examples of valid strings when `multiple` is specified:

-   `""`
-   `"me@example"`
-   `"me@example.org"`
-   `"me@example.org,you@example.org"`
-   `"me@example.org, you@example.org"`
-   `"me@example.org,you@example.org,    us@example.org"`

Some examples of invalid strings:

-   `","`
-   `"me"`
-   `"me@example.org you@example.org"`

### Placeholders

Sometimes it's helpful to offer an in-context hint as to what form the input data should take. This can be especially important if the page design doesn't offer descriptive labels for each [`input`](/html/element/input/). This is where **placeholders** come in. A placeholder is a value that demonstrates the form the `value` should take by presenting an example of a valid value, which is displayed inside the edit box when the element's `value` is "". Once data is entered into the box, the placeholder disappears; if the box is emptied, the placeholder reappears.

Here, we have an `email` input with the placeholder `sophie@example.com`. Note how the placeholder disappears and reappears as you manipulate the contents of the edit field.

```html
<input type="email" placeholder="sophie@example.com">
```

{{ EmbedLiveSample('Placeholders', 600, 40)  }}

### Controlling the input size

You can control not only the physical length of the input box, but also the minimum and maximum lengths allowed for the input text itself.

#### Physical input element size

The physical size of the input box can be controlled using the {{ htmlattrxref("size", "input") }} attribute. With it, you can specify the number of characters the input box can display at a time. In this example the `email` edit box is 15 characters wide:

```html
<input type="email" size="15">
```

{{ EmbedLiveSample('Physical_input_element_size', 600, 40)  }}

#### Element value length

The `size` is separate from the length limitation on the entered e-mail address itself so that you can have fields fit in a small space while still allowing longer e-mail address strings to be entered. You can specify a minimum length, in characters, for the entered e-mail address using the {{ htmlattrxref("minlength", "input") }} attribute; similarly, use {{ htmlattrxref("maxlength", "input") }} to set the maximum length of the entered e-mail address.

The example below creates a 32 character-wide e-mail address entry box, requiring that the contents be no shorter than 3 characters and no longer than 64 characters.

```html
<input type="email" size="32" minlength="3" maxlength="64">
```

{{ EmbedLiveSample("Element_value_length", 600, 40)  }}

### Providing default options

As always, you can provide a default value for an `email` input box by setting its {{ htmlattrxref("value", "input") }} attribute:

```html
<input type="email" value="default@example.com">
```

{{ EmbedLiveSample("Default_value", 600, 40) }}

#### Offering suggested values

Taking it a step farther, you can provide a list of default options from which the user can select by specifying the {{ htmlattrxref("list", "input") }} attribute. This doesn't limit the user to those options, but does allow them to select commonly-used e-mail addresses more quickly. This also offers hints to {{ htmlattrxref("autocomplete", "input") }}. The `list` attribute specifies the ID of a [`datalist`](/html/element/datalist/), which in turn contains one [`option`](/html/element/option/) element per suggested value; each `option`'s `value` is the corresponding suggested value for the email entry box.

```html
<input type="email" size="40" list="defaultEmails">

<datalist id="defaultEmails">
  <option value="jbond007@mi6.defence.gov.uk">
  <option value="jbourne@unknown.net">
  <option value="nfury@shield.org">
  <option value="tony@starkindustries.com">
  <option value="hulk@grrrrrrrr.arg">
</datalist>
```

{{ EmbedLiveSample("Offering_suggested_values", 600, 40) }}

With the [`datalist`](/html/element/datalist/) element and its [`option`](/html/element/option/)s in place, the browser will offer the specified values as potential values for the e-mail address; this is typically presented as a popup or drop-down menu containing the suggestions. While the specific user experience may vary from one browser to another, typically clicking in the edit box presents a drop-down of the suggested e-mail addresses. Then, as the user types, the list is filtered to show only matching values. Each typed character narrows down the list until the user makes a selection or types a custom value.

![Animation: Using keyboard entry to filter the list of suggested e-mail addresses](https://mdn.mozillademos.org/files/14831/html-input-email1.gif)

## Validation

There are two levels of content validation available for `email` inputs. First, there's the standard level of validation offered to all [`input`](/html/element/input/)s, which automatically ensures that the contents meet the requirements to be a valid e-mail address. But there's also the option to add additional filtering to ensure that your own specialized needs are met, if you have any.

**Important**: HTML form validation is _not_ a substitute for scripts that ensure that the entered data is in the proper format.It's far too easy for someone to make adjustments to the HTML that allow them to bypass the validation, or to remove it completely. It's also possible for someone to simply bypass your HTML entirely and submit the data directly to your server. If your server-side code fails to validate the data it receives, disaster could strike when improperly-formatted data (or data which is too large, is of the wrong type, and so forth) is entered into your database.

### Basic validation

Browsers that support the `email` input type automatically provide validation to ensure that only text that matches the standard format for Internet e-mail addresses is entered into the input box. Browsers that implement the specification should be using an algorithm equivalent to the following regular expression:

```js
/^[a-zA-Z0-9.!#$%&'*+\/=?^_`{|}~-]+@[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}
[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?)*$/

```

Tolearn more about how form validation works and how to take advantage of the {{ cssxref(":valid") }} and {{ cssxref(":invalid") }} CSS properties to style the input based on whether or not the current value is valid, see [Form data validation](/en-US/docs/Learn/HTML/Forms/Form_validation).

**Note**: There are known specification issues related to international domain names and the validation of e-mail addresses in HTML. See [W3C bug 15489](https://www.w3.org/Bugs/Public/show_bug.cgi?id=15489) for details.

### Pattern validation

If you need the entered e-mail address to be restricted further than just "any string that looks like an e-mail address," you can use the {{ htmlattrxref("pattern", "input") }} attribute to specify a [regular expression](/glossary/regular_expression/) the value must match for it to be valid. If the {{ htmlattrxref("multiple", "input") }} attribute is specified, each individual item in the comma-delineated list of values must match the [regular expression](/glossary/regular_expression/).

For example, let's say you're building a page for employees of Best Startup Ever, Inc. which will let them contact their IT department for help. In our simplified form, the user needs to enter their e-mail address and a message describing the problem they need help with. We want to ensure that not only does the user provide a valid e-mail address, but for security purposes, we require that the address be an internal corporate e-mail address.

Since inputs of type `email` validate against both the standard e-mail address validation _and_ the specified {{ htmlattrxref("pattern", "input") }}, you can implement this easily. Let's see how:

```css
body {
  font: 16px sans-serif;
}

.emailBox {
  padding-bottom: 20px;
}

.messageBox {
  padding-bottom: 20px;
}

label {
  line-height: 22px;
}

label::after {
  content: ":";
}
```

```html
<form>
 <div class="emailBox">
   <label for="emailAddress">Your e-mail address</label><br>
   <input id="emailAddress" type="email" size="64" maxLength="64" required
          placeholder="username@beststartupever.com" pattern=".+@beststartupever.com"
          title="Please provide only a Best Startup Ever corporate e-mail address">
 </div>

 <div class="messageBox">
   <label for="message">Request</label><br>
   <textarea id="message" cols="80" rows="8" required
             placeholder="My shoes are too tight, and I have forgotten how to dance."></textarea>
 </div>
  <input type="submit" value="Send Request">
</form>

```

{{ EmbedLiveSample("Pattern_validation", 700, 275) }}

Our [`form`](/html/element/form/) contains one [`input`](/html/element/input/) of type `email` for the user's e-mail address, a [`textarea`](/html/element/textarea/) to enter their message for IT into, and an `<input>` of type `["submit"](/html/element/input/submit)`, which creates a button to submit the form. Each text entry box has a [`label`](/html/element/label/) associated with it to let the user know what's expected of them.

Let's take a closer look at the e-mail address entry box. Its {{ htmlattrxref("size", "input") }} and {{ htmlattrxref("maxlength", "input") }} attributes are both set to 64 in order to show room for 64 characters worth of e-mail address, and to limit the number of characters actually entered to a maximum of 64. The {{ htmlattrxref("required", "input") }} attribute is specified, making it mandatory that a valid e-mail address be provided.

An appropriate {{ htmlattrxref("placeholder", "input") }} is provided—`username@beststartupever.com`—to demonstrate what constitutes a valid entry. This string demonstrates both that an e-mail address should be entered, and suggests that it should be a corporate beststartupever.com account. This is in addition to the fact that using type `email` will validate the text to ensure that it's formatted like an e-mail address. If the text in the input box isn't an e-mail address, you'll get an error message that looks something like this:

![](https://mdn.mozillademos.org/files/14855/enter-valid-email-address.png)

If we left things at that, we would at least be validating on legitimate e-mail addresses. But we want to go one step farther: we want to make sure that the e-mail address is in fact in the form "_username_@beststartupever.com". This is where we'll use {{ htmlattrxref("pattern", "input") }}. We set `pattern` to `.+@beststartupever.com`. This simple regular expression requests a string that consists of at least one character of any kind, then an "@" followed by the domain name "beststartupever.com".

Note that this is not even close to an adequate filter for valid e-mail addresses; it would allow things such as " @beststartupever.com" (note the leading space) or "@@beststartupever.com", neither of which is valid. However, the browser runs both the standard e-mail address filter _and_ our custom pattern against the specified text. As a result, we wind up with a validation which says "make sure this resembles a valid e-mail address, and if it is, make sure it's also a beststartupever.com address."

It's advisable to use the {{ htmlattrxref("title") }} attribute along with `pattern`. If you do, the `title` _must_ describe the pattern. That is, it should explain what format the data should take on, rather than any other information. That's because the `title` may be displayed or spoken as part of a validation error message. For example, the browser might present the message "The entered text doesn't match the required pattern." followed by your specified `title`. If your `title` is something like "E-mail address", the result would be the message "The entered text doesn't match the required pattern. E-mail address", which isn't very good.

That's why, instead, we specify the string "Please provide only a Best Startup Ever corporate e-mail address" By doing that, the resulting full error message might be something like "The entered text doesn't match the required pattern. Please provide only a Best Startup Ever corporate e-mail address."

![](https://mdn.mozillademos.org/files/14853/email-pattern-match-bad.png)

**Note**: If you run into trouble while writing your validation regular expressions and they're not working properly, check your browser's console; there may be helpful error messages there to aid you in solving the problem.

## Examples

Here we have an email input with the ID `emailAddress` which is allowed to be up to a maximum of 256 characters long. The input box itself is physically 64 characters wide, and displays the text `user@example.gov` as a placeholder anytime the field is empty. In addition, by using the `[multiple](/html/attributes/multiple)` attribute, the box is configured to allow the user to enter zero or more e-mail addresses, separated by commas, as described in {{ anch("Allowing multiple e-mail addresses") }}. As a final touch, the `[list](/html/attributes/list)` attribute contains the ID of a [`datalist`](/html/element/datalist/) whose [`option`](/html/element/option/)s specify a set of suggested values the user can choose from.

As an added touch, the [`label`](/html/element/label/) element is used to establish a label for the email entry box, with its {{ htmlattrxref("for", "label") }} attribute referencing the `emailAddress` ID of the [`input`](/html/element/input/) element. By associating the two elements in this way, clicking on the label will focus the input element.

```html
<label for="emailAddress">Email</label><br/>
<input id="emailAddress" type="email" placeholder="user@example.gov"
       list="defaultEmails" size="64" maxlength="256" multiple>

<datalist id="defaultEmails">
  <option value="jbond007@mi6.defence.gov.uk">
  <option value="jbourne@unknown.net">
  <option value="nfury@shield.org">
  <option value="tony@starkindustries.com">
  <option value="hulk@grrrrrrrr.arg">
</datalist>
```

{{ EmbedLiveSample('Examples', 600, 50) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/#email-state-(type=email) | {{ Spec2('HTML WHATWG') }} | Initial definition |

## Browser compatibility

The compatibility table on this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.input.input-email") }}

## See also

-   [HTML forms guide](/en-US/docs/Learn/HTML/Forms)
-   [`input`](/html/element/input/)
-   `[<input type="tel">](/html/element/input/tel)`
-   `[<input type="url">](/html/element/input/url)`
-   Attributes:
    -   `[list](/html/attributes/list)`
    -   `[minlength](/html/attributes/minlength)`
    -   `[maxlength](/html/attributes/maxlength)`
    -   `[multiple](/html/attributes/multiple)`
    -   `[pattern](/html/attributes/pattern)`
    -   `[placeholder](/html/attributes/placeholder)`
    -   `[readonly](/html/attributes/readonly)`
    -   `[size](/html/attributes/size)`
-   [Compatibility of CSS properties](/en-US/docs/Learn/HTML/Forms/Property_compatibility_table_for_form_widgets)