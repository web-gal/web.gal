---
title: 'Link types: noreferrer'
tags:
  - Attribute
  - HTML
  - Link types
  - Reference
permalink: html/link_types/noreferrer
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/noreferrer'
browserCompact: html.elements.link.a.noreferrer
---
The **`noreferrer`** keyword for the `[rel](/html/attributes/rel)` attribute of the [`a`](/html/element/a/), [`area`](/html/element/area/), and [`form`](/html/element/form/) elements instructs the browser, when navigating to the target resource, to omit the {{ HTTPHeader("Referer") }} header and otherwise leak no referrer information — and additionally to behave as if the `[noopener](/html/link_types/noopener)` keyword were also specified.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'noreferrer' in that specification](https://html.spec.whatwg.org/multipage/#link-type-noreferrer) | {{ Spec2("HTML WHATWG") }} |  |

## Browser compatibility

{{ Compat("html.elements.link.a.noreferrer") }}