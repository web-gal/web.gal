---
title: '<nobr>: The Non-Breaking Text element (obsolete)'
tags:
  - Element
  - HTML
  - Non-standard
  - Obsolete
  - Reference
  - Web
  - nobr
permalink: html/element/nobr
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nobr'
nonStandard: true
obsolete: true
browserCompact: html.elements.nobr
---
{{ HTMLRef }}

The non-standard, obsolete HTML `<nobr>` element prevents the text it contains from automatically wrapping across multiple lines, potentially resulting in the user having to scroll horizontally to see the entire width of the text.

This element was _never_ standard HTML and was not widely implemented, so you shouldn't use it. Instead, use the CSS property {{ CSSxRef("white-space") }} like this:

```html
<span style="white-space: nowrap;">Long line with no breaks</span>
```

## Browser compatibility

{{ Compat("html.elements.nobr") }}

## See also

-   {{ CSSxRef("white-space") }}
-   {{ CSSxRef("overflow") }}