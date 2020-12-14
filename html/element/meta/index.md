---
title: '<meta>: The Document-level Metadata element'
tags:
  - Document
  - Element
  - HTML
  - HTML charset
  - HTML document metadata
  - Reference
  - Web
  - charset
  - http-equiv
  - metadata
permalink: html/element/meta
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta'
browserCompact: html.elements.meta
---
{{ HTMLRef }}

The **HTML `<meta>` element** represents [metadata](/glossary/metadata/) that cannot be represented by other HTML meta-related elements, like [`base`](/html/element/base/), [`link`](/html/element/link/), [`script`](/html/element/script/), [`style`](/html/element/style/) or [`title`](/html/element/title/).

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | Metadata content. If the {{ htmlattrxref("itemprop") }} attribute is present: [flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content). |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | As it is a void element, the start tag must be present and the end tag must not be present. |
| Permitted parents | `<meta charset>`, `<meta http-equiv>`: a [`head`](/html/element/head/) element. If the {{ htmlattrxref("http-equiv", "meta") }} is not an encoding declaration, it can also be inside a [`noscript`](/html/element/noscript/) element, itself inside a [`head`](/html/element/head/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLMetaElement") }} |

The type of metadata provided by the `meta` element can be one of the following:

-   If the {{ htmlattrxref("name", "meta") }} attribute is set, the `meta` element provides _document-level metadata_, applying to the whole page.
-   If the {{ htmlattrxref("http-equiv", "meta") }} attribute is set, the `meta` element is a _pragma directive_, providing information equivalent to what can be given by a similarly-named HTTP header.
-   If the {{ htmlattrxref("charset", "meta") }} attribute is set, the `meta` element is a _charset declaration_, giving the character encoding in which the document is encoded.
-   If the {{ htmlattrxref("itemprop") }} attribute is set, the `meta` element provides _user-defined metadata_.

## Attributes

This element includes the [global attributes](/html/global_attributes).

**Note:** the attribute {{ htmlattrxref("name", "meta") }} has a specific meaning for the `<meta>` element, and the {{ htmlattrxref("itemprop") }} attribute must not be set on the same `<meta>` element that has any existing {{ htmlattrxref("name", "meta") }}, {{ htmlattrxref("http-equiv", "meta") }} or {{ htmlattrxref("charset", "meta") }} attributes.

{{ htmlattrdef("charset") }}
: This attribute declares the document's character encoding. If the attribute is present, its value must be an ASCII case-insensitive match for the string "`utf-8`", because UTF-8 is the only valid encoding for HTML5 documents. `meta` elements which declare a character encoding must be located entirely within the first 1024 bytes of the document.

{{ htmlattrdef("content") }}
: This attribute contains the value for the {{ htmlattrxref("http-equiv", "meta") }} or {{ htmlattrxref("name", "meta") }} attribute, depending on which is used.

{{ htmlattrdef("http-equiv") }}
: Defines a pragma directive. The attribute is named `**http-equiv**(alent)` because all the allowed values are names of particular HTTP headers:

-   `content-security-policy`
    
    Allows page authors to define a [content policy](/security/csp/csp_policy_directives) for the current page. Content policies mostly specify allowed server origins and script endpoints which help guard against cross-site scripting attacks.
    
-   `content-type`
    
    Declares the [MIME type](/http/basics_of_http/mime_types) and character encoding of the document. If specified, the `content` attribute must have the value "`text/html; charset=utf-8`". This is equivalent to a `meta` element with the {{ htmlattrxref("charset", "meta") }} attribute specified, and carries the same restriction on placement within the document. **Note:** Can only be used in documents served with a `text/html` — not in documents served with an XML MIME type.
    
-   `default-style`
    
    Sets the name of the default [CSS style sheet](/css) set.
    
-   `x-ua-compatible`
    
    If specified, the `content` attribute must have the value "`IE=edge`". User agents are required to ignore this pragma.
    
-   `refresh`
    
    This instruction specifies:
    
    -   The number of seconds until the page should be reloaded - only if the {{ htmlattrxref("content", "meta") }} attribute contains a positive integer.
    -   The number of seconds until the page should redirect to another - only if the {{ htmlattrxref("content", "meta") }} attribute contains a positive integer followed by the string '`;url=`', and a valid URL.
    
    ##### Accessibility concerns
    
    Pages set with a `refresh` value run the risk of having the time interval being too short. People navigating with the aid of assistive technology such as a screen reader may be unable to read through and understand the page's content before being automatically redirected. The abrupt, unannounced updating of the page content may also be disorienting for people experiencing low vision conditions.
    
    -   [MDN Understanding WCAG, Guideline 2.1 explanations](/accessibility/understanding_wcag/operable#guideline_2.2_—_enough_time_provide_users_enough_time_to_read_and_use_content)
    -   [MDN Understanding WCAG, Guideline 3.1 explanations](/accessibility/understanding_wcag/understandable#guideline_3.2_—_predictable_make_web_pages_appear_and_operate_in_predictable_ways)
    -   [Understanding Success Criterion 2.2.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-required-behaviors.html)
    -   [Understanding Success Criterion 2.2.4 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-postponed.html)
    -   [Understanding Success Criterion 3.2.5 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-no-extreme-changes-context.html)

{{ htmlattrdef("name") }}
: The `name` and `content` attributes can be used together to provide document metadata in terms of name-value pairs, with the `name` attribute giving the metadata name, and the `content` attribute giving the value.

See [standard metadata names](/html/element/meta/name) for details about the set of standard metadata names defined in the HTML specification.

## Examples

```html
<meta charset="utf-8">

<!-- Redirect page after 3 seconds -->
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org">

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<meta>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-meta-element) | {{ Spec2('HTML WHATWG') }} |  |

## Browser compatibility

{{ Compat("html.elements.meta") }}