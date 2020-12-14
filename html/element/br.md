---
title: '<br>: The Line Break element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
permalink: html/element/br
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br'
browserCompact: html.elements.br
---
{{ HTMLRef }}

The **HTML `<br>` element** produces a line break in text (carriage-return). It is useful for writing a poem or an address, where the division of lines is significant.

{{ EmbedInteractiveExample("pages/tabbed/br.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

As you can see from the above example, a `<br>` element is included at each point where we want the text to break. The text after the `<br>` begins again at the start of the next line of the text block.

**Note**: Do not use `<br>` to create margins between paragraphs; wrap them in [`p`](/html/element/p/) elements and use the [CSS](/css) {{ cssxref('margin') }} property to control their size.

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

### Deprecated attributes

{{ htmlattrdef("clear") }}
: Indicates where to begin the next line after the break.

## Styling with CSS

The `<br>` element has a single, well-defined purpose — to create a line break in a block of text. As such, it has no dimensions or visual output of its own, and there is very little you can do to style it.

You can set a {{ cssxref("margin") }} on `<br>` elements themselves to increase the spacing between the lines of text in the block, but this is a bad practice — you should use the {{ cssxref("line-height") }} property that was designed for that purpose.

## Examples

### Simple br

In the following example we use `<br>` elements to create line breaks between the different lines of a postal address:

```html
Mozilla<br>
331 E. Evelyn Avenue<br>
Mountain View, CA<br>
94041<br>
USA<br>

```

The result looks like so:

{{ EmbedLiveSample('Simple_br', '100%', '90')  }}

## Accessibility concerns

Creating separate paragraphs of text using `<br>` is not only bad practice, it is problematic for people who navigate with the aid of screen reading technology. Screen readers may announce the presence of the element, but not any content contained within `<br>`s. This can be a confusing and frustrating experience for the person using the screen reader.

Use `<p>` elements, and use CSS properties like {{ cssxref("margin") }} to control their spacing.

## Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content). |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | Must have a start tag, and must not have an end tag. In XHTML documents, write this element as `<br />`. |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation) |
| DOM interface | {{ domxref("HTMLBRElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<br>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-br-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<br>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-br-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<br>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.3.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.br") }}

## See also

-   [`address`](/html/element/address/) element
-   [`p`](/html/element/p/) element
-   [`wbr`](/html/element/wbr/) element