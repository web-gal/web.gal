---
title: <wbr>
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
permalink: html/element/wbr
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/wbr'
browserCompact: html.elements.wbr
---
{{ HTMLRef }}

The **HTML `<wbr>` element** represents a word break opportunity—a position within text where the browser may optionally break a line, though its line-breaking rules would not otherwise create a break at that location.

{{ EmbedInteractiveExample("pages/tabbed/wbr.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), [phrasing content](/guide/html/content_categories#phrasing_content). |
| Permitted content | Empty |
| Tag omission | It is an [empty element](/glossary/empty_element/); it must have a start tag, but must not have an end tag. |
| Permitted parents | Any element that accepts [phrasing content](/guide/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes).

## Notes

On UTF-8 encoded pages, `<wbr>` behaves like the `U+200B` `ZERO-WIDTH SPACE` code point. In particular, it behaves like a Unicode bidi BN code point, meaning it has no effect on [bidi](/glossary/bidi/)-ordering: `<div dir=rtl>123,<wbr>456</div>` displays, when not broken on two lines, `123,456` and not `456,123`.

For the same reason, the `<﻿wbr﻿>` element does not introduce a hyphen at the line break point. To make a hyphen appear only at the end of a line, use the soft hyphen character entity (`&﻿shy;`) instead.

This element was first implemented in Internet Explorer 5.5 and was officially defined in HTML5.

## Example

_[The Yahoo Style Guide](https://web.archive.org/web/20121105171040/http://styleguide.yahoo.com/)_ recommends [breaking a URL _before_ punctuation](https://web.archive.org/web/20121105171040/http://styleguide.yahoo.com/editing/treat-abbreviations-capitalization-and-titles-consistently/website-names-and-addresses), to avoid leaving a punctuation mark at the end of the line, which the reader might mistake for the end of the URL.

```html
<p>http://this<wbr>.is<wbr>.a<wbr>.really<wbr>.long<wbr>.example<wbr>.com/With<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages</p>

```

{{ EmbedLiveSample("Example") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<wbr>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-wbr-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<wbr>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-wbr-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.wbr") }}

## See also

-   {{ cssxref("overflow-wrap") }}
-   {{ cssxref("word-break") }}
-   {{ cssxref("hyphens") }}
-   The [`br`](/html/element/br/) element