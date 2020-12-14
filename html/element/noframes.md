---
title: '<noframes>: The Frame Fallback element'
tags:
  - Element
  - Frames
  - HTML
  - HTML frames
  - Obsolete
  - Reference
  - Web
  - noframes
permalink: html/element/noframes
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/noframes'
obsolete: true
browserCompact: html.elements.noframes
---
The obsolete HTML **No Frames** or **frame fallback** element, **`<noframes>`**, provides content to be presented in browsers that don't support (or have disabled support for) the [`frame`](/html/element/frame/) element. Although most commonly-used browsers support frames, there are exceptions, including certain special-use browsers including some mobile browsers, as well as text-mode browsers.

A `<noframes>` element can contain any HTML elements that are allowed within the body of an HTML document, with the exception of the [`frameset`](/html/element/frameset/) and [`frame`](/html/element/frame/) elements, since using frames when they aren't supported doesn't make sense.

`<noframes>` can be used to present a message explaining that the user's browser doesn't support frames, but ideally should be used to present an alternate form of the site that doesn't use frames but still offers the same or similar functionality.

In HTML 5 and later, `<noframes>` is obsolete and shouldn't be used, since the [`frame`](/html/element/frame/) and [`frameset`](/html/element/frameset/) elements are also obsolete. When frames are needed at all, they should be presented using the [`iframe`](/html/element/iframe/) element.

## Attributes

Like all other HTML elements, this element supports the [global attributes](/en-US/HTML/Global_attributes "HTML/Global attributes"). It has no other attributes available.

## Example

In this example, we see a frameset with two frames. In addition, `<noframes>` is used to present an explanatory message if the [user agent](/glossary/user_agent/) doesn't support frames.

```html
<frameset cols="50%,50%">
  <frame src="https://developer.mozilla.org/en/HTML/Element/frameset" />
  <frame src="https://developer.mozilla.org/en/HTML/Element/frame" />
  <noframes><p>It seems your browser does not support frames or is
  configured to not allow them.</p></noframes>
</frameset>
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5** The definition of 'noframes' in that specification](https://www.w3.org/TR/html52/#noframes) | {{ Spec2('HTML5 W3C') }} |   |
| [**HTML 4.01 Specification** The definition of '<noframes>' in that specification](https://www.w3.org/TR/html401/frames.html#edef-NOFRAMES) | {{ Spec2('HTML4.01') }} |   |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.noframes") }}

## See also

-   [`frameset`](/html/element/frameset/)
-   [`frame`](/html/element/frame/)

{{ HTMLRef }}