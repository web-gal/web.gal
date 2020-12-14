---
title: <input type="reset">
tags:
  - Element
  - Form Button
  - Form input
  - Forms
  - HTML
  - HTML forms
  - Input
  - Input Types
  - Reference
  - Reset Button
  - reset
permalink: html/element/input/reset
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/reset'
browserCompact: html.elements.input.input-reset
---
{{ HTMLRef("Input_types") }}

[`input`](/html/element/input/) elements of type **`reset`** are rendered as buttons, with a default {{ event("click") }} event handler that resets all of the inputs in the form to their initial values.

{{ EmbedInteractiveExample("pages/tabbed/input-reset.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

You should usually avoid including reset buttons in your forms. They're rarely useful, and are instead more likely to frustrate users who click them by mistake (often while trying to click the [submit button](/html/element/input/submit)).

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} used as the button's label |
| **Events** | {{ domxref("Element/click_event", "click") }} |
| **Supported common attributes** | {{ htmlattrxref("type", "input") }} and {{ htmlattrxref("value", "input") }} |
| **IDL attributes** | `value` |
| **Methods** | None |

## Value

An `<input type="reset">` element's {{ htmlattrxref("value", "input") }} attribute contains a {{ domxref("DOMString") }} that is used as the button's label. Buttons such as `reset` don't have a value otherwise.

```html
<input type="reset" value="Reset the form">
```

{{ EmbedLiveSample("summary-example3", 650, 30) }}

If you don't specify a `value`, you get an button with the default label (typically "Reset," but this will vary depending on the [user agent](/glossary/user_agent/)):

```html
<input type="reset">
```

{{ EmbedLiveSample("summary-example1", 650, 30) }}

## Using reset buttons

`<input type="reset">` buttons are used to reset forms. If you want to create a custom button and then customize the behaviour using JavaScript, you need to use `[<input type="button">](/html/element/input/button)`, or better still, a [`button`](/html/element/button/) element.

### A simple reset button

We'll begin by creating a simple reset button:

```html
<form>
  <div>
    <label for="example">Type in some sample text</label>
    <input id="example" type="text">
  </div>
  <div>
    <input type="reset" value="Reset the form">
  </div>
</form>

```

This renders like so:

{{ EmbedLiveSample("A_simple_reset_button", 650, 100) }}

Try entering some text into the text field, and then pressing the reset button.

### Adding a reset keyboard shortcut

To add a keyboard shortcut to a reset button — just as you would with any [`input`](/html/element/input/) for which it makes sense — you use the {{ htmlattrxref("accesskey") }} global attribute.

In this example, r is specified as the access key (you'll need to press r plus the particular modifier keys for your browser/OS combination; see {{ htmlattrxref("accesskey") }} for a useful list of those).

```html
<form>
  <div>
    <label for="example">Type in some sample text</label>
    <input id="example" type="text">
  </div>
  <div>
    <input type="reset" value="Reset the form"
     accesskey="r">
  </div>
</form>
```

{{ EmbedLiveSample("Adding_a_reset_keyboard_shortcut", 650, 100) }}

The problem with the above example is that there's no way for the user to know what the access key is! This is especially true since the modifiers are typically non-standard to avoid conflicts. When building a site, be sure to provide this information in a way that doesn't interfere with the site design (for example by providing an easily accessible link that points to information on what the site access keys are). Adding a tooltip to the button (using the {{ htmlattrxref("title") }} attribute) can also help, although it's not a complete solution for accessibility purposes.

### Disabling and enabling a reset button

To disable a reset button, simply specify the {{ htmlattrxref("disabled") }} global attribute on it, like so:

```html
<input type="reset" value="Disabled" disabled>
```

You can enable and disable buttons at run time by simply setting `disabled` to `true` or `false`; in JavaScript this looks like `btn.disabled = true` or `btn.disabled = false`.

**Note**: See the `[<input type="button">](/html/element/input/button#disabling_and_enabling_a_button)` page for more ideas about enabling and disabling buttons.

## Validation

Buttons don't participate in constraint validation; they have no real value to be constrained.

## Examples

We've included simple examples above. There isn't really anything more to say about reset buttons. 

## Specifications

| Specification | Status |
| --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/forms.html#reset-button-state-(type=reset) | {{ Spec2('HTML WHATWG') }} |
| [**HTML 5**](https://www.w3.org/TR/html52/forms.html#reset-button-state-(type=reset) | {{ Spec2('HTML5 W3C') }} |

## Browser compatibility

{{ Compat("html.elements.input.input-reset") }}

## See also

-   [`input`](/html/element/input/) and the {{ domxref("HTMLInputElement") }} interface which implements it.
-   [Forms and buttons](/en-US/docs/Learn/Forms/Basic_native_form_controls#Actual_buttons)
-   [Forms (accessibility)](/accessibility/aria/forms)
-   [HTML forms](/en-US/docs/Learn/HTML/Forms)
-   The [`button`](/html/element/button/) element
-   [Compatibility of CSS properties](/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)