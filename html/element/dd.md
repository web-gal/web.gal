---
title: '<dd>: The Description Details element'
tags:
  - Definition
  - Description Details
  - Element
  - HTML
  - HTML grouping content
  - Reference
  - Web
  - dd
  - description list
  - details
permalink: html/element/dd
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd'
browserCompact: html.elements.dd
---
{{ HTMLRef }}

The **HTML `<dd>` element** provides the description, definition, or value for the preceding term ([`dt`](/html/element/dt/)) in a description list ([`dl`](/html/element/dl/)).

{{ EmbedInteractiveExample("pages/tabbed/dd.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | None. |
| Permitted content | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Tag omission | The start tag is required. The end tag may be omitted if the [`dd`](/html/element/dd/) element is immediately followed by another `<dd>` element or a [`dt`](/html/element/dt/) element, or if there is no more content in the parent element. |
| Permitted parents | [`dl`](/html/element/dl/) or (in [WHATWG](/en-US/docs/Glossary/WHATWG) HTML) a [`div`](/html/element/div/) that is inside a [`dl`](/html/element/dl/). |
| Previous sibling | [`dt`](/html/element/dt/) or another [`dd`](/html/element/dd/) element. |
| Implicit ARIA role | [`definition`](https://w3c.github.io/aria/#definition) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element's attributes include the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("nowrap") }} {{ Non-standard_inline }}
: If the value of this attribute is set to `yes`, the definition text will not wrap. The default value is `no`.

## Example

For an example, see [<dl> examples](/en-US/docs/HTML/Element/dl#examples).

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<dd>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-dd-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<dd>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-dd-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<dd>' in that specification](https://www.w3.org/TR/html401/struct/lists.html#h-10.3) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.dd") }}

## See also

-   [`dl`](/html/element/dl/)
-   [`dt`](/html/element/dt/)