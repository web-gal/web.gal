---
title: '<param>: The Object Parameter element'
tags:
  - Element
  - HTML
  - HTML embedded content
  - Reference
  - Web
permalink: html/element/param
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/param'
browserCompact: html.elements.param
---
{{ HTMLRef }}

The **HTML `<param>` element** defines parameters for an [`object`](/html/element/object/) element.

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | None. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | As it is a void element, the start tag must be present and the end tag must not be present. |
| Permitted parents | An [`object`](/html/element/object/) before any [flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLParamElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("name") }}
: Name of the parameter.

{{ htmlattrdef("value") }}
: Specifies the value of the parameter.

### Deprecated attributes

{{ htmlattrdef("type") }} {{ deprecated_inline }}
: Only used if the `valuetype` is set to `ref`. Specifies the MIME type of values found at the URI specified by value.

{{ htmlattrdef("valuetype") }} {{ deprecated_inline }}
: Specifies the type of the `value` attribute. Possible values are:

-   `data`: Default value. The value is passed to the object's implementation as a string.
-   `ref`: The value is a URI to a resource where run-time values are stored.
-   `object`: An ID of another [`object`](/html/element/object/) in the same document.

## Examples

Please see the [`object`](/html/element/object/) page for examples on `<param>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<param>' in that specification](https://html.spec.whatwg.org/multipage/iframe-embed-object.html#the-param-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<param>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-param-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<param>' in that specification](https://www.w3.org/TR/html401/struct/objects.html#h-13.3.2) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.param") }}

## See also

-   [`object`](/html/element/object/)