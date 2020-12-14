---
title: '<dialog>: The Dialog element'
tags:
  - Dialog
  - Element
  - HTML
  - HTML interactive elements
  - Reference
  - Web
  - polyfill
permalink: html/element/dialog
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog'
browserCompact: html.elements.dialog
---
{{ HTMLRef }}

The **HTML `<dialog>` element** represents a dialog box or other interactive component, such as a dismissable alert, inspector, or subwindow.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [sectioning root](/html/sections_and_outlines_of_an_html5_document#sectioning_roots) |
| Permitted content | [Flow content](/html/content_categories#flow_content) |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content) |
| Implicit ARIA role | [dialog](/accessibility/aria/roles/dialog_role) |
| Permitted ARIA roles | [`alertdialog`](https://w3c.github.io/aria/#alertdialog) |
| DOM interface | {{ domxref("HTMLDialogElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

The `tabindex` attribute must not be used on the `<dialog>` element.

{{ htmlattrdef("open") }}
: Indicates that the dialog is active and can be interacted with. When the `open` attribute is not set, the dialog _shouldn't_ be shown to the user.

## Usage notes

-   [`form`](/html/element/form/) elements can close a dialog if they have the attribute `method="dialog"`. When such a form is submitted, the dialog closes with its {{ domxref("HTMLDialogElement.returnValue", "returnValue") }} property set to the `value` of the button that was used to submit the form.
-   The {{ cssxref('::backdrop') }} CSS pseudo-element can be used to style behind a `<dialog>` element when the dialog is displayed with {{ domxref("HTMLDialogElement.showModal()") }}. For example, to dim unreachable content behind the modal dialog.

## Examples

### Simple example

```html
<dialog open>
  <p>Greetings, one and all!</p>
</dialog>

```

### Advanced example

This example opens a pop-up dialog box that contains a form, when the "Update details" button is clicked.

#### HTML

```html
<!-- Simple pop-up dialog box containing a form -->
<dialog id="favDialog">
  <form method="dialog">
    <p><label>Favorite animal:
      <select>
        <option></option>
        <option>Brine shrimp</option>
        <option>Red panda</option>
        <option>Spider monkey</option>
      </select>
    </label></p>
    <menu>
      <button value="cancel">Cancel</button>
      <button id="confirmBtn" value="default">Confirm</button>
    </menu>
  </form>
</dialog>

<menu>
  <button id="updateDetails">Update details</button>
</menu>

<output aria-live="polite"></output>

```

#### JavaScript

```js
var updateButton = document.getElementById('updateDetails');
var favDialog = document.getElementById('favDialog');
var outputBox = document.querySelector('output');
var selectEl = document.querySelector('select');
var confirmBtn = document.getElementById('confirmBtn');

// "Update details" button opens the <dialog> modally
updateButton.addEventListener('click', function onOpen() {
  if (typeof favDialog.showModal === "function") {
    favDialog.showModal();
  } else {
    alert("The <dialog> API is not supported by this browser");
  }
});
// "Favorite animal" input sets the value of the submit button
selectEl.addEventListener('change', function onSelect(e) {
  confirmBtn.value = selectEl.value;
});
// "Confirm" button of form triggers "close" on dialog because of [method="dialog"]
favDialog.addEventListener('close', function onClose() {
  outputBox.value = favDialog.returnValue + " button clicked - " + (new Date()).toString();
});
```

### Result

{{ EmbedLiveSample("Advanced_example", "100%", 300) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<dialog>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-dialog-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.2** The definition of '<dialog>' in that specification](https://www.w3.org/TR/html52/interactive-elements.html#the-dialog-element) | {{ Spec2('HTML5.2') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.dialog") }}

## Polyfill

Include this polyfill to provide support for browsers without `<dialog>` element.

[dialog-polyfill](https://github.com/GoogleChrome/dialog-polyfill)

## See also

-   The {{ domxref("HTMLDialogElement/close_event", "close") }} event
-   The {{ domxref("HTMLDialogElement/cancel_event", "cancel") }} event
-   [HTML forms guide](/guide/html/forms).
-   The {{ cssxref("::backdrop") }} pseudo-element