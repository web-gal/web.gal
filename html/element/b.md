---
title: '<b>: The Bring Attention To element'
tags:
  - Attention
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Web
permalink: html/element/b
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b'
browserCompact: html.elements.b
---
{{ HTMLRef }}

The **HTML Bring Attention To element (`<b>`)** is used to draw the reader's attention to the element's contents, which are not otherwise granted special importance. This was formerly known as the Boldface element, and most browsers still draw the text in boldface. However, you should not use `<b>` for styling text; instead, you should use the CSS {{ cssxref("font-weight") }} property to create boldface text, or the [`strong`](/html/element/strong/) element to indicate that text is of special importance.

{{ EmbedInteractiveExample("pages/tabbed/b.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

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

-   Use the `<b>` for cases like keywords in a summary, product names in a review, or other spans of text whose typical presentation would be boldfaced (but not including any special importance).
-   Do not confuse the `<b>` element with the [`strong`](/html/element/strong/), [`em`](/html/element/em/), or [`mark`](/html/element/mark/) elements. The [`strong`](/html/element/strong/) element represents text of certain _importance_, [`em`](/html/element/em/) puts some emphasis on the text and the [`mark`](/html/element/mark/) element represents text of certain _relevance_. The `<b>` element doesn't convey such special semantic information; use it only when no others fit.
-   Similarly, do not mark titles and headings using the `<b>` element. For this purpose, use the [`h1`](/html/element/h1/) to [`h6`](/html/element/h6/) tags. Further, stylesheets can change the default style of these elements, with the result that they are not _necessarily_ displayed in bold.
-   It is a good practice to use the {{ htmlattrxref("class") }} attribute on the `<b>` element in order to convey additional semantic information as needed (for example `<b class="lead">` for the first sentence in a paragraph). This makes it easier to manage multiple use cases of `<b>` if your stylistic needs change, without the need to change all of its uses in the HTML.
-   Historically, the `<b>` element was meant to make text boldface. Styling information has been deprecated since HTML4, so the meaning of the `<b>` element has been changed.
-   If there is no semantic purpose to using the `<b>` element, you should use the CSS {{ cssxref("font-weight") }} property with the value `"bold"` instead in order to make text bold.

## Examples

```html
<p>
  This article describes several <b class="keywords">text-level</b> elements.
  It explains their usage in an <b class="keywords">HTML</b> document.
</p>
Keywords are displayed with the default style of the <b>element, likely in bold.</b>

```

### Result

{{ EmbedLiveSample("Examples") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<b>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-b-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<b>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-b-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<b>' in that specification](https://www.w3.org/TR/html401/present/graphics.html#h-15.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.b") }}

## See also

-   Other elements conveying [text-level semantics](/en-US/docs/HTML/Text_level_semantics_conveying_elements): [`a`](/html/element/a/), [`em`](/html/element/em/), [`strong`](/html/element/strong/), [`small`](/html/element/small/), [`cite`](/html/element/cite/), [`q`](/html/element/q/), [`dfn`](/html/element/dfn/), [`abbr`](/html/element/abbr/), [`time`](/html/element/time/), [`code`](/html/element/code/), [`var`](/html/element/var/), [`samp`](/html/element/samp/), [`kbd`](/html/element/kbd/), [`sub`](/html/element/sub/), [`sup`](/html/element/sup/), [`i`](/html/element/i/), [`mark`](/html/element/mark/), [`ruby`](/html/element/ruby/), [`rp`](/html/element/rp/), [`rt`](/html/element/rt/), [`bdo`](/html/element/bdo/), [`span`](/html/element/span/), [`br`](/html/element/br/), [`wbr`](/html/element/wbr/).
-   [Using <b> and <i> elements (W3C)](https://www.w3.org/International/questions/qa-b-and-i-tags)