---
title: 'Link types: dns-prefetch'
tags:
  - Attribute
  - HTML
  - Link
  - Link types
  - Reference
permalink: html/link_types/dns-prefetch
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/dns-prefetch'
browserCompact: html.elements.link.rel.dns-prefetch
---
The **`dns-prefetch`** keyword for the {{ HTMLAttrxRef("rel", "link") }} attribute of the [`link`](/html/element/link/) element is a hint to browsers that the user is likely to need resources from the target resource's origin, and therefore the browser can likely improve the user experience by preemptively performing DNS resolution for that origin.

See [Using dns-prefetch](/performance/dns-prefetch) for more details.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'dns-prefetch' in that specification](https://html.spec.whatwg.org/multipage/#link-type-dns-prefetch) | {{ Spec2("HTML WHATWG") }} |  |

## Browser compatibility

{{ Compat("html.elements.link.rel.dns-prefetch") }}