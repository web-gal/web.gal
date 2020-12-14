---
title: '<big>: The Bigger Text element'
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
permalink: html/element/big
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/big'
obsolete: true
browserCompact: html.elements.big
---
The obsolete **HTML Big Element** (**`<big>`**) renders the enclosed text at a font size one level larger than the surrounding text (`medium` becomes `large`, for example). The size is capped at the browser's maximum permitted font size.

**Usage note:** As it was purely presentational, this element has been removed in [HTML5](/guide/html/html5 "/en-US/docs/Web/Guide/HTML/HTML5") and shouldn't be used anymore. Instead web developers should use the CSS {{ cssxref("font-size") }} property to adjust the font size.

## Attributes

This element has no other attributes than the [global attributes](/en-US/docs/HTML/global_attributes "HTML/global attributes"), common to all elements.

## Examples

Here we see examples showing the use of `<big>` followed by an example showing how to accomplish the same results using modern CSS syntax instead.

### Using `<big>`

This example uses the obsolete `<big>` element to increase the size of some text.

#### HTML

```html
<p>
  This is the first sentence. <big>This whole
  sentence is in bigger letters.</big>
</p>
```

#### Result

{{ EmbedLiveSample("Using_big", 640, 60) }}

### Using CSS `font-size`

This example uses the CSS {{ cssxref("font-size") }} property to increase the font size by one level.

#### CSS

```css
.bigger {
  font-size: larger;
}
```

#### HTML

```html
<p>
  This is the first sentence. <span class="bigger">This whole
  sentence is in bigger letters.</span>
</p>
```

#### Result

{{ EmbedLiveSample("Using_CSS_font-size", 640, 60) }}

## DOM interface

This element implements the {{ domxref('HTMLElement') }} interface.

**Implementation note:** Up to Gecko 1.9.2 inclusive, Firefox implements the {{ domxref('HTMLSpanElement') }} interface for this element.

## Browser compatibility

{{ Compat("html.elements.big") }}

## See also

-   CSS: {{ cssxref("font-size") }}, {{ cssxref("font") }}
-   HTML: [`small`](/html/element/small/), [`font`](/html/element/font/), [`style`](/html/element/style/)
-   HTML 4.01 Specification: [Font Styles](http://www.w3.org/TR/html4/present/graphics.html#h-15.2)

{{ HTMLRef }}