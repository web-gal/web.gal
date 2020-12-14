---
title: '<rp>: The Ruby Fallback Parenthesis element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Ruby
  - Text
  - Web
permalink: html/element/rp
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rp'
browserCompact: html.elements.rp
---
{{ HTMLRef }}

The **HTML Ruby Fallback Parenthesis (`<rp>`) element** is used to provide fall-back parentheses for browsers that do not support display of ruby annotations using the [`ruby`](/html/element/ruby/) element. One `<rp>` element should enclose each of the opening and closing parentheses that wrap the [`rt`](/html/element/rt/) element that contains the annotation's text.

{{ EmbedInteractiveExample("pages/tabbed/rp.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | Text |
| Tag omission | The end tag can be omitted if the element is immediately followed by an [`rt`](/html/element/rt/) or another `<rp>` element, or if there is no more content in the parent element. |
| Permitted parents | A [`ruby`](/html/element/ruby/) element. `<rp>` must be positioned immediately before or after an [`rt`](/html/element/rt/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

-   Ruby annotations are for showing pronunciation of East Asian characters, like using Japanese furigana or Taiwanese bopomofo characters. The `<rp>` element is used in the case of lack of [`ruby`](/html/element/ruby/) element support; the `<rp>` content provides what should be displayed in order to indicate the presence of a ruby annotation, usually parentheses.

## Examples

This example uses ruby annotations to display the [`Romaji`](https://en.wikipedia.org/wiki/Romaji) equivalents for each character.

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

### CSS

```css
body {
  font-size: 22px;
}
```

The result looks like this in your browser:

{{ EmbedLiveSample("with-ruby", 600, 60) }}

The HTML above rendered by a browser _without_ ruby support might look like this:

```html
漢 (Kan) 字 (ji)
```
```css
body {
  font-size: 22px;
}

```

{{ EmbedLiveSample("without-ruby", 600, 60) }}

See the article about the [`ruby`](/html/element/ruby/) element for further examples.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<rp>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-rp-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<rp>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-rp-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.rp") }}

## See also

-   [`ruby`](/html/element/ruby/)
-   [`rt`](/html/element/rt/)
-   [`rb`](/html/element/rb/)
-   [`rtc`](/html/element/rtc/)