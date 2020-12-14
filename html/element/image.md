---
title: '<image>: The obsolete Image element'
tags:
  - Element
  - HTML
  - HTML Element Reference
  - HTML Reference
  - HTML element
  - Non-standard
  - Obsolete
  - Reference
permalink: html/element/image
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/image'
obsolete: true
nonStandard: true
browserCompact: html.elements.image
---
The obsolete **HTML Image element (`<image>`)** is an obsolete remnant of an ancient version of HTML lost in the mists of time; use the standard [`img`](/html/element/img/) element instead. Seriously, the specification even literally uses the words "Don't ask" when describing this element.

**Do not use this!** In order to display images, use the standard [`img`](/html/element/img/) element.

While some browsers will attempt to automatically convert this into an [`img`](/html/element/img/) element, they won't always do so, and won't always succeed when they try, due to various ways in which the options can be interpreted. So just don't use it if you like your users.

## Specifications

This might have once been part of a specification, but nobody seems to remember. It certainly isn't anymore. Just avoid it like the plague.

## Browser compatibility

In general, browsers will attempt to map this to `<img>`, but only if the {{ htmlattrxref("src", "img") }} attribute is specified as well.  Creating an `<image>` element without a `src` attribute results in an {{ domxref("HTMLElement") }} object with the local element name `"image"`. However, if the element is created with a `src` attribute, the result is instead an {{ domxref("HTMLImageElement") }} and its local element name is changed to `"img"`.

However, that doesn't mean this is a good idea to use. It's not.

{{ Compat("html.elements.image") }}

## See also

-   [`img`](/html/element/img/): The correct way to display an image in a document
-   [`picture`](/html/element/picture/): A more powerful correct way to display an image in a document

{{ HTMLRef }}