---
title: <span>
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - Reference
  - Web
permalink: html/element/span
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span'
browserCompact: html.elements.span
---
{{ HTMLRef }}

The **HTML `<span>` element** is a generic inline container for phrasing content, which does not inherently represent anything. It can be used to group elements for styling purposes (using the {{ htmlattrxref("class") }} or {{ htmlattrxref("id") }} attributes), or because they share attribute values, such as {{ htmlattrxref("lang") }}. It should be used only when no other semantic element is appropriate. `<span>` is very much like a [`div`](/html/element/div/) element, but [`div`](/html/element/div/) is a [block-level element](/html/block-level_elements) whereas a `<span>` is an [inline element](/html/inline_elements).

{{ EmbedInteractiveExample("pages/tabbed/span.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content). |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content), or any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLSpanElement") }} (before [HTML5](/glossary/html5/), the interface was {{ domxref("HTMLElement") }}) |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Example

### Example 1

#### HTML

```html
<p><span>Some text</span></p>
```

#### Result

{{ EmbedLiveSample('Example_1') }}

### Example 2

#### HTML

```html
<li><span>
    <a href="portfolio.html" target="_blank">See my portfolio</a>
</span></li>

```

#### CSS

```css
li span {
  background: gold;
 }

```

#### Result

{{ EmbedLiveSample('Example_2') }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<span>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-span-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<span>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-span-element) | {{ Spec2('HTML5 W3C') }} | The [DOM](/glossary/dom/) interface is now {{ domxref("HTMLSpanElement") }}. |
| [**HTML 4.01 Specification** The definition of '<span>' in that specification](https://www.w3.org/TR/html401/struct/global.html#edef-SPAN) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.span") }}

## See also

-   HTML [`div`](/html/element/div/) element