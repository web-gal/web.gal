---
title: id
tags:
  - Global attributes
  - HTML
  - Reference
  - Web
  - id
permalink: html/global_attributes/id
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id'
browserCompact: html.global_attributes.id
---
The **`id` [global attribute](/glossary/global_attribute/)** defines an identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking (using a [fragment identifier](/http/basics_of_http/identifying_resources_on_the_web#fragment)), scripting, or styling (with [CSS](/glossary/css/)).

{{ EmbedInteractiveExample("pages/tabbed/attribute-id.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

This attribute's value is an opaque string: this means that web authors should not rely on it to convey human-readable information (although having your IDs somewhat human-readable can be useful for code comprehension, e.g. consider `ticket-18659` versus `r45tgfe-freds&$@`).

`id`'s value must not contain [whitespace](/glossary/whitespace/) (spaces, tabs etc.). Browsers treat non-conforming IDs that contain whitespace as if the whitespace is part of the ID. In contrast to the {{ htmlattrxref("class") }} attribute, which allows space-separated values, elements can only have one single ID value.

**Note:** Using characters except [ASCII](/glossary/ascii/) letters, digits, `'_'`, `'-'` and `'.'` may cause compatibility problems, as they weren't allowed in HTML 4. Though this restriction has been lifted in [HTML5](/glossary/html5/), an ID should start with a letter for compatibility.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'id' in that specification](https://html.spec.whatwg.org/multipage/dom.html#the-id-attribute) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'id' in that specification](https://www.w3.org/TR/html51/dom.html#the-id-attribute) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'id' in that specification](https://www.w3.org/TR/html52/dom.html#the-id-attribute) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), now accept `'_'`, `'-'` and `'.'` if not at the beginning of the id. It is also a true global attribute. |
| [**HTML 4.01 Specification** The definition of 'id' in that specification](https://www.w3.org/TR/html401/struct/global.html#adef-id) | {{ Spec2('HTML4.01') }} | Supported on all elements but [`base`](/html/element/base/), [`head`](/html/element/head/), [`html`](/html/element/html/), [`meta`](/html/element/meta/), [`script`](/html/element/script/), [`style`](/html/element/style/), and [`title`](/html/element/title/). |

## Browser compatibility

{{ Compat("html.global_attributes.id") }}

## See also

-   All [global attributes](/html/global_attributes).
-   {{ domxref("Element.id") }} that reflects this attribute.