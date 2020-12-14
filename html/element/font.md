---
title: <font>
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
permalink: html/element/font
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/font'
obsolete: true
browserCompact: html.elements.font
---
## Summary

The _HTML Font Element_ (`<font>`) defines the font size, color and face for its content.

_Usage note:_ 

**Do not use this element!** Though once normalized in HTML 3.2, it was deprecated in HTML 4.01, at the same time as all elements related to styling only, then made obsolete in HTML5.

Starting with HTML 4, HTML does not convey styling information anymore (outside the [`style`](/html/element/style/) element or the **style** attribute of each element). For any new web development, styling should be written using [CSS](/en-US/docs/CSS "CSS") only.

The former behavior of the [`font`](/html/element/font/) element can be achieved, and even better controlled using the [CSS Fonts](/css/css_fonts) CSS properties.

## Attributes

Like all other HTML elements, this element supports the [global attributes](/en-US/docs/HTML/Global_attributes "HTML/Global attributes").

{{ htmlattrdef("color") }}
: This attribute sets the text color using either a named color or a color specified in the hexadecimal #RRGGBB format.

{{ htmlattrdef("face") }}
: This attribute contains a comma-separated list of one or more font names. The document text in the default style is rendered in the first font face that the client's browser supports. If no font listed is installed on the local system, the browser typically defaults to the proportional or fixed-width font for that system.

{{ htmlattrdef("size") }}
: This attribute specifies the font size as either a numeric or relative value. Numeric values range from `1` to `7` with `1` being the smallest and `3` the default. It can be defined using a relative value, like `+2` or `-3`, which set it relative to the value of the {{ htmlattrxref("size", "basefont") }} attribute of the [`basefont`](/html/element/basefont/) element, or relative to `3`, the default value, if none does exist.

## DOM interface

This element implements the {{ domxref("HTMLFontElement") }} interface.

## Browser compatibility

{{ Compat("html.elements.font") }}

{{ HTMLRef }}