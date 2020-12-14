---
title: '<rtc>: The Ruby Text Container element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - NeedsContent
  - Reference
  - Ruby Text
  - Text
  - Web
  - rtc
permalink: html/element/rtc
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rtc'
browserCompact: html.elements.rtc
---
{{ HTMLRef }}

The **HTML Ruby Text Container (`<rtc>`) element** embraces semantic annotations of characters presented in a ruby of [`rb`](/html/element/rb/) elements used inside of [`ruby`](/html/element/ruby/) element. [`rb`](/html/element/rb/) elements can have both pronunciation ([`rt`](/html/element/rt/)) and semantic ([`rtc`](/html/element/rtc/)) annotations.

{{ EmbedInteractiveExample("pages/tabbed/rtc.html", "tabbed-standard") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content) or [`rt`](/html/element/rt/) elements. |
| Tag omission | The closing tag can be omitted if it is immediately followed by a [`rb`](/html/element/rb/), [`rtc`](/html/element/rtc/) or [`rt`](/html/element/rt/) element opening tag or by its parent closing tag. |
| Permitted parents | A [`ruby`](/html/element/ruby/) element. |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes).

## Examples

```html
<div class="info">
  <ruby>
    <rbc>
      <rb>旧</rb><rt>jiù</rt>
      <rb>金</rb><rt>jīn</rt>
      <rb>山</rb><rt>shān</rt>
    </rbc>
    <rtc>San Francisco</rtc>
  </ruby>
</div>

```

```css
.info {
  padding-top: 10px;
  font-size: 36px;
}

```

{{ EmbedLiveSample("Examples", 600, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5.2** The definition of '<rtc>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-rtc-element) | {{ Spec2('HTML5.2') }} |  |
| [**HTML 5.1** The definition of '<rtc>' in that specification](https://www.w3.org/TR/html51/textlevel-semantics.html#the-rtc-element) | {{ Spec2('HTML5.1') }} |  |
| [**HTML 5** The definition of '<rtc>' in that specification](https://www.w3.org/TR/html52/text-level-semantics.html#the-rtc-element) | {{ Spec2('HTML5 W3C') }} | Initial definition. |

## Browser compatibility

{{ Compat("html.elements.rtc") }}

## See also

-   [`ruby`](/html/element/ruby/)
-   [`rp`](/html/element/rp/)
-   [`rb`](/html/element/rb/)
-   [`rt`](/html/element/rt/)
-   [`rbc`](/html/element/rbc/)