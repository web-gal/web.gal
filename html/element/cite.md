---
title: '<cite>: The Citation element'
tags:
  - Attribution
  - Citation
  - Citing References
  - Citing Works
  - Element
  - HTML
  - HTML text-level semantics
  - Quotations
  - Reference
  - Web
permalink: html/element/cite
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite'
browserCompact: html.elements.cite
---
{{ HTMLRef }}

The **HTML Citation element** (**`<cite>`**) is used to describe a reference to a cited creative work, and must include the title of that work. The reference may be in an abbreviated form according to context-appropriate conventions related to citation metadata.

{{ EmbedInteractiveExample("pages/tabbed/cite.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} Up to Gecko 1.9.2 (Firefox 4) inclusive, Firefox implements the {{ domxref("HTMLSpanElement") }} interface for this element. |

## Attributes

This element only includes the [global attributes](/html/global_attributes "HTML/Global attributes").

## Usage notes

In the context of the `<cite>` element, a creative work that might be cited could be, for example, one of the following:

-   A book
-   A research paper
-   An essay
-   A poem
-   A musical score
-   A song
-   A play or film script
-   A film
-   A television show
-   A game
-   A sculpture
-   A painting
-   A theatrical production
-   A play
-   An opera
-   A musical
-   An exhibition
-   A legal case report
-   A computer program
-   A web site
-   A web page
-   A blog post or comment
-   A forum post or comment
-   A tweet
-   A Facebook post
-   A written or oral statement
-   And so forth.

It's worth noting that the W3C specification says that a reference to a creative work, as included within a `<cite>` element, may include the name of the work’s author. However, the WHATWG specification for `<cite>` says the opposite: that a person’s name must _never_ be included, under any circumstances.

To include a reference to the source of quoted material which is contained within a [`blockquote`](/html/element/blockquote/) or [`q`](/html/element/q/) element, use the {{ htmlattrxref("cite", "blockquote") }} attribute on the element.

Typically, browsers style the contents of a `<cite>` element in italics by default. To avoid this, apply the CSS {{ cssxref("font-style") }} property to the `<cite>` element.

## Example

```html
<p>More information can be found in <cite>[ISO-0000]</cite>.</p>
```

The HTML above outputs:

{{ EmbedLiveSample("Example", 640, 60) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<cite>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-cite-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<cite>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-cite-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<cite>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you’d like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.cite") }}

## See also

-   The element [`blockquote`](/html/element/blockquote/) for long quotations.
-   The element [`q`](/html/element/q/) for inline quotations.