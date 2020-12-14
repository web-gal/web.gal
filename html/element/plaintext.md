---
title: '<plaintext>: The Plain Text element (Deprecated)'
tags:
  - Element
  - HTML
  - Obsolete
  - Plain text
  - Reference
  - Web
  - plaintext
permalink: html/element/plaintext
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/plaintext'
obsolete: true
browserCompact: html.elements.plaintext
---
The _HTML Plaintext Element_ (`<plaintext>`) renders everything following the start tag as raw text, ignoring any following HTML. There is no closing tag, since everything after it is considered raw text.

**Note:** Do not use this element.

-   `<plaintext>` is deprecated since HTML 2, and not all browsers implemented it. Browsers that did implement it didn't do so consistently.
-   `<plaintext>` is obsolete in HTML5; browsers that accept it may instead treat it as a [`pre`](/html/element/pre/) element that still interprets HTML within.
-   If `<plaintext>` is the first element on the page (other than any non-displayed elements, like [`head`](/html/element/head/)), do not use HTML at all. Instead serve a text file with the `text/plain` [MIME-type](/en-US/docs/Properly_Configuring_Server_MIME_Types "Properly Configuring Server MIME Types").
-   Instead of `<plaintext>`, use the [`pre`](/html/element/pre/) element or, if semantically accurate (such as for inline text), the [`code`](/html/element/code/) element. Escape any `<`, `>` and `&` characters, to prevent browsers inadvertently parsing content the element content as HTML.
-   A monospaced font can be applied to any HTML element via a [CSS](/css) {{ cssxref("font-family") }} style with the `monospace` generic value.

## Attributes

This element has no other attributes than the [global attributes](/html/global_attributes "HTML/global attributes") common to all elements.

## DOM interface

This element implements the {{ domxref('HTMLElement') }} interface.

**Implementation note:** In Gecko 1.9.2 and before, Firefox implements the interface {{ domxref('HTMLSpanElement') }} for this element.

## Browser compatibility

{{ Compat("html.elements.plaintext") }}

## See also

-   The [`pre`](/html/element/pre/) and [`code`](/html/element/code/) elements, which should be used instead.
-   The [`listing`](/html/element/listing/) and [`xmp`](/html/element/xmp/) elements, which are both obsolete elements similar to [`plaintext`](/html/element/plaintext/).

{{ HTMLRef }}