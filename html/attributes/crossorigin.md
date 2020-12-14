---
title: 'HTML attribute: crossorigin'
tags:
  - Advanced
  - Attribute
  - CORS
  - HTML
  - NeedsContent
  - Reference
  - Security
permalink: html/attributes/crossorigin
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/crossorigin'
draft: true
browserCompact: html.elements.link.crossorigin
---
The crossorigin attribute, valid on the [`audio`](/html/element/audio/), [`img`](/html/element/img/), [`link`](/html/element/link/), [`script`](/html/element/script/), and [`video`](/html/element/video/) elements, provides support for [CORS](/http/cors), defining how the element handles crossorigin requests, thereby enabling the configuration of the CORS requests for the element's fetched data. Depending on the element, the attribute can be a CORS settings attribute.

The `crossorigin` content attribute on media elements is a CORS settings attribute.

These attributes are enumerated, and have the following possible values:

<table class="standard-table"><tbody><tr><td class="header">Keyword</td><td class="header">Description</td></tr><tr><td><code>anonymous</code></td><td>CORS requests for this element will have the credentials flag set to 'same-origin'.</td></tr><tr><td><code>use-credentials</code></td><td>CORS requests for this element will have the credentials flag set to 'include'.</td></tr><tr><td><code>""</code></td><td>Setting the attribute name to an empty value, like <code>crossorigin</code> or <code>crossorigin=""</code>, is the same as <code>anonymous</code>.</td></tr></tbody></table>

By default (that is, when the attribute is not specified), CORS is not used at all. The "anonymous" keyword means that there will be no exchange of **user credentials** via cookies, client-side SSL certificates or HTTP authentication as described in the [Terminology section of the CORS specification](http://www.w3.org/TR/cors/#user-credentials), unless it is in the same origin.

An invalid keyword and an empty string will be handled as the `anonymous` keyword.

Prior to Firefox 83 the `crossorigin` attribute was not supported for `rel="icon"` there is also [an open issue for Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=1121645).

### Example: crossorigin with the script element

You can use the following [`script`](/html/element/script/) element to tell a browser to execute the `https://example.com/example-framework.js` script without sending user-credentials.

```html
<script src="https://example.com/example-framework.js" crossorigin="anonymous"></script>
```

### Example: Webmanifest with credentials

The `use-credentials` value must be used when fetching a [manifest](/manifest) that requires credentials, even if the file is from the same origin.

```html
<link rel="manifest" href="/app.webmanifest" crossorigin="use-credentials">
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'CORS settings attributes' in that specification](https://html.spec.whatwg.org/multipage/infrastructure.html#cors-settings-attributes) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML Living Standard** The definition of 'crossorigin' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#attr-img-crossorigin) | {{ Spec2('HTML WHATWG') }} |  |

## Browser compatibility

### <script crossorigin>

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.script.crossorigin") }}

### <video crossorigin>

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.video.crossorigin") }}

### <link crossorigin>

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.link.crossorigin") }}

## See also

-   [Cross-Origin Resource Sharing (CORS)](/http/cors)
-   [HTML attribute: `rel`](/html/attributes/rel)

{{ QuickLinksWithSubpages("/en-US/docs/Web/HTML/") }}