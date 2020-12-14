---
title: '<strong>: The Strong Importance element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Strong Importance
  - Urgency
  - Web
  - strong
permalink: html/element/strong
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong'
browserCompact: html.elements.strong
---
{{ HTMLRef }}

The HTML **Strong Importance Element** (**`<strong>`**) indicates that its contents have strong importance, seriousness, or urgency. Browsers typically render the contents in bold type.

{{ EmbedInteractiveExample("pages/tabbed/strong.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | None, must have both a start tag and an end tag. |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content), or any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

The `<strong>` element is for content that is of "strong importance," including things of great seriousness or urgency (such as warnings). This could be a sentence that is of great importance to the whole page, or you could merely try to point out that some words are of greater importance compared to nearby content.

Typically this element is rendered by default using a bold font weight. However, it should _not_ be used simply to apply bold styling; use the CSS {{ cssxref("font-weight") }} property for that purpose. Use the [`b`](/html/element/b/) element to draw attention to certain text without indicating a higher level of importance. Use the [`em`](/html/element/em/) element to mark text that has stress emphasis.

Another accepted use for `<strong>` is to denote the labels of paragraphs which represent notes or warnings within the text of a page.

### <b> vs. <strong>

It is often confusing to new developers why there are so many ways to express the same thing on a rendered website. [`b`](/html/element/b/) and `<strong>` are perhaps one of the most common sources of confusion, causing developers to ask "Should I use `<b>` or `<strong>`? Don't they both do the same thing?"

Not exactly. The `<strong>` element is for content that is of greater importance, while the `<b>` element is used to draw attention to text without indicating that it's more important.

It may help to realize that both are valid and semantic elements in HTML5 and that it's a coincidence that they both have the same default styling (boldface) in most browsers (although some older browsers actually underline `<strong>`). Each element is meant to be used in certain types of scenarios, and if you want to bold text simply for decoration, you should instead actually use the CSS {{ cssxref("font-weight") }} property.

The intended meaning or purpose of the enclosed text should be what determines which element you use. Communicating meaning is what semantics are all about.

### <em> vs. <strong>

Adding to the confusion is the fact that while HTML 4 defined `<strong>` as simply indicating a stronger emphasis, HTML 5 defines `<strong>` as representing "strong importance for its contents." This is an important distinction to make.

While `<em>` is used to change the meaning of a sentence as spoken emphasis does ("I _love_ carrots" vs. "I love _carrots_"), `<strong>` is used to give portions of a sentence added importance (e.g., "**Warning!** This is **very dangerous.**") Both `<strong>` and `<em>` can be nested to increase the relative degree of importance or stress emphasis, respectively.

## Examples

### Basic example

```html
<p>Before proceeding, <strong>make sure you put on your safety goggles</strong>.</p>
```

The resulting output:

{{ EmbedLiveSample("Basic_example", 650, 80) }}

### Labeling warnings

```html
<p><strong>Important:</strong> Before proceeding, make sure you add plenty of butter.</p>
```

This results in:

{{ EmbedLiveSample("Labeling_warnings", 650, 80) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<strong>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-strong-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<strong>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-strong-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<strong>' in that specification](https://www.w3.org/TR/html401/struct/text.html#edef-STRONG) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.strong") }}

## See also

-   The [`b`](/html/element/b/) element
-   The [`em`](/html/element/em/) element
-   The {{ cssxref("font-weight") }} property