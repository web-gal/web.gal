---
title: <data>
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
permalink: html/element/data
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/data'
browserCompact: html.elements.data
---
{{ HTMLRef }}

The **HTML `<data>` element** links a given piece of content with a machine-readable translation. If the content is time- or date-related, the [`time`](/html/element/time/) element must be used.

{{ EmbedInteractiveExample("pages/tabbed/data.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLDataElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("value") }}
: This attribute specifies the machine-readable translation of the content of the element.

## Examples

The following example displays product names but also associates each name with a product number.

```html
<p>New Products</p>
<ul>
 <li><data value="398">Mini Ketchup</data></li>
 <li><data value="399">Jumbo Ketchup</data></li>
 <li><data value="400">Mega Jumbo Ketchup</data></li>
</ul>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<data>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-data-element) | {{ Spec2('HTML WHATWG') }} | No change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of '<data>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-data-element) | {{ Spec2('HTML5 W3C') }} | Initial definition. |

## Browser compatibility

{{ Compat("html.elements.data") }}

## See also

-   The HTML [`time`](/html/element/time/) element.