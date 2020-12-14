---
title: <listing>
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
permalink: html/element/listing
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/listing'
obsolete: true
browserCompact: html.elements.listing
---
## Summary

The _HTML Listing Element_ (`<listing>`) renders text between the start and end tags without interpreting the HTML in between and using a monospaced font. The HTML 2 standard recommended that lines shouldn't be broken when not greater than 132 characters.

**Note:** Do not use this element.

-   It is deprecated since HTML 3.2 and was neither implemented by all browsers, nor in a consistent way. Even more it is obsoleted in HTML5 and may be rendered by conforming user-agents as the [`pre`](/html/element/pre/) element, which will interpret the internal HTML!
-   Instead use the [`pre`](/html/element/pre/) element or if semantically adequate the [`code`](/html/element/code/) element, eventually escaping the HTML '`<`' and '`>`' so that they don't get interpreted.
-   A monospaced font can also be obtained on a simple [`div`](/html/element/div/) element, by applying an adequate [CSS](/css "CSS") style using `monospace` as the generic-font value in a {{ cssxref("font-family") }} property.

## Attributes

This element has no other attributes than the [global attributes](/html/global_attributes "HTML/global attributes"), common to all elements.

## DOM interface

This element implements the {{ domxref('HTMLElement') }} interface.

**Implementation note:** up to Gecko 1.9.2 inclusive, Firefox implements the {{ domxref('HTMLSpanElement') }} interface for this element.

## Browser compatibility

{{ Compat("html.elements.listing") }}

## See also

-   The [`pre`](/html/element/pre/) and [`code`](/html/element/code/) elements to be used instead.
-   The [`plaintext`](/html/element/plaintext/) and [`xmp`](/html/element/xmp/) elements, similar to [`listing`](/html/element/listing/) but also obsolete.

{{ HTMLRef }}