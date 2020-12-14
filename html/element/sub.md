---
title: '<sub>: The Subscript element'
tags:
  - Baseline
  - Element
  - Footnotes
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Subscript
  - Web
  - sub
permalink: html/element/sub
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub'
browserCompact: html.elements.sub
---
{{ HTMLRef }}

The HTML **Subscript element** (**`<sub>`**) specifies inline text which should be displayed as subscript for solely typographical reasons. Subscripts are typically rendered with a lowered baseline using smaller text.

{{ EmbedInteractiveExample("pages/tabbed/sub.html", "tabbed-shorter") }}

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

The `<sub>` element should be used only for typographical reasons—that is, to change the position of the text to comply with typographical conventions or standards, rather than solely for presentation or appearance purposes.

For example, using `<sub>` to style the name of a company which uses altered baselines in their [`wordmark`](https://en.wikipedia.org/wiki/wordmark) would not be appropriate; instead, CSS should be used (likely the {{ cssxref("vertical-align") }} property, such as `vertical-align: sub` or, to more precisely control the baseline shift, `vertical-align: -25%`.

Appropriate use cases for `<sub>` include (but aren't necessarily limited to):

-   Marking up footnote numbers. See {{ anch("Footnote numbers") }} for an example.
-   Marking up the subscript in mathematical variable numbers (although you may also consider using a [MathML](/mathml) formula for this). See {{ anch("Variable subscripts") }}.
-   Denoting the number of atoms of a given element within a chemical formula (such as every developer's best friend, C8H10N4O2, otherwise known as "caffeine"). See {{ anch("Chemical formulas") }}.

## Examples

### Footnote numbers

Traditional footnotes are denoted using numbers which are rendered in subscript. This is a common use case for `<sub>`:

```html
<p>According to the computations by Nakamura, Johnson, and
Mason<sub>1</sub> this will result in the complete annihilation
of both particles.</p>
```

The resulting output looks like this:

{{ EmbedLiveSample("Footnote_numbers", 650, 80) }}

### Variable subscripts

In mathematics, families of variables related to the same concept (such as distances along the same axis) are represented using the same variable name with a subscript following. For example:

```html
<p>The horizontal coordinates' positions along the X-axis are
represented as <var>x<sub>1</sub></var> ... <var>x<sub>n</sub></var>.</p>
```

The resulting output:

{{ EmbedLiveSample("Variable_subscripts", 650, 80) }}

### Chemical formulas

When writing a chemical formula, such as H20, the number of atoms of a given element within the described molecule is represented using a subscripted number; in the case of water, the subscripted "2" indicates that there are two atoms of hydrogen in the molecule.

Another example:

```html
<p>Almost every developer's favorite molecule is
C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>, which is
commonly known as "caffeine."</p>
```

The output:

{{ EmbedLiveSample("Chemical_formulas", 650, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<sub> and <sup>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-sub-and-sup-elements) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<sub> and <sup>;' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-sub-and-sup-elements) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.sub") }}

## See also

-   The [`sup`](/html/element/sup/) HTML element that produces superscript. Note that you cannot use them both at the same time and you need to use [MathML](/en-US/docs/MathML) to produce both a superscript directly above a subscript next to the chemical symbol of an element, representing its atomic number and its nuclear number.
-   The [`<msub>`](/en-US/docs/MathML/Element/msub), [`<msup>`](/en-US/docs/MathML/Element/msup), and [`<msubsup>`](/en-US/docs/MathML/Element/msubsup) MathML elements.
-   The CSS {{ cssxref("vertical-align") }} property.