---
title: <xmp>
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
permalink: html/element/xmp
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/xmp'
obsolete: true
browserCompact: html.elements.xmp
---
## Summary

The _HTML Example Element_ (`<xmp>`) renders text between the start and end tags without interpreting the HTML in between and using a monospaced font. The HTML2 specification recommended that it should be rendered wide enough to allow 80 characters per line.

**Note:** Do not use this element.

-   It has been deprecated since HTML3.2 and was not implemented in a consistent way. It was completely removed from the language in HTML5.
-   Use the [`pre`](/html/element/pre/) element or, if semantically adequate, the [`code`](/html/element/code/) element instead. Note that you will need to escape the '`<`' character as '`&lt;`' to make sure it is not interpreted as markup.
-   A monospaced font can also be obtained on any element, by applying an adequate [CSS](/en-US/docs/CSS "CSS") style using `monospace` as the generic-font value for the {{ cssxref("font-family") }} property.

## Attributes

This element has no other attributes than the [global attributes](/html/global_attributes "HTML/global attributes"), common to all elements.

## DOM interface

This element implements the {{ domxref('HTMLElement') }} interface.

**Implementation note:** up to Gecko 1.9.2 inclusive, Firefox implements the {{ domxref('HTMLSpanElement') }} interface for this element.

## Browser compatibility

{{ Compat("html.elements.xmp") }}

## See also

-   The [`pre`](/html/element/pre/) and [`code`](/html/element/code/) elements to be used instead.
-   The [`plaintext`](/html/element/plaintext/) and [`listing`](/html/element/listing/) elements, similar to [`xmp`](/html/element/xmp/) but also obsolete.

{{ HTMLRef }}