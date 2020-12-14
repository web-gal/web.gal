---
title: '<small>: the side comment element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
  - font-size
permalink: html/element/small
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small'
browserCompact: html.elements.small
---
{{ HTMLRef }}

The **HTML `<small>`** **element** represents side-comments and small print, like copyright and legal text, independent of its styled presentation. By default, it renders text within it one font-size smaller, such as from `small` to `x-small`.

{{ EmbedInteractiveExample("pages/tabbed/small.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| Content categories | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content) |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content) |
| Tag omission | None, must have both a start tag and an end tag. |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content), or any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Examples

### Basic usage

```html
<p>This is the first sentence.
 <small>This whole sentence is in small letters.</small>
</p>

```

{{ EmbedLiveSample("Basic_usage") }}

### CSS alternative

```html
<p>This is the first sentence.
  <span style="font-size:0.8em">This whole sentence is in small
  letters.</span>
</p>

```

{{ EmbedLiveSample("CSS_alternative") }}

## Specifications

| Specification | Status | Comments |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<small>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-small-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<small>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-small-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<small>' in that specification](https://www.w3.org/TR/html401/present/graphics.html#edef-SMALL) | {{ Spec2('HTML4.01') }} |  |

## Notes

Although the `<small>` element, like the [`b`](/html/element/b/) and [`i`](/html/element/i/) elements, may be perceived to violate the principle of separation between structure and presentation, all three are valid in HTML5. Authors are encouraged to use their best judgement when determining whether to use `<small>` or CSS.

## Browser compatibility

{{ Compat("html.elements.small") }}

## See also

-   [`b`](/html/element/b/)
-   [`sub`](/html/element/sub/) and [`sup`](/html/element/sup/)
-   [`font`](/html/element/font/)
-   [`style`](/html/element/style/)
-   HTML 4.01 Specification: [Font Styles](https://www.w3.org/TR/html4/present/graphics.html#h-15.2)