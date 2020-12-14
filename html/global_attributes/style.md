---
title: style
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/style
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style'
browserCompact: html.global_attributes.style
---
The `**style**` [global attribute](/html/global_attributes) contains [CSS](/css) styling declarations to be applied to the element. Note that it is recommended for styles to be defined in a separate file or files. This attribute and the [`style`](/html/element/style/) element have mainly the purpose of allowing for quick styling, for example for testing purposes.

{{ EmbedInteractiveExample("pages/tabbed/attribute-style.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

**Usage note:** This attribute must not be used to convey semantic information. Even if all styling is removed, a page should remain semantically correct. Typically it shouldn't be used to hide irrelevant information; this should be done using the [`hidden`](/html/global_attributes/hidden) attribute.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'style' in that specification](https://html.spec.whatwg.org/multipage/dom.html#the-style-attribute) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'style' in that specification](https://www.w3.org/TR/html51/dom.html#the-style-attribute) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'style' in that specification](https://www.w3.org/TR/html52/dom.html#the-style-attribute) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/). From [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/), it is now a true global attribute. |
| [**HTML 4.01 Specification** The definition of 'style' in that specification](https://www.w3.org/TR/html401/present/styles.html#h-14.2.2) | {{ Spec2('HTML4.01') }} | Supported on all elements but [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`head`](/html/element/head/), [`html`](/html/element/html/), [`meta`](/html/element/meta/), [`param`](/html/element/param/), [`script`](/html/element/script/), [`style`](/html/element/style/), and [`title`](/html/element/title/). |
| {{ SpecName("CSS3 Style", "", "") }} | {{ Spec2("CSS3 Style") }} | Defines the content of the `style` attribute. |

## Browser compatibility

{{ Compat("html.global_attributes.style") }}

## See also

-   {{ DOMxRef("ElementCSSInlineStyle.style") }}
-   All [global attributes](/html/global_attributes).