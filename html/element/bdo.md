---
title: '<bdo>: The Bidirectional Text Override element'
tags:
  - BiDi
  - Bidirectional Text
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Left to Right
  - Reference
  - Right to Left
  - Text
  - Text Direction
  - Text Rendering
  - Web
  - ltr
  - rtl
permalink: html/element/bdo
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bdo'
browserCompact: html.elements.bdo
---
{{ HTMLRef }}

The **HTML Bidirectional Text Override element** (**`<bdo>`**) overrides the current directionality of text, so that the text within is rendered in a different direction.

{{ EmbedInteractiveExample("pages/tabbed/bdo.html", "tabbed-standard") }}

The text's characters are drawn from the starting point in the given direction; the individual characters' orientation is not affected (so characters don't get drawn backward, for example).

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), [phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} Up to Gecko 1.9.2 (Firefox 4) inclusive, Firefox implements the `[HTMLSpanElement](/api/htmlspanelement)` interface for this element. |

## Attributes

This element's attributes include the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("dir") }}
: The direction in which text should be rendered in this element's contents. Possible values are:

-   `ltr`: Indicates that the text should go in a left-to-right direction.
-   `rtl`: Indicates that the text should go in a right-to-left direction.

## Examples

```html
<!-- Switch text direction -->
<p>This text will go left to right.</p>
<p><bdo dir="rtl">This text will go right
to left.</bdo></p>

```

### Result

{{ EmbedLiveSample('Examples') }}

## Notes

The HTML 4 specification did not specify events for this element; they were added in XHTML. This is most likely an oversight.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<bdo>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-bdo-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<bdo>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-bdo-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<bdo>' in that specification](https://www.w3.org/TR/html401/dirlang.html#h-8.2.4) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.bdo") }}

## See also

-   Related HTML element: [`bdi`](/html/element/bdi/)