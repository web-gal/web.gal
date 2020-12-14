---
title: <strike>
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
permalink: html/element/strike
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strike'
obsolete: true
browserCompact: html.elements.strike
---
{{ HTMLRef }}

The **HTML `<strike>` element** (or _HTML Strikethrough Element_) places a strikethrough (horizontal line) over text.

**Usage note:** This element is deprecated in HTML 4 and XHTML 1, and obsoleted in HTML5. If semantically appropriate, i.e., if it represents _deleted_ content, use [`del`](/html/element/del/) instead. In all other cases use [`s`](/html/element/s/).

| Property | Value |
| --- | --- |
| DOM interface | {{ DOMxRef("HTMLElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

## Example

```html
&lt;strike&gt;:	<strike>Today's Special: Salmon</strike> SOLD OUT<br />
&lt;s&gt;:	<s>Today's Special: Salmon</s> SOLD OUT

```

The result of this code is:

{{ EmbedLiveSample("Example") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5** The definition of '<strike>' in that specification](https://www.w3.org/TR/html52/obsolete.html#strike) | {{ Spec2("HTML5 W3C") }} | Make obsolete in favor of [`del`](/html/element/del/) and [`s`](/html/element/s/). |
| [**HTML 4.01 Specification** The definition of '<strike>' in that specification](https://www.w3.org/TR/html401//present/graphics.html#edef-STRIKE) | {{ Spec2("HTML4.01") }} | Make deprecated in favor of [`del`](/html/element/del/) and [`s`](/html/element/s/). |

## Browser compatibility

{{ Compat("html.elements.strike") }}

## See also

-   The [`s`](/html/element/s/) element.
-   The [`del`](/html/element/del/) element should be used if the data has been _deleted_.
-   The CSS {{ CSSxRef("text-decoration") }} property can be used to style text with a strikethrough.