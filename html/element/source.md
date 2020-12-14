---
title: '<source>: The Media or Image Source element'
tags:
  - Element
  - HTML
  - HTML embedded content
  - Media
  - Reference
  - Web
  - Web Performance
permalink: html/element/source
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source'
browserCompact: html.elements.source
---
{{ HTMLRef }}

The **HTML `<source>` element** specifies multiple media resources for the [`picture`](/html/element/picture/), the [`audio`](/html/element/audio/) element, or the [`video`](/html/element/video/) element. It is an empty element, meaning that it has no content and does not have a closing tag. It is commonly used to offer the same media content in multiple file formats in order to provide compatibility with a broad range of browsers given their differing support for [image file formats](/media/formats/image_types) and [media file formats](/media/formats).

{{ EmbedInteractiveExample("pages/tabbed/source.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | It must have a start tag, but must not have an end tag. |
| Permitted parents | 
A media element—[`audio`](/html/element/audio/) or [`video`](/html/element/video/)—and it must be placed before any [flow content](/html/content_categories#flow_content) or [`track`](/html/element/track/) element.

A [`picture`](/html/element/picture/) element, and it must be placed before the [`img`](/html/element/img/) element.

 |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLSourceElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("media") }}
: [Media query](/css/media_queries) of the resource's intended media; this should be used only in a [`picture`](/html/element/picture/) element.

{{ htmlattrdef("sizes") }}
: Is a list of source sizes that describes the final rendered width of the image represented by the source. Each source size consists of a comma-separated list of media condition-length pairs. This information is used by the browser to determine, before laying the page out, which image defined in {{ htmlattrxref("srcset", "source") }} to use. Please note that `sizes` will have its effect only if width dimension descriptors are provided with `srcset` instead of pixel ratio values (200w instead of 2x for example).

The `sizes` attribute has an effect only when the [`source`](/html/element/source/) element is the direct child of a [`picture`](/html/element/picture/) element.

{{ htmlattrdef("src") }}
: Required for [`audio`](/html/element/audio/) and [`video`](/html/element/video/), address of the media resource. The value of this attribute is ignored when the `<source>` element is placed inside a [`picture`](/html/element/picture/) element.

{{ htmlattrdef("srcset") }}
: A list of one or more strings separated by commas indicating a set of possible images represented by the source for the browser to use. Each string is composed of:

1.  One URL specifying an image.
2.  A width descriptor, which consists of a string containing a positive integer directly followed by `"w"`, such as `300w`. The default value, if missing, is the infinity.
3.  A pixel density descriptor, that is a positive floating number directly followed by `"x"`. The default value, if missing, is `1x`.

Each string in the list must have at least a width descriptor or a pixel density descriptor to be valid. Among the list, there must be only one string containing the same tuple of width descriptor and pixel density descriptor. The browser chooses the most adequate image to display at a given point of time.

The `srcset` attribute has an effect only when the [`source`](/html/element/source/) element is the direct child of a [`picture`](/html/element/picture/) element.

{{ htmlattrdef("type") }}
: The [MIME media type of the resource](/media/formats/image_types), optionally with a [`codecs` parameter](/media/formats/codecs_parameter).

If the `type` attribute isn't specified, the media's type is retrieved from the server and checked to see if the user agent can handle it; if it can't be rendered, the next `<source>` is checked. If the `type` attribute is specified, it's compared against the types the user agent can present, and if it's not recognized, the server doesn't even get queried; instead, the next `<source>` element is checked at once.

When used in the context of a `<picture>` element, the browser will fall back to using the image specified by the `<picture>` element's [`img`](/html/element/img/) child if it is unable to find a suitable image to use after examining every provided `<source>`.

## Usage notes

The `<source>` element is an **empty element (or void element)**, which means that it not only has no content but also has no closing tag. That is, you _never_ use "`</source>`" in your HTML.

For information about image formats supported by web browsers and guidance on selecting appropriate formats to use, see our [Image file type and format guide](/media/formats/image_types) on the web. For details on the video and audio media types, you can use, see the [Guide to media types formats used on the web](/media/formats).

## Examples

### Video example

This example demonstrates how to offer a video in Ogg format for users whose browsers support Ogg format, and a QuickTime format video for users whose browsers support that. If the `audio` or `video` element is not supported by the browser, a notice is displayed instead. If the browser supports the element but does not support any of the specified formats, an `error` event is raised and the default media controls (if enabled) will indicate an error. Be sure to reference our [guide to media types and formats on the web](/media/formats) for details on what media file formats you can use and how well they're supported by browsers.

```html
<video controls>
  <source src="foo.webm" type="video/webm">
  <source src="foo.ogg" type="video/ogg">
  <source src="foo.mov" type="video/quicktime">
  I'm sorry; your browser doesn't support HTML5 video.
</video>

```

For more examples, the learning area article [Video and audio content](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content) is a great resource.

### Picture example

In this example, two `<source>` elements are included within the [`picture`](/html/element/picture/), providing versions of an image to use when the available space exceeds certain widths. If the available width is less than the smaller of these widths, the user agent will fall back to the image given by the [`img`](/html/element/img/) element.

```html
<picture>
   <source srcset="mdn-logo-wide.png" media="(min-width: 800px)">
   <source srcset="mdn-logo-medium.png" media="(min-width: 600px)">
   <img src="mdn-logo-narrow.png" alt="MDN Web Docs">
</picture>

```

With the `<picture>` element, you must always include an `<[img](/html/element/img)>` with a fallback image, with an `alt` attribute to ensure accessibility (unless the image is an irrelevant background decorative image).

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<source>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-source-element) | {{ Spec2('HTML WHATWG') }} |  |

## Browser compatibility

{{ Compat("html.elements.source") }}

## See also

-   [Guide to media types and formats on the web](/media/formats)
-   [Image file type and format guide](/media/formats/image_types)
-   [`picture`](/html/element/picture/) element
-   [`audio`](/html/element/audio/) element
-   [`video`](/html/element/video/) element
-   [Web Performance](/en-US/docs/Learn/Performance)