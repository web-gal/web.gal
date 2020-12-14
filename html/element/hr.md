---
title: '<hr>: The Thematic Break (Horizontal Rule) element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - Reference
permalink: html/element/hr
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr'
browserCompact: html.elements.hr
---
{{ HTMLRef }}

The **HTML `<hr>` element** represents a thematic break between paragraph-level elements: for example, a change of scene in a story, or a shift of topic within a section.

{{ EmbedInteractiveExample("pages/tabbed/hr.html", "tabbed-shorter") }}

Historically, this has been presented as a horizontal rule or line. While it may still be displayed as a horizontal rule in visual browsers, this element is now defined in semantic terms, rather than presentational terms, so if you wish to draw a horizontal line, you should do so using appropriate CSS.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content). |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | It must have start tag, but must not have an end tag. |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [`separator`](https://w3c.github.io/aria/#separator) |
| Permitted ARIA roles | [`presentation`](https://w3c.github.io/aria/#presentation) or [`none`](https://w3c.github.io/aria/#none) |
| DOM interface | {{ domxref("HTMLHRElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: Sets the alignment of the rule on the page. If no value is specified, the default value is `left`.

{{ htmlattrdef("color") }} {{ Non-standard_inline }}
: Sets the color of the rule through color name or hexadecimal value.

{{ htmlattrdef("noshade") }} {{ deprecated_inline }}
: Sets the rule to have no shading.

{{ htmlattrdef("size") }} {{ deprecated_inline }}
: Sets the height, in pixels, of the rule.

{{ htmlattrdef("width") }} {{ deprecated_inline }}
: Sets the length of the rule on the page through a pixel or percentage value.

## Example

### HTML

```html
<p>
  This is the first paragraph of text.
  This is the first paragraph of text.
  This is the first paragraph of text.
  This is the first paragraph of text.
</p>

<hr>

<p>
  This is the second paragraph of text.
  This is the second paragraph of text.
  This is the second paragraph of text.
  This is the second paragraph of text.
</p>
```

### Result

{{ EmbedLiveSample("Example") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<hr>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-hr-element) | {{ Spec2('HTML WHATWG') }} | Definition of the `<hr>` element |
| [**HTML 5** The definition of '<hr>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-hr-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<hr>' in that specification](https://www.w3.org/TR/html401/present/graphics.html#h-15.3) | {{ Spec2('HTML4.01') }} | The `align`, `noshade`, `size`, and `width` attributes are deprecated |

## Browser compatibility

{{ Compat("html.elements.hr") }}

## See also

-   [`p`](/html/element/p/)