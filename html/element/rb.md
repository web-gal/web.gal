---
title: '<rb>: The Ruby Base element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Ruby
  - Text
  - Web
permalink: html/element/rb
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rb'
nonStandard: true
browserCompact: html.elements.rb
---
{{ HTMLRef }}

The **HTML Ruby Base (`<rb>`) element** is used to delimit the base text component of a  [`ruby`](/html/element/ruby/) annotation, i.e. the text that is being annotated. One `<rb>` element should wrap each separate atomic segment of the base text.

\{{ EmbedInteractiveExample("pages/tabbed/rb.html", "tabbed-standard") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | As a child of a [`ruby`](/html/element/ruby/) element. |
| Tag omission | The end tag can be omitted if the element is immediately followed by an [`rt`](/html/element/rt/), [`rtc`](/html/element/rtc/), or [`rp`](/html/element/rp/) element or another `<rb>` element, or if there is no more content in the parent element. |
| Permitted parents | A [`ruby`](/html/element/ruby/) element. |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes).

## Usage notes

-   Ruby annotations are for showing pronunciation of East Asian characters, like using Japanese furigana or Taiwanese bopomofo characters. The `<rb>` element is used to separate out each segment of the ruby base text.
-   Even though `<rb>` is not an empty element, it is common to just include the opening tag of each element in the source code, so that the ruby markup is less complex and easier to read. The browser can then fill in the full element in the rendered version.
-   You need to include one [`rt`](/html/element/rt/) element for each base segment/`<rb>` element that you want to annotate.

## Examples

In this example, we provide an annotation for the original character equivalent of "Kanji":

```html
<ruby>
  <rb>漢<rb>字
  <rp>(</rp><rt>kan<rt>ji<rp>)</rp>
</ruby>
```

Note how we've included two `<rb>` elements, to delimit the two separate parts of the ruby base text. The annotation on the other hand is delimited by two [`rt`](/html/element/rt/) elements.

Note that we could also write this example with the two base text parts annotated completely separately. In this case we don't need to include `<rb>` elements:

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

```html
<ruby> <rb>漢<rb>字 <rp>(</rp><rt>kan<rt>ji<rp>)</rp> </ruby>

```
```css
body {
  font-size: 22px;
}
```

The output looks like so:

{{ EmbedLiveSample("with-ruby", "100%", 60) }}

The HTML above might look something like this when rendered by a browser _without_ ruby support:

```html
漢字 (kan ji)
```
```css
body {
  font-size: 22px;
}

```

{{ EmbedLiveSample("without-ruby", "100%", 60) }}

**Note**: See the article about the [`ruby`](/html/element/ruby/) element for further examples.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5** The definition of '<rb>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-rb-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.rb") }}

## See also

-   [`ruby`](/html/element/ruby/)
-   [`rt`](/html/element/rt/)
-   [`rp`](/html/element/rp/)
-   [`rtc`](/html/element/rtc/)