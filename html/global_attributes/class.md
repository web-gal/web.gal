---
title: class
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/class
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class'
browserCompact: html.global_attributes.class
---
The `**class**` [global attribute](/html/global_attributes) is a space-separated list of the case-sensitive classes of the element. Classes allow CSS and Javascript to select and access specific elements via the [class selectors](/css/class_selectors) or functions like the DOM method {{ domxref("document.getElementsByClassName") }}.

{{ EmbedInteractiveExample("pages/tabbed/attribute-class.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

Though the specification doesn't put requirements on the name of classes, web developers are encouraged to use names that describe the semantic purpose of the element, rather than the presentation of the element. For example, _attribute_ to describe an attribute rather than _italics_, although an element of this class may be presented by _italics_. Semantic names remain logical even if the presentation of the page changes.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'class' in that specification](https://html.spec.whatwg.org/multipage/elements.html#classes) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'class' in that specification](https://www.w3.org/TR/html51/elements.html#classes) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'class' in that specification](https://www.w3.org/TR/html52/elements.html#classes) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/). From [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/), `class` is now a true global attribute. |
| [**HTML 4.01 Specification** The definition of 'class' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.5.2) | {{ Spec2('HTML4.01') }} | Supported on all elements but [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`head`](/html/element/head/), [`html`](/html/element/html/), [`meta`](/html/element/meta/), [`param`](/html/element/param/), [`script`](/html/element/script/), [`style`](/html/element/style/), and [`title`](/html/element/title/). |

## Browser compatibility

{{ Compat("html.global_attributes.class") }}

## See also

-   All [global attributes](/html/global_attributes).
-   {{ domxref('element.className') }}
-   {{ domxref('element.classList') }}
-   [Introduction to CSS](/en-US/docs/Learn/CSS/)