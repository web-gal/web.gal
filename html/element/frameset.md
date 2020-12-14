---
title: <frameset>
tags:
  - Deprecated
  - Element
  - HTML
  - Reference
  - Web
permalink: html/element/frameset
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frameset'
deprecated: true
browserCompact: html.elements.frameset
---
{{ HTMLRef }}

The **HTML `<frameset>` element** is used to contain [`frame`](/html/element/frame/) elements.

**Note:** Because the use of frames is now discouraged in favor of using [`iframe`](/html/element/iframe/), this element is not typically used by modern web sites.

## Attributes

Like all other HTML elements, this element supports the [global attributes](/html/global_attributes).

{{ htmlattrdef("cols") }}
: This attribute specifies the number and size of horizontal spaces in a frameset.

{{ htmlattrdef("rows") }}
: This attribute specifies the number and size of vertical spaces in a frameset.

## Example

```html
<frameset cols="50%,50%">
  <frame src="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frameset" />
  <frame src="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frame" />
</frameset>
```

## Browser compatibility

{{ Compat("html.elements.frameset") }}

## See also

-   [`frame`](/html/element/frame/)
-   [`iframe`](/html/element/iframe/)