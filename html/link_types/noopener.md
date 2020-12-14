---
title: 'Link types: noopener'
tags:
  - Attribute
  - HTML
  - Link types
  - Reference
permalink: html/link_types/noopener
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/noopener'
browserCompact: html.elements.link.a.noopener
---
The **`noopener`** keyword for the `[rel](/html/attributes/rel)` attribute of the [`a`](/html/element/a/), [`area`](/html/element/area/), and [`form`](/html/element/form/) elements instructs the browser to navigate to the target resource without granting the new browsing context access to the document that opened it — by not setting the {{ DOMxRef("Window.opener") }} property on the opened window (it returns `null`).

This is especially useful when opening untrusted links, in order to ensure they cannot tamper with the originating document via the {{ DOMxRef("Window.opener") }} property (see [About rel=noopener](https://mathiasbynens.github.io/rel-noopener/) for more details), while still providing the `Referer` HTTP header (unless `noreferrer` is used as well).

Note that when `noopener` is used, nonempty target names other than `_top`, `_self`, and `_parent` are all treated like `_blank` in terms of deciding whether to open a new window/tab.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'noopener' in that specification](https://html.spec.whatwg.org/multipage/#link-type-noopener) | {{ Spec2("HTML WHATWG") }} |  |

## Browser compatibility

{{ Compat("html.elements.link.a.noopener") }}