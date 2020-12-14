---
title: '<base>: The Document Base URL element'
tags:
  - Element
  - HTML
  - HTML document metadata
  - 'HTML:Metadata content'
  - Reference
permalink: html/element/base
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base'
browserCompact: html.elements.base
---
{{ HTMLRef }}

The **HTML `<base>` element** specifies the base URL to use for all _relative_ URLs in a document. There can be only one `<base>` element in a document.

A document's used base URL can be accessed by scripts with {{ domxref('document.baseURI') }}. If the document has no `<base>` elements, then `baseURI` defaults to {{ domxref("location.href") }}.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | Metadata content. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | There must be no closing tag. |
| Permitted parents | A [`head`](/html/element/head/) that doesn't contain another [`base`](/html/element/base/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLBaseElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

If either of the following attributes are specified, this element **must** come before other elements with attribute values of URLs, such as [`link`](/html/element/link/)’s `href` attribute.

{{ htmlattrdef("href") }}
: The base URL to be used throughout the document for relative URLs. Absolute and relative URLs are allowed.

{{ htmlattrdef("target") }}
: A **keyword** or **author-defined name** of the default [browsing context](/glossary/browsing_context/) to show the results of navigation from [`a`](/html/element/a/), [`area`](/html/element/area/), or [`form`](/html/element/form/) elements without explicit `target` attributes.

: The following keywords have special meanings:

-   `_self` (default): Show the result in the current browsing context.
-   `_blank`: Show the result in a new, unnamed browsing context.
-   `_parent`: Show the result in the parent browsing context of the current one, if the current page is inside a frame. If there is no parent, acts the same as `_self`.
-   `_top`: Show the result in the topmost browsing context (the browsing context that is an ancestor of the current one and has no parent). If there is no parent, acts the same as `_self`.

## Usage notes

### Multiple <base> elements

If multiple `<base>` elements are used, only the first `href` and first `target` are obeyed — all others are ignored.

### In-page anchors

Links pointing to a fragment in the document — e.g. `<a href="#some-id">` — are resolved with the `<base>`, triggering an HTTP request to the base URL with the fragment attached. For example:

1.  Given `<base href="https://example.com">`
2.  ...and this link: `<a href="#anchor">Anker</a>`
3.  ...the link points to `https://example.com/#anchor`.

### Open Graph

[Open Graph](https://ogp.me/) tags do not acknowledge `<base>`, and should always have full absolute URLs. For example:

```html
<meta property="og:image" content="https://example.com/thumbnail.jpg">
```

## Examples

```html
<base href="https://www.example.com/">
<base target="_blank">
<base target="_top" href="https://example.com/">

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<base>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-base-element) | {{ Spec2('HTML WHATWG') }} | No change since last snapshot. |
| [**HTML 5** The definition of '<base>' in that specification](https://www.w3.org/TR/html52/document-metadata#the-base-element) | {{ Spec2('HTML5 W3C') }} | Specified the behavior of `target` |
| [**HTML 4.01 Specification** The definition of '<base>' in that specification](https://www.w3.org/TR/html401/struct/links.html#h-12.4) | {{ Spec2('HTML4.01') }} | Added the `target` attribute |

## Browser compatibility

{{ Compat("html.elements.base") }}