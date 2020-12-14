---
title: '<noembed>: The Embed Fallback element (Obsolete)'
tags:
  - Element
  - Embedded content
  - Embedding
  - HTML
  - Non-standard
  - Obsolete
  - Reference
  - noembed
permalink: html/element/noembed
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/noembed'
nonStandard: true
obsolete: true
browserCompact: html.elements.noembed
---
{{ HTMLRef }}

The `**<noembed>**` element is an obsolete, non-standard way to provide alternative, or "fallback", content for browsers that do not support the [`embed`](/html/element/embed/) element or do not support the type of [embedded content](/guide/html/content_categories#embedded_content) an author wishes to use. This element was deprecated in HTML 4.01 and above in favor of placing fallback content between the opening and closing tags of an [`object`](/html/element/object/) element.

While this element currently still works in many browsers, it is obsolete and should not be used. Use [`object`](/html/element/object/) instead, with fallback content between the opening and closing tags of the element.

## Examples

The message inside `<noembed>` tag will appear only when your browser does not support `<embed>` tag.

### Show an alternative content

```html
<embed type="vide/webm" src="/media/examples/flower.mp4" width="200" height="200">
  <noembed>
    <h1>Alternative content</h1>
  </noembed>
</embed>
```

## Browser compatibility

{{ Compat("html.elements.noembed") }}