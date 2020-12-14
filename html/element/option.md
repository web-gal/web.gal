---
title: '<option>: The HTML Option element'
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - Reference
  - Select
permalink: html/element/option
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option'
browserCompact: html.elements.option
---
{{ HTMLRef }}

The **HTML `<option>` element** is used to define an item contained in a [`select`](/html/element/select/), an [`optgroup`](/html/element/optgroup/), or a [`datalist`](/html/element/datalist/) element. As such, `<option>` can represent menu items in popups and other lists of items in an HTML document.

{{ EmbedInteractiveExample("pages/tabbed/option.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | Text, possibly with escaped characters (like `&eacute;`). |
| Tag omission | The start tag is mandatory. The end tag is optional if this element is immediately followed by another `<option>` element or an [`optgroup`](/html/element/optgroup/), or if the parent element has no more content. |
| Permitted parents | A [`select`](/html/element/select/), an [`optgroup`](/html/element/optgroup/) or a [`datalist`](/html/element/datalist/) element. |
| Implicit ARIA role | [`option`](https://w3c.github.io/aria/#option) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLOptionElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("disabled") }}
: If this Boolean attribute is set, this option is not checkable. Often browsers grey out such control and it won't receive any browsing event, like mouse clicks or focus-related ones. If this attribute is not set, the element can still be disabled if one of its ancestors is a disabled [`optgroup`](/html/element/optgroup/) element.

{{ htmlattrdef("label") }}
: This attribute is text for the label indicating the meaning of the option. If the `label` attribute isn't defined, its value is that of the element text content.

{{ htmlattrdef("selected") }}
: If present, this Boolean attribute indicates that the option is initially selected. If the `<option>` element is the descendant of a [`select`](/html/element/select/) element whose {{ htmlattrxref("multiple", "select") }} attribute is not set, only one single `<option>` of this [`select`](/html/element/select/) element may have the `selected` attribute.

{{ htmlattrdef("value") }}
: The content of this attribute represents the value to be submitted with the form, should this option be selected. If this attribute is omitted, the value is taken from the text content of the option element.

## Examples

See [`select`](/html/element/select/) for examples.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<option>' in that specification](https://html.spec.whatwg.org/multipage/form-elements.html#the-option-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<option>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-option-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<option>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.6) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.option") }}

## See also

-   Other form-related elements: [`form`](/html/element/form/), [`legend`](/html/element/legend/), [`label`](/html/element/label/), [`button`](/html/element/button/), [`select`](/html/element/select/), [`datalist`](/html/element/datalist/), [`optgroup`](/html/element/optgroup/), [`fieldset`](/html/element/fieldset/), [`textarea`](/html/element/textarea/), [`keygen`](/html/element/keygen/), [`input`](/html/element/input/), [`output`](/html/element/output/), [`progress`](/html/element/progress/) and [`meter`](/html/element/meter/).