---
title: '<head>: The Document Metadata (Header) element'
tags:
  - Element
  - HTML
  - HTML document metadata
  - 'HTML:Metadata content'
  - Reference
  - Web
permalink: html/element/head
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head'
browserCompact: html.elements.head
---
{{ HTMLRef }}

The **HTML `<head>` element** contains machine-readable information ([metadata](/glossary/metadata/)) about the document, like its [title](/html/element/title), [scripts](/html/element/script), and [style sheets](/html/element/style).

**Note:** `<head>` primarily holds information for machine processing, not human-readability. For human-visible information, like top-level headings and listed authors, see the [`header`](/html/element/header/) element.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | 
If the document is an [`iframe`](/html/element/iframe/) {{ htmlattrxref("srcdoc", "iframe") }} document, or if title information is available from a higher level protocol (like the subject line in HTML email), zero or more elements of metadata content.

Otherwise, one or more elements of metadata content where exactly one is a [`title`](/html/element/title/) element.

 |
| Tag omission | The start tag may be omitted if the first thing inside the `<head>` element is an element.  
The end tag may be omitted if the first thing following the `<head>` element is not a space character or a comment. |
| Permitted parents | An [`html`](/html/element/html/) element, as its first child. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLHeadElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("profile") }} {{ obsolete_inline }}
: The [URI](/glossary/uri/)s of one or more metadata profiles, separated by [white space](/glossary/whitespace/).

## Example

```html
<!doctype html>
<html>
  <head>
    <title>Document title</title>
  </head>
</html>

```

## Notes

HTML5-compliant browsers automatically create a `<head>` element if its tags are omitted in the markup. [This auto-creation is not guaranteed in ancient browsers](https://www.stevesouders.com/blog/2010/05/12/autohead-my-first-browserscope-user-test/).

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<head>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-head-element) | {{ Spec2('HTML WHATWG') }} | No change from latest shapshot |
| [**HTML 5** The definition of '<head>' in that specification](https://www.w3.org/TR/html52/document-metadata.html#the-head-element) | {{ Spec2('HTML5 W3C') }} | Obsoleted `profile` |
| [**HTML 4.01 Specification** The definition of '<head>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.4.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.head") }}

## See also

-   Elements that can be used inside the `<head>`:
    -   [`title`](/html/element/title/)
    -   [`base`](/html/element/base/)
    -   [`link`](/html/element/link/)
    -   [`style`](/html/element/style/)
    -   [`meta`](/html/element/meta/)
    -   [`script`](/html/element/script/)
    -   [`noscript`](/html/element/noscript/)
    -   [`template`](/html/element/template/)