---
title: '<blockquote>: The Block Quotation element'
tags:
  - Blockquote
  - Element
  - HTML
  - HTML grouping content
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Sectioning root'
  - Quotations
  - Reference
  - Web
permalink: html/element/blockquote
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote'
browserCompact: html.elements.blockquote
---
{{ HTMLRef }}

The **HTML `<blockquote>` Element** (or _HTML Block Quotation Element_) indicates that the enclosed text is an extended quotation. Usually, this is rendered visually by indentation (see [Notes](#Usage_notes) for how to change it). A URL for the source of the quotation may be given using the **cite** attribute, while a text representation of the source can be given using the [`cite`](/html/element/cite/) element.

{{ EmbedInteractiveExample("pages/tabbed/blockquote.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), sectioning root, palpable content. |
| Permitted content | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLQuoteElement") }} |

## Attributes

This element's attributes include the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("cite") }}
: A URL that designates a source document or message for the information quoted. This attribute is intended to point to information explaining the context or the reference for the quote.

## Usage notes

To change the indentation applied to the quoted text, use the [CSS](/glossary/css/) {{ cssxref("margin-left") }} and/or {{ cssxref("margin-right") }} properties, or the {{ cssxref("margin") }} shorthand property.

To include shorter quotes inline rather than in a separate block, use the [`q`](/html/element/q/) (Quotation) element.

## Example

This example demonstrates the use of the `<blockquote>` element to quote a passage from [RFC 1149](https://tools.ietf.org/html/rfc1149), A Standard for the Transmission of IP Datagrams on Avian Carriers.

```html
<blockquote cite="https://tools.ietf.org/html/rfc1149">
  <p>Avian carriers can provide high delay, low
  throughput, and low altitude service. The
  connection topology is limited to a single
  point-to-point path for each carrier, used with
  standard carriers, but many carriers can be used
  without significant interference with each other,
  outside of early spring. This is because of the 3D
  ether space available to the carriers, in contrast
  to the 1D ether used by IEEE802.3. The carriers
  have an intrinsic collision avoidance system, which
  increases availability.</p>
</blockquote>

```

The output from this HTML snippet looks like this:

{{ EmbedLiveSample("Example", 640, 180) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<blockquote>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-blockquote-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<blockquote>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-blockquote-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<blockquote>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.2) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.blockquote") }}

## See also

-   The [`q`](/html/element/q/) element for inline quotations.
-   The [`cite`](/html/element/cite/) element for source citations.