---
title: '<embed>: The Embed External Content element'
tags:
  - Element
  - Embedding Content
  - External content
  - HTML
  - HTML embedded content
  - HTML5
  - Plugins
  - Reference
  - Web
  - embed
permalink: html/element/embed
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed'
browserCompact: html.elements.embed
---
{{ HTMLRef }}

The **HTML `<embed>` element** embeds external content at the specified point in the document. This content is provided by an external application or other source of interactive content such as a browser plug-in.

{{ EmbedInteractiveExample("pages/tabbed/embed.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

**Note:** This topic documents only the element that is defined as part of HTML5. It does not address earlier, non-standardized implementation of the element.

Keep in mind that most modern browsers have deprecated and removed support for browser plug-ins, so relying upon `<embed>` is generally not wise if you want your site to be operable on the average user's browser.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), [phrasing content](/guide/html/content_categories#phrasing_content), embedded content, interactive content, [palpable content](/guide/html/content_categories#palpable_content). |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | Must have a start tag, and must not have an end tag. |
| Permitted parents | Any element that accepts embedded content. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`application`](https://w3c.github.io/aria/#application), [`document`](https://w3c.github.io/aria/#document), [`img`](https://w3c.github.io/aria/#img), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation) |
| DOM interface | {{ domxref("HTMLEmbedElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("height") }}
: The displayed height of the resource, in [CSS pixels](https://drafts.csswg.org/css-values/#px). This must be an absolute value; percentages are _not_ allowed.

{{ htmlattrdef("src") }}
: The URL of the resource being embedded.

{{ htmlattrdef("type") }}
: The [MIME type](/glossary/mime_type/) to use to select the plug-in to instantiate.

{{ htmlattrdef("width") }}
: The displayed width of the resource, in [CSS pixels](https://drafts.csswg.org/css-values/#px). This must be an absolute value; percentages are _not_ allowed.

## Usage notes

You can use the {{ cssxref("object-position") }} property to adjust the positioning of the embedded object within the element's frame, and the {{ cssxref("object-fit") }} property to control how the object's size is adjusted to fit within the frame.

## Examples

```html
<embed type="video/quicktime" src="movie.mov" width="640" height="480" title="Title of my video">

```

## Accessibility concerns

Use the [`title` attribute](/html/global_attributes/title) on an `embed` element to label its content so that people navigating with assistive technology such as a screen reader can understand what it contains. The title's value should concisely describe the embedded content. Without a title, they may not be able to determine what its embedded content is. This context shift can be confusing and time-consuming, especially if the `embed` element contains interactive content like video or audio.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<embed>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-embed-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<embed>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-embed-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

**Note**: Prior to version 45, Firefox did not display content of HTML resource, but a generic message saying the content needs a plug-in (see [bug 730768](https://bugzilla.mozilla.org/show_bug.cgi?id=730768)).

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.embed") }}

## See also

-   Other elements that are used for embedding content of various types include [`audio`](/html/element/audio/), [`canvas`](/html/element/canvas/), [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), {{ MathMLElement("math") }}, [`object`](/html/element/object/), {{ SVGElement("svg") }}, and [`video`](/html/element/video/).
-   Positioning and sizing the embedded content within its frame: {{ cssxref("object-position") }} and {{ cssxref("object-fit") }}