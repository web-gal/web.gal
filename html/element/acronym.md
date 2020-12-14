---
title: <acronym>
tags:
  - Element
  - HTML
  - 'HTML:Flow content'
  - Obsolete
  - Reference
  - Web
permalink: html/element/acronym
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/acronym'
obsolete: true
browserCompact: html.elements.acronym
---
## Summary

The HTML Acronym Element (`<acronym>`) allows authors to clearly indicate a sequence of characters that compose an acronym or abbreviation for a word.

**Usage note:** This element has been removed in HTML5 and shouldn't be used anymore. Instead web developers should use the [`abbr`](/html/element/abbr/) element.

## Attributes

This element only has [global attributes](/en-US/docs/HTML/global_attributes "HTML/global attributes"), which are common to all elements.

## DOM Interface

This element implements the {{ domxref('HTMLElement') }} interface.

**Implementation note:** Up to Gecko 1.9.2 inclusive, Firefox implements the {{ domxref('HTMLSpanElement') }} interface for this element.

## Example

```html
<p>The <acronym title="World Wide Web">WWW</acronym> is only a component of the Internet.</p>

```

## Default styling

Though the purpose of this tag is purely for the convenience of the author, its default styling varies from one browser to another:

-   Some browsers, like Internet Explorer, do not style it differently than a [`span`](/html/element/span/) element.
-   Opera, Firefox, Chrome, and some others add a dotted underline to the content of the element.
-   A few browsers not only add a dotted underline, but also put it in small caps; to avoid this styling, adding something like {{ cssxref('font-variant') }}`: none` in the CSS takes care of this case.

It is therefore recommended that web authors either explicitly style this element, or accept some cross-browser variation.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 4.01 Specification** The definition of '<acronym>' in that specification](https://www.w3.org/TR/html401/struct/text.html#edef-ACRONYM) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.acronym") }}

## See also

-   The [`abbr`](/html/element/abbr/) HTML element

{{ HTMLRef }}