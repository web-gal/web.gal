---
title: <noscript>
tags:
  - Element
  - HTML
  - HTML scripting
  - Reference
  - Web
permalink: html/element/noscript
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/noscript'
browserCompact: html.elements.noscript
---
{{ HTMLRef }}

The **HTML `<noscript>` element** defines a section of HTML to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Metadata content](/html/content_categories#metadata_content), [flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content). |
| Permitted content | When scripting is disabled and when it is a descendant of the [`head`](/html/element/head/) element: in any order, zero or more [`link`](/html/element/link/) elements, zero or more [`style`](/html/element/style/) elements, and zero or more [`meta`](/html/element/meta/) elements.  
When scripting is disabled and when it isn't a descendant of the [`head`](/html/element/head/) element: any [transparent content](/guide/html/content_categories#transparent_content_model), but no `<noscript>` element must be among its descendants.  
Otherwise: flow content or phrasing content. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content), if there are no ancestor `<noscript>` element, or in a [`head`](/html/element/head/) element (but only for an HTML document), here again if there are no ancestor `<noscript>` element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Examples

```html
<noscript>
  <!-- anchor linking to external file -->
  <a href="https://www.mozilla.com/">External Link</a>
</noscript>
<p>Rocks!</p>

```

### Result with scripting enabled

Rocks!

### Result with scripting disabled

[External Link](https://www.mozilla.com/)

Rocks!

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<noscript>' in that specification](https://html.spec.whatwg.org/multipage/scripting.html#the-noscript-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<noscript>' in that specification](https://www.w3.org/TR/html52/semantics-scripting.html#the-noscript-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<noscript>' in that specification](https://www.w3.org/TR/html401/interact/scripts.html#h-18.3.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.noscript") }}