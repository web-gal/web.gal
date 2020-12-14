---
title: '<del>: The Deleted Text element'
tags:
  - Deleted Text
  - Element
  - HTML
  - HTML edits
  - Reference
  - Web
  - del
permalink: html/element/del
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del'
browserCompact: html.elements.del
---
{{ HTMLRef }}

The **HTML `<del>` element** represents a range of text that has been deleted from a document. This can be used when rendering "track changes" or source code diff information, for example. The [`ins`](/html/element/ins/) element can be used for the opposite purpose: to indicate text that has been added to the document.

{{ EmbedInteractiveExample("pages/tabbed/del.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

This element is often (but need not be) rendered by applying a strike-through style to the text.

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | [Phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content), [flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Permitted content | [Transparent](/en-US/docs/HTML/Content_categories#Transparent_content_model). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLModElement") }} |

## Attributes

This element's attributes include the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("cite") }}
: A URI for a resource that explains the change (for example, meeting minutes).

{{ htmlattrdef("datetime") }}
: This attribute indicates the time and date of the change and must be a valid date string with an optional time. If the value cannot be parsed as a date with an optional time string, the element does not have an associated time stamp. For the format of the string without a time, see [Date strings](/html/date_and_time_formats#date_strings). The format of the string if it includes both date and time is covered in [Local date and time strings](/html/date_and_time_formats#local_date_and_time_strings).

## Examples

```html
<p><del>This text has been deleted</del>,
here is the rest of the paragraph.</p>
<del><p>This paragraph has been deleted.</p></del>
```

### Result

{{ EmbedLiveSample("Examples") }}

## Accessibility concerns

The presence of the `del` element is not announced by most screen reading technology in its default configuration. It can be made to be announced by using the CSS {{ cssxref("content") }} property, along with the {{ cssxref("::before") }} and {{ cssxref("::after") }} pseudo-elements.

```
del::before,
del::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

del::before {
  content: " [deletion start] ";
}

del::after {
  content: " [deletion end] ";
}

```

Some people who use screen readers deliberately disable announcing content that creates extra verbosity. Because of this, it is important to not abuse this technique and only apply it in situations where not knowing content has been deleted would adversely affect understanding.

-   [Short note on making your mark (more accessible) | The Paciello Group](https://developer.paciellogroup.com/blog/2017/12/short-note-on-making-your-mark-more-accessible/)
-   [Tweaking Text Level Styles | Adrian Roselli](http://adrianroselli.com/2017/12/tweaking-text-level-styles.html)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<del>' in that specification](https://html.spec.whatwg.org/multipage/edits.html#the-del-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<del>' in that specification](https://www.w3.org/TR/html52/edits.html#the-del-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<del>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.4) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.del") }}

## See also

-   [`ins`](/html/element/ins/) element for insertions into a text
-   [`s`](/html/element/s/) element for strikethrough separate from representing deletion of text