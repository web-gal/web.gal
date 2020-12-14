---
title: <ruby>
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
permalink: html/element/ruby
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ruby'
browserCompact: html.elements.ruby
---
{{ HTMLRef }}

The **HTML `<ruby>` element** represents small annotations that are rendered above, below, or next to base text, usually used for showing the pronunciation of East Asian characters. It can also be used for annotating other kinds of text, but this usage is less common.

The term _ruby_ originated as [a unit of measurement used by typesetters](https://en.wikipedia.org/wiki/Agate_(typography)), representing the smallest size that text can be printed on newsprint while remaining legible.

{{ EmbedInteractiveExample("pages/tabbed/ruby.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Examples

### Example 1: Character

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

### Example 2: Word

```html
<ruby>
  明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp>
</ruby>
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<ruby>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-ruby-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<ruby>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-ruby-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.ruby") }}

## See also

-   [`rt`](/html/element/rt/)
-   [`rp`](/html/element/rp/)
-   [`rb`](/html/element/rb/)
-   [`rtc`](/html/element/rtc/)
-   [`rbc`](/html/element/rbc/)
-   {{ CSSxRef("text-transform") }}: full-size-kana