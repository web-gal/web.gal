---
title: '<dt>: The Description Term element'
tags:
  - Definition
  - Definition List
  - Definition Term
  - Element
  - HTML
  - HTML grouping content
  - Reference
  - Term
  - dt
  - lists
permalink: html/element/dt
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt'
browserCompact: html.elements.dt
---
{{ HTMLRef }}

The **HTML `<dt>` element** specifies a term in a description or definition list, and as such must be used inside a [`dl`](/html/element/dl/) element. It is usually followed by a [`dd`](/html/element/dd/) element; however, multiple `<dt>` elements in a row indicate several terms that are all defined by the immediate next [`dd`](/html/element/dd/) element.

The subsequent [`dd`](/html/element/dd/) (**Description Details**) element provides the definition or other related text associated with the term specified using `<dt>`.

{{ EmbedInteractiveExample("pages/tabbed/dt.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | [Flow content](/html/content_categories#flow_content), but with no [`header`](/html/element/header/), [`footer`](/html/element/footer/), sectioning content or heading content descendants. |
| Tag omission | Must have a start tag. The end tag may be omitted if this element is immediately followed by another `<dt>` or a [`dd`](/html/element/dd/) element, or if there is no more content in the parent element. |
| Permitted parents | Before a [`dt`](/html/element/dt/) or a [`dd`](/html/element/dd/) element, inside a [`dl`](/html/element/dl/) or (in [WHATWG](/en-US/docs/Glossary/WHATWG) HTML) a [`div`](/html/element/div/) that is inside a [`dl`](/html/element/dl/). |
| Implicit ARIA role | [`term`](https://w3c.github.io/aria/#term) |
| Permitted ARIA roles | `[listitem](/accessibility/aria/roles/listitem_role)` |
| DOM interface | {{ domxref("HTMLElement") }} Up to Gecko 1.9.2 (Firefox 4) inclusive, Firefox implements the [`HTMLSpanElement`](/api/htmlspanelement) interface for this element. |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Example

For an example, see the [example provided for the `<dl>` element](/html/element/dl#examples).

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<dt>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-dt-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<dt>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-dt-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<dt>' in that specification](https://www.w3.org/TR/html401/struct/lists.html#h-10.3) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.dt") }}

## See also

-   [`dd`](/html/element/dd/), [`dl`](/html/element/dl/)