---
title: 'Link types: prerender'
tags:
  - Attribute
  - HTML
  - Link
  - Link types
  - Reference
permalink: html/link_types/prerender
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/prerender'
browserCompact: html.elements.link.rel.prerender
---
The **`prerender`** keyword for the {{ HTMLAttrxRef("rel", "link") }} attribute of the [`link`](/html/element/link/) element is a hint to browsers that the user might need the target resource for the next navigation, and therefore the browser can likely improve the user experience by preemptively fetching and processing the resource — for example, by fetching its subresources or performing some rendering in the background offscreen.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'prerender' in that specification](https://html.spec.whatwg.org/multipage/#link-type-prerender) | {{ Spec2("HTML WHATWG") }} |  |

## Browser compatibility

{{ Compat("html.elements.link.rel.prerender") }}