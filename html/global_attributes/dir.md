---
title: dir
tags:
  - BiDi
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/dir
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir'
browserCompact: html.global_attributes.dir
---
The `**dir**` [global attribute](/html/global_attributes) is an enumerated attribute that indicates the directionality of the element's text.

{{ EmbedInteractiveExample("pages/tabbed/attribute-dir.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

It can have the following values:

-   `ltr`, which means _left to right_ and is to be used for languages that are written from the left to the right (like English);
-   `rtl`, which means _right to left_ and is to be used for languages that are written from the right to the left (like Arabic);
-   `auto`, which lets the user agent decide. It uses a basic algorithm as it parses the characters inside the element until it finds a character with a strong directionality, then applies that directionality to the whole element.

**Usage notes:** This attribute is mandatory for the [`bdo`](/html/element/bdo/) element where it has a different semantic meaning.

-   This attribute is _not_ inherited by the [`bdi`](/html/element/bdi/) element. If not set, its value is `auto`.
    
-   This attribute can be overridden by the CSS properties {{ cssxref("direction")  }} and {{ cssxref("unicode-bidi")  }}, if a CSS page is active and the element supports these properties.
    
-   As the directionality of the text is semantically related to its content and not to its presentation, it is recommended that web developers use this attribute instead of the related CSS properties when possible. That way, the text will display correctly even on a browser that doesn't support CSS or has the CSS deactivated.
    
-   The `auto` value should be used for data with an unknown directionality, like data coming from user input, eventually stored in a database.
    

Browsers might allow users to change the directionality of [`input`](/html/element/input/) and [`textarea`](/html/element/textarea/)s in order to assist with authoring content. Chrome and Safari provide a directionality option in the contextual menu of input fields while Internet Explorer and Edge use the key combinations Ctrl + Left Shift and Ctrl + Right Shift. Firefox uses Ctrl/Cmd + Shift + X but does NOT update the `**dir**` attribute value.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'dir' in that specification](https://html.spec.whatwg.org/multipage/dom.html#the-dir-attribute) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'dir' in that specification](https://www.w3.org/TR/html51/dom.html#the-dir-attribute) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'dir' in that specification](https://www.w3.org/TR/html52/dom.html#the-dir-attribute) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), from [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/) it added the `auto` value, and is now a true global attribute. |
| [**HTML 4.01 Specification** The definition of 'dir' in that specification](https://www.w3.org/TR/html401/dirlang.html#h-8.2) | {{ Spec2('HTML4.01') }} | Supported on all elements but [`applet`](/html/element/applet/), [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`bdo`](/html/element/bdo/), [`br`](/html/element/br/), [`frame`](/html/element/frame/), [`frameset`](/html/element/frameset/), [`iframe`](/html/element/iframe/), [`param`](/html/element/param/), and [`script`](/html/element/script/). |

## Browser compatibility

{{ Compat("html.global_attributes.dir") }}

## See also

-   All [global attributes](/html/global_attributes).
-   {{ domxref("HTMLElement.dir") }} that reflects this attribute.