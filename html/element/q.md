---
title: '<q>: The Inline Quotation element'
tags:
  - Citation
  - Cite
  - Element
  - HTML
  - HTML text-level semantics
  - Q
  - Quotation
  - Quotation Marks
  - Reference
  - Web
  - quote
permalink: html/element/q
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q'
browserCompact: html.elements.q
---
{{ HTMLRef }}

The **HTML `<q>` element** indicates that the enclosed text is a short inline quotation. Most modern browsers implement this by surrounding the text in quotation marks. This element is intended for short quotations that don't require paragraph breaks; for long quotations use the [`blockquote`](/html/element/blockquote/) element.

{{ EmbedInteractiveExample("pages/tabbed/q.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), [phrasing content](/guide/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/guide/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/guide/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLQuoteElement") }} |

**Usage note:** Most modern browsers will automatically add quotation marks around text inside a `<q>` element. A style rule may be needed to add quotation marks in older browsers.

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("cite") }}
: The value of this attribute is a URL that designates a source document or message for the information quoted. This attribute is intended to point to information explaining the context or the reference for the quote.

## Example

```html
<p>According to Mozilla's website,
  <q
  cite="https://www.mozilla.org/en-US/about/history/details/">Firefox 1.0
  was released in 2004 and became a big success.</q></p>

```

{{ EmbedLiveSample('Example') }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<q>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-q-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<q>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-q-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<q>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.2) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.q") }}

## See also

-   The [`blockquote`](/html/element/blockquote/) element for long quotations.
-   The [`cite`](/html/element/cite/) element for source citations.