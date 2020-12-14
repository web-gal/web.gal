---
title: <optgroup>
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - Reference
  - Web
permalink: html/element/optgroup
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup'
browserCompact: html.elements.optgroup
---
{{ HTMLRef }}

The **HTML `<optgroup>` element** creates a grouping of options within a [`select`](/html/element/select/) element.

{{ EmbedInteractiveExample("pages/tabbed/optgroup.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | None. |
| Permitted content | Zero or more [`option`](/html/element/option/) elements. |
| Tag omission | The start tag is mandatory. The end tag is optional if this element is immediately followed by another `<optgroup>` element, or if the parent element has no more content. |
| Permitted parents | A [`select`](/html/element/select/) element. |
| Implicit ARIA role | [`group`](https://w3c.github.io/aria/#group) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLOptGroupElement") }} |

{{ Note("Optgroup elements may not be nested.") }}

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("disabled") }}
: If this Boolean attribute is set, none of the items in this option group is selectable. Often browsers grey out such control and it won't receive any browsing events, like mouse clicks or focus-related ones.

{{ htmlattrdef("label") }}
: The name of the group of options, which the browser can use when labeling the options in the user interface. This attribute is mandatory if this element is used.

## Examples

```html
<select>
  <optgroup label="Group 1">
    <option>Option 1.1</option>
  </optgroup>
  <optgroup label="Group 2">
    <option>Option 2.1</option>
    <option>Option 2.2</option>
  </optgroup>
  <optgroup label="Group 3" disabled>
    <option>Option 3.1</option>
    <option>Option 3.2</option>
    <option>Option 3.3</option>
  </optgroup>
</select>

```

### Result

{{ EmbedLiveSample("Examples") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<optgroup>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-optgroup-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<optgroup>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-optgroup-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<optgroup>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.6) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.optgroup") }}

## See also

-   Other form-related elements: [`form`](/html/element/form/), [`legend`](/html/element/legend/), [`label`](/html/element/label/), [`button`](/html/element/button/), [`select`](/html/element/select/), [`datalist`](/html/element/datalist/), [`option`](/html/element/option/), [`fieldset`](/html/element/fieldset/), [`textarea`](/html/element/textarea/), [`keygen`](/html/element/keygen/), [`input`](/html/element/input/), [`output`](/html/element/output/), [`progress`](/html/element/progress/) and [`meter`](/html/element/meter/).