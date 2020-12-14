---
title: translate
tags:
  - Experimental
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/translate
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/translate'
browserCompact: html.global_attributes.translate
---
The **`translate`** [global attribute](/html/global_attributes) is an enumerated attribute that is used to specify whether an element's _translateable attribute_ values and its {{ domxref("Text") }} node children should be translated when the page is localized, or whether to leave them unchanged. It can have the following values:

-   empty string or "`yes`", which indicates that the element should be translated when the page is localized.
-   "`no`", which indicates that the element must not be translated.

Although not all browsers recognize this attribute, it is respected by automatic translation systems such as Google Translate, and may also be respected by tools used by human translators. As such it's important that web authors use this attribute to mark content that should not be translated.

## Examples

In this example, the `translate` attribute is used to ask translation tools not to translate the company's brand name in the footer.

```
<footer>
  <small>© 2020 <span translate="no">BrandName</span></small>
</footer>
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'translate' in that specification](https://html.spec.whatwg.org/multipage/dom.html#attr-translate) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'translate' in that specification](https://www.w3.org/TR/html51/dom.html#the-translate-attribute) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), initial definition |

## Browser compatibility

{{ Compat("html.global_attributes.translate") }}

## See also

-   All [global attributes](/html/global_attributes).
-   The {{ domxref("HTMLElement.translate") }} property that reflects this attribute.
-   [Using HTML's translate attribute](https://www.w3.org/International/questions/qa-translate-flag).
-   HTML {{ htmlattrxref("lang") }} attribute