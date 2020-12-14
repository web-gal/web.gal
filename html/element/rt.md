---
title: '<rt>: The Ruby Text element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Ruby
  - Text
  - Web
permalink: html/element/rt
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rt'
browserCompact: html.elements.rt
---
{{ HTMLRef }}

The **HTML Ruby Text (`<rt>`) element** specifies the ruby text component of a ruby annotation, which is used to provide pronunciation, translation, or transliteration information for East Asian typography. The `<rt>` element must always be contained within a [`ruby`](/html/element/ruby/) element.

{{ EmbedInteractiveExample("pages/tabbed/rt.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

See the article about the [`ruby`](/html/element/ruby/) element for more examples.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | The end tag may be omitted if the `<rt>` element is immediately followed by an `<rt>` or [`rp`](/html/element/rp/) element, or if there is no more content in the parent element |
| Permitted parents | A [`ruby`](/html/element/ruby/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Examples

This simple example provides Romaji transliteration for the kanji characters within the [`ruby`](/html/element/ruby/) element:

```html
<ruby>
  漢 <rt>Kan</rt>
  字 <rt>ji</rt>
</ruby>

```

```css
body {
  font-size: 22px;
}

```

The output looks like this in your browser:

{{ EmbedLiveSample("with-ruby", 600, 60) }}

On a browser _without_ ruby support, this example might look like this:

```html
漢 Kan 字 ji
```
```css
body {
  font-size: 22px;
}

```

{{ EmbedLiveSample("without-ruby", 600, 60) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<rt>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-rt-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<rt>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-rt-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.rt") }}

## See also

-   [`ruby`](/html/element/ruby/)
-   [`rp`](/html/element/rp/)
-   [`rb`](/html/element/rb/)
-   [`rtc`](/html/element/rtc/)
-   {{ CSSXRef("text-transform", "text-transform: full-size-kana") }}