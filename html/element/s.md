---
title: <s>
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
  - text-decoration
permalink: html/element/s
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/s'
browserCompact: html.elements.s
---
{{ HTMLRef }}

The **HTML `<s>` element** renders text with a strikethrough, or a line through it. Use the `<s>` element to represent things that are no longer relevant or no longer accurate. However, `<s>` is not appropriate when indicating document edits; for that, use the [`del`](/html/element/del/) and [`ins`](/html/element/ins/) elements, as appropriate.

{{ EmbedInteractiveExample("pages/tabbed/s.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Phrasing content](/html/content_categories#phrasing_content), [flow content](/html/content_categories#flow_content). |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

**Implementation note:** Up to Gecko 1.9.2 inclusive, Firefox implements the {{ domxref("HTMLSpanElement") }} interface for this element.

## Examples

```html
<s>Today's Special: Salmon</s> SOLD OUT<br>
<span style="text-decoration:line-through;">Today's Special:
  Salmon</span> SOLD OUT
```

{{ EmbedLiveSample("Examples") }}

## Accessibility concerns

The presence of the `s` element is not announced by most screen reading technology in its default configuration. It can be made to be announced by using the CSS {{ cssxref("content") }} property, along with the {{ cssxref("::before") }} and {{ cssxref("::after") }} pseudo-elements.

```css
s::before,
s::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

s::before {
  content: " [start of stricken text] ";
}

s::after {
  content: " [end of stricken text] ";
}

```

Some people who use screen readers deliberately disable announcing content that creates extra verbosity. Because of this, it is important to not abuse this technique and only apply it in situations where not knowing content has been struck out would adversely affect understanding.

-   [Short note on making your mark (more accessible) | The Paciello Group](https://developer.paciellogroup.com/blog/2017/12/short-note-on-making-your-mark-more-accessible/)
-   [Tweaking Text Level Styles | Adrian Roselli](http://adrianroselli.com/2017/12/tweaking-text-level-styles.html)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 's element' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-s-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 's element' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-s-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.s") }}

## See also

-   The [`strike`](/html/element/strike/) element, alter ego of the [`s`](/html/element/s/) element is obsolete and should not be used on Web sites any more.
-   The [`del`](/html/element/del/) element is to be used instead if the data has been _deleted_.
-   The CSS {{ cssxref("text-decoration-line") }} property is to be used to achieve the former visual aspect of the [`s`](/html/element/s/) element.