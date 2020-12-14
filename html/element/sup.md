---
title: '<sup>: The Superscript element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Web
permalink: html/element/sup
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup'
browserCompact: html.elements.sup
---
{{ HTMLRef }}

The **HTML Superscript element** (**`<sup>`**) specifies inline text which is to be displayed as superscript for solely typographical reasons. Superscripts are usually rendered with a raised baseline using smaller text.

{{ EmbedInteractiveExample("pages/tabbed/sup.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

The `<sup>` element should only be used for typographical reasons—that is, to change the position of the text to comply with typographical conventions or standards, rather than solely for presentation or appearance purposes.

For example, to style the [`wordmark`](https://en.wikipedia.org/wiki/wordmark) of a business or product which uses a raised baseline should be done using CSS (most likely {{ cssxref("vertical-align") }}) rather than `<sup>`. This would be done using, for example, `vertical-align: super` or, to shift the baseline up 50%, `vertical-align: 50%`.

Appropriate use cases for `<sup>` include (but aren't necessarily limited to):

-   Displaying exponents, such as "x3." It may be worth considering the use of [MathML](/mathml) for these, especially in more complex cases. See {{ anch("Exponents") }} under {{ anch("Examples") }} below.
-   Displaying [`superior letter`](https://en.wikipedia.org/wiki/superior_letter), which is used in some languages when rendering certain abbreviations. For example, in French, the word "mademoiselle" can be abbreviated "Mlle"); this is an acceptable use case. See {{ anch("Superior lettering") }} for examples.
-   Representing ordinal numbers, such as "4th" instead of "fourth." See {{ anch("Ordinal numbers") }} for examples.

## Examples

### Exponents

Exponents, or powers of a number, are among the most common uses of superscripted text. For example:

```html
<p>One of the most common equations in all of physics is
<var>E</var>=<var>m</var><var>c</var><sup>2</sup>.<p>
```

The resulting output looks like this:

{{ EmbedLiveSample("Exponents", 650, 80) }}

### Superior lettering

Superior lettering is not technically the same thing as superscript. However, it is common to use `<sup>` to present superior lettering in HTML. Among the most common uses of superior lettering is the presentation of certain abbreviations in French:

```html
<p>Robert a présenté son rapport à M<sup>lle</sup> Bernard.</p>
```

The resulting output:

{{ EmbedLiveSample("Superior_lettering", 650, 80) }}

### Ordinal numbers

Ordinal numbers, such as "fourth" in English or "quinto" in Spanish may be abbreviated using numerals and language-specific text rendered in superscript:

```html
<p>The ordinal number "fifth" can be abbreviated in various
languages as follows:</p>
<ul>
  <li>English: 5<sup>th</sup></li>
  <li>French: 5<sup>ème</sup></li>
</ul>
```

The output:

{{ EmbedLiveSample("Ordinal_numbers", 650, 160) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<sub> and <sup>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-sub-and-sup-elements) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<sub> and <sup>;' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-sub-and-sup-elements) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.sup") }}

## See also

-   The [`sub`](/html/element/sub/) HTML element that produces subscripts. Note that you cannot use them both at the same time and you need to use [MathML](/en-US/docs/MathML) to produce both a superscript and a subscript next to the chemical symbol of an element, representing its atomic number and its nuclear number.
-   The [`<msub>`](/mathml/element/msub), [`<msup>`](/mathml/element/msup), and [`<msubsup>`](/mathml/element/msubsup) MathML elements.
-   The CSS {{ cssxref("vertical-align") }} property.