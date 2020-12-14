---
title: theme-color
tags:
  - Attribute
  - HTML
  - HTML document metadata
  - Reference
  - metadata
permalink: html/element/meta/name/theme-color
mdn: >-
  https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name/theme-color
browserCompact: html.elements.meta.name.theme-color
---
{{ HTMLRef }}

The **`theme-color`** value for the {{ htmlattrxref("name", "meta") }} attribute of the [`meta`](/html/element/meta/) element indicates a suggested color that user agents should use to customize the display of the page or of the surrounding user interface. If specified, the {{ htmlattrxref("content", "meta") }} attribute must contain a valid CSS {{ cssxref("<color>") }}.

## Example

```html
<meta name="theme-color" content="#4285f4">
```

The following image shows the effect that the [`meta`](/html/element/meta/) element above will have on a document displayed in Chrome running on an Android mobile device.

![Image showing the effect of using theme-color](https://mdn.mozillademos.org/files/17199/theme-color.png)

Image credit: from [Icons & Browser Colors](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization), created and [shared by Google](https://developers.google.com/readme/policies) and used according to terms described in the [Creative Commons 4.0 Attribution License](https://creativecommons.org/licenses/by/4.0/).

## Specifications

| Specification |
| --- |
| [**HTML Living Standard** The definition of 'theme-color' in that specification](https://html.spec.whatwg.org/multipage/#meta-theme-color) |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.meta.name.theme-color") }}