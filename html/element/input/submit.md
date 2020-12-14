---
title: <input type="submit">
tags:
  - Element
  - Form Button
  - Form input
  - HTML
  - HTML forms
  - Input
  - Input Types
  - Reference
  - Submit Form
  - button
  - form
  - submit
  - submit button
permalink: html/element/input/submit
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit'
browserCompact: html.elements.input.input-submit
---
{{ HTMLRef("Input_types") }}

[`input`](/html/element/input/) elements of type **`submit`** are rendered as buttons. When the {{ domxref("Element/click_event", "click") }} event occurs (typically because the user clicked the button), the [user agent](/glossary/user_agent/) attempts to submit the form to the server.

```html
<input type="submit" value="Send Request">
```

{{ EmbedLiveSample("summary-example2", 650, 30) }}

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} used as the button's label |
| **Events** | {{ domxref("Element/click_event", "click") }} |
| **Supported common attributes** | {{ htmlattrxref("type", "input") }} and {{ htmlattrxref("value", "input") }} |
| **IDL attributes** | `value` |
| **Methods** | None |

## Value

An `<input type="submit">` element's {{ htmlattrxref("value", "input") }} attribute contains a {{ domxref("DOMString") }} which is displayed as the button's label. Buttons do not have a true value otherwise.

```html
<input type="submit" value="Send Request">
```

{{ EmbedLiveSample("summary-example3", 650, 30) }}

If you don't specify a `value`, the button will have a default label, chosen by the user agent. This label is likely to be something along the lines of "Submit" or "Submit Query." Here's an example of a submit button with a default label in your browser:

```html
<input type="submit">
```

{{ EmbedLiveSample("summary-example1", 650, 30) }}

## Additional attributes

In addition to the attributes shared by all [`input`](/html/element/input/) elements, `submit` button inputs support the following attributes:

| Attribute | Description |
| --- | --- |
| `{{ anch("formaction") }}` | The URL to which to submit the form's data; overrides the form's {{ htmlattrxref("action", "form") }} attribute, if any |
| `{{ anch("formenctype") }}` | A string specifying the encoding type to use for the form data |
| `{{ anch("formmethod") }}` | The HTTP method ({{ HTTPMethod("get") }} or {{ HTTPMethod("post") }}) to use when submitting the form. |
| `{{ anch("formnovalidate") }}` | A Boolean which, if present, means the form's fields will not be subjected to [constraint validation](/guide/html/html5/constraint_validation) before submitting the data to the server |
| `{{ anch("formtarget") }}` | The [browsing context](/glossary/browsing_context/) into which to load the response returned by the server after submitting the form |

### {{ htmlattrdef("formaction") }}

A string indicating the URL to which to submit the data. This takes precedence over the {{ htmlattrxref("action", "form") }} attribute on the [`form`](/html/element/form/) element that owns the [`input`](/html/element/input/).

This attribute is also available on `[<input type="image">](/html/element/input/image)` and [`button`](/html/element/button/) elements.

### {{ htmlattrdef("formenctype") }}

A string that identifies the encoding method to use when submitting the form data to the server. There are three permitted values:

`application/x-www-form-urlencoded`
: This, the default value, sends the form data as a string after URL encoding the text using an algorithm such as {{ jsxref("encodeURI", "encodeURI()") }}.

`multipart/form-data`
: Uses the {{ domxref("FormData") }} API to manage the data, allowing for files to be submitted to the server. You _must_ use this encoding type if your form includes any [`input`](/html/element/input/) elements of {{ htmlattrxref("type", "input") }} `file` (`[<input type="file">](/html/element/input/file)`).

`text/plain`
: Plain text; mostly useful only for debugging, so you can easily see the data that's to be submitted.

If specified, the value of the `formenctype` attribute overrides the owning form's {{ htmlattrxref("action", "form") }} attribute.

This attribute is also available on `[<input type="image">](/html/element/input/image)` and [`button`](/html/element/button/) elements.

### {{ htmlattrdef("formmethod") }}

A string indicating the HTTP method to use when submitting the form's data; this value overrides any {{ htmlattrxref("method", "form") }} attribute given on the owning form. Permitted values are:

`get`
: A URL is constructed by starting with the URL given by the `formaction` or {{ htmlattrxref("action", "form") }} attribute, appending a question mark ("?") character, then appending the form's data, encoded as described by `formenctype` or the form's {{ htmlattrxref("enctype", "form") }} attribute. This URL is then sent to the server using an HTTP {{ HTTPMethod("get") }} request. This method works well for simple forms that contain only ASCII characters and have no side effects. This is the default value.

`post`
: The form's data is included in the body of the request that is sent to the URL given by the `formaction` or {{ htmlattrxref("action", "form") }} attribute using an HTTP {{ HTTPMethod("post") }} method. This method supports complex data and file attachments.

`dialog`
: This method is used to indicate that the button simply closes the dialog with which the input is associated, and does not transmit the form data at all.

This attribute is also available on `[<input type="image">](/html/element/input/image)` and [`button`](/html/element/button/) elements.

### {{ htmlattrdef("formnovalidate") }}

A Boolean attribute which, if present, specifies that the form should not be validated before submission to the server. This overrides the value of the {{ htmlattrxref("novalidate", "form") }} attribute on the element's owning form.

This attribute is also available on `[<input type="image">](/html/element/input/image)` and [`button`](/html/element/button/) elements.

### {{ htmlattrdef("formtarget") }}

A string which specifies a name or keyword that indicates where to display the response received after submitting the form. The string must be the name of a **browsing context** (that is, a tab, window, or [`iframe`](/html/element/iframe/). A value specified here overrides any target given by the {{ htmlattrxref("target", "form") }} attribute on the [`form`](/html/element/form/) that owns this input.

In addition to the actual names of tabs, windows, or inline frames, there are a few special keywords that can be used:

`_self`
: Loads the response into the same browsing context as the one that contains the form. This will replace the current document with the received data. This is the default value used if none is specified.

`_blank`
: Loads the response into a new, unnamed, browsing context. This is typically a new tab in the same window as the current document, but may differ depending on the configuration of the [user agent](/glossary/user_agent/).

`_parent`
: Loads the response into the parent browsing context of the current one. If there is no parent context, this behaves the same as `_self`.

`_top`
: Loads the response into the top-level browsing context; this is the browsing context that is the topmost ancestor of the current context. If the current context is the topmost context, this behaves the same as `_self`.

This attribute is also available on `[<input type="image">](/html/element/input/image)` and [`button`](/html/element/button/) elements.

## Using submit buttons

`<input type="submit">` buttons are used to submit forms. If you want to create a custom button and then customize the behavior using JavaScript, you need to use `[<input type="button">](/html/element/input/button)`, or better still, a [`button`](/html/element/button/) element.

If you choose to use `<button>` elements to create the buttons in your form, keep this in mind: if there's only one `<button>` inside the [`form`](/html/element/form/), that button will be treated as the "submit" button. So you should be in the habit of expressly specifying which button is the submit button.

### A simple submit button

We'll begin by creating a form with a simple submit button:

```html
<form>
  <div>
    <label for="example">Let's submit some text</label>
    <input id="example" type="text" name="text">
  </div>
  <div>
    <input type="submit" value="Send">
  </div>
</form>

```

This renders like so:

{{ EmbedLiveSample("A_simple_submit_button", 650, 100) }}

Try entering some text into the text field, and then submitting the form.

Upon submitting, the data name/value pair gets sent to the server. In this instance, the string will be `text=_usertext_`, where "usertext" is the text entered by the user, encoded to preserve special characters. Where and how the data is submitted depends on the configuration of the `<form>`; see [Sending form data](/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data) for more details.

### Adding a submit keyboard shortcut

Keyboard shortcuts, also known as access keys and keyboard equivalents, let the user trigger a button using a key or combination of keys on the keyboard. To add a keyboard shortcut to a submit button — just as you would with any [`input`](/html/element/input/) for which it makes sense — you use the {{ htmlattrxref("accesskey") }} global attribute.

In this example, s is specified as the access key (you'll need to press s plus the particular modifier keys for your browser/OS combination. In order to avoid conflicts with the user agent's own keyboard shortcuts, different modifier keys are used for access keys than for other shortcuts on the host computer. See {{ htmlattrxref("accesskey") }} for further details.

Here's the previous example with the s access key added:

```html
<form>
  <div>
    <label for="example">Let's submit some text</label>
    <input id="example" type="text" name="text">
  </div>
  <div>
    <input type="submit" value="Send"
     accesskey="s">
  </div>
</form>
```

For example, in Firefox for Mac, pressing Control-Option-S triggers the Send button, while Chrome on Windows uses Alt+S.

{{ EmbedLiveSample("Adding_a_submit_keyboard_shortcut", 650, 100) }}

The problem with the above example is that the user will not know what the access key is! This is especially true since the modifiers are typically non-standard to avoid conflicts. When building a site, be sure to provide this information in a way that doesn't interfere with the site design (for example by providing an easily accessible link that points to information on what the site access keys are). Adding a tooltip to the button (using the {{ htmlattrxref("title") }} attribute) can also help, although it's not a complete solution for accessibility purposes.

### Disabling and enabling a submit button

To disable a submit button, simply specify the {{ htmlattrxref("disabled") }} global attribute on it, like so:

```html
<input type="submit" value="Disabled" disabled>
```

You can enable and disable buttons at run time by simply setting `disabled` to `true` or `false`; in JavaScript this looks like `btn.disabled = true` or `btn.disabled = false`.

See the `[<input type="button">](/html/element/input/button#disabling_and_enabling_a_button)` page for more ideas about enabling and disabling buttons.

## Validation

Submit buttons don't participate in constraint validation; they have no real value to be constrained.

## Examples

We've included simple examples above. There isn't really anything more to say about submit buttons. There's a reason this kind of control is sometimes called a "simple button."

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/forms.html#submit-button-state-(type=submit) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5**](https://www.w3.org/TR/html52/forms.html#submit-button-state-(type=submit) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.input.input-submit") }}

## See also

-   [`input`](/html/element/input/) and the {{ domxref("HTMLInputElement") }} interface which implements it.
-   [Forms and buttons](/en-US/docs/Learn/Forms/Basic_native_form_controls#Actual_buttons)
-   [Forms (accessibility)](/accessibility/aria/forms)
-   [HTML forms](/en-US/docs/Learn/HTML/Forms)
-   The [`button`](/html/element/button/) element
-   [Compatibility of CSS properties](/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)