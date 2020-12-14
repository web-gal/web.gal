---
title: '<output>: The Output element'
tags:
  - Element
  - HTML
  - HTML forms
  - HTML5
  - 'HTML:Flow content'
  - Reference
  - Web
permalink: html/element/output
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/output'
browserCompact: html.elements.output
---
{{ HTMLRef }}

The **HTML Output element** (**`<output>`**) is a container element into which a site or app can inject the results of a calculation or the outcome of a user action.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), [listed](/html/content_categories#form_listed), [labelable](/html/content_categories#form_labelable), [resettable](/html/content_categories#form_resettable) [form-associated element](/html/content_categories#form-associated_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [`status`](https://w3c.github.io/aria/#status) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLOutputElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("for") }}
: A space-separated list of other elements’ {{ htmlattrxref("id") }}s, indicating that those elements contributed input values to (or otherwise affected) the calculation.

{{ htmlattrdef("form") }}
: The [`form`](/html/element/form/) element to associate the output with (its _form owner_). The value of this attribute must be the {{ htmlattrxref("id") }} of a `<form>` in the same document. (If this attribute is not set, the `<output>` is associated with its ancestor `<form>` element, if any.)

: This attribute lets you associate `<output>` elements to `<form>`s anywhere in the document, not just inside a `<form>`. It can also override an ancestor `<form>` element.

{{ htmlattrdef("name") }}
: The element's name. Used in the {{ domxref("HTMLFormElement.elements", "form.elements") }} API.

The `<output>` value, name, and contents are NOT submitted during form submission.

## Examples

In the following example, the form provides a slider whose value can range between `0` and `100`, and an [`input`](/html/element/input/) element into which you can enter a second number. The two numbers are added together, and the result is displayed in the `<output>` element each time the value of any of the controls changes.

```html
<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
  <input type="range" id="b" name="b" value="50" /> +
  <input type="number" id="a" name="a" value="10" /> =
  <output name="result" for="a b">60</output>
</form>

```

{{ EmbedLiveSample('Examples') }}

## Accessibility Concerns

Many browsers implement this element as an `[aria-live](/accessibility/aria/aria_live_regions)` region. Assistive technology will thereby announce the results of UI interactions posted inside it without requiring that focus is switched away from the controls that produce those results.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<output>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-output-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<output>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-output-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.output") }}