---
title: '<center>: The Centered Text element (obsolete)'
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Text
  - Text Alignment
  - Web
  - alignment
  - center
permalink: html/element/center
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/center'
obsolete: true
browserCompact: html.elements.center
---
The obsolete **HTML Center Element** (**`<center>`**) is a [block-level element](/en-US/docs/HTML/Block-level_elements "HTML/Block-level_elements") that displays its block-level or inline contents centered horizontally within its containing element. The container is usually, but isn't required to be, [`body`](/html/element/body/).

This tag has been deprecated in HTML 4 (and XHTML 1) in favor of the [CSS](/css "/en-US/docs/Web/CSS") {{ Cssxref("text-align") }} property, which can be applied to the [`div`](/html/element/div/) element or to an individual [`p`](/html/element/p/). For centering blocks, use other CSS properties like {{ Cssxref("margin-left") }} and {{ Cssxref("margin-right") }} and set them to `auto` (or set {{ Cssxref("margin") }} to `0 auto`).

## DOM interface

This element implements the {{ domxref("HTMLElement") }} interface.

**Implementation note:** up to Gecko 1.9.2 inclusive, Firefox implements the {{ domxref("HTMLSpanElement") }} interface for this element.

## Example 1

```html
<center>This text will be centered.
<p>So will this paragraph.</p></center>

```

## Example 2 (CSS alternative)

```html
<div style="text-align:center">This text will be centered.
<p>So will this paragraph.</p></div>

```

## Example 3 (CSS alternative)

```html
<p style="text-align:center">This line will be centered.<br>
And so will this line.</p>

```

## Note

Applying {{ Cssxref("text-align") }}`:center` to a [`div`](/html/element/div/) or [`p`](/html/element/p/) element centers the _contents_ of those elements while leaving their overall dimensions unchanged.

## Browser compatibility

{{ Compat("html.elements.center") }}

## See also

-   {{ Cssxref("text-align") }}
-   {{ Cssxref("display") }}

{{ HTMLRef }}