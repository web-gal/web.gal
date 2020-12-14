---
title: '<picture>: The Picture element'
tags:
  - Element
  - Graphics
  - HTML
  - HTML embedded content
  - Images
  - Reference
  - Web
  - WebP
  - picture
permalink: html/element/picture
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture'
browserCompact: html.elements.picture
---
{{ HTMLRef }}

The **HTML `<picture>` element** contains zero or more [`source`](/html/element/source/) elements and one [`img`](/html/element/img/) element to offer alternative versions of an image for different display/device scenarios.

The browser will consider each child `<source>` element and choose the best match among them. If no matches are found—or the browser doesn't support the `<picture>` element—the URL of the `<img>` element's {{ htmlattrxref("src", "img") }} attribute is selected. The selected image is then presented in the space occupied by the `<img>` element.

{{ EmbedInteractiveExample("pages/tabbed/picture.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

To decide which URL to load, the [user agent](/glossary/user_agent/) examines each `<source>`'s {{ htmlattrxref("srcset", "source") }}, {{ htmlattrxref("media", "source") }}, and {{ htmlattrxref("type", "source") }} attributes to select a compatible image that best matches the current layout and capabilities of the display device.

The `<img>` element serves two purposes:

1.  It describes the size and other attributes of the image and its presentation.
2.  It provides a fallback in case none of the offered `<source>` elements are able to provide a usable image.

Common use cases for `<picture>`:

-   **Art direction.** Cropping or modifying images for different `media` conditions (for example, loading a simpler version of an image which has too many details, on smaller displays).
-   **Offering alternative image formats**, for cases where certain formats are not supported.
    
    **Note:** For example, newer formats like [AVIF](https://wiki.developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#AVIF) or [WEBP](https://wiki.developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#WebP) have many advantages, but  might not be supported by the browser. A list of supported image formats can be found in: [Image file type and format guide](/media/formats/image_types).
    
-   **Saving bandwidth and speeding page load times** by loading the most appropriate image for the viewer's display.

If providing higher-density versions of an image for high-DPI (Retina) display, use {{ htmlattrxref("srcset", "img") }} on the `<img>` element instead. This lets browsers opt for lower-density versions in data-saving modes, and you don't have to write explicit `media` conditions.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), phrasing content, embedded content |
| Permitted content | Zero or more [`source`](/html/element/source/) elements, followed by one [`img`](/html/element/img/) element, optionally intermixed with script-supporting elements. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that allows embedded content. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLPictureElement") }} |

## Attributes

This element includes only [global attributes](/html/global_attributes).

## Usage notes

You can use the {{ cssxref("object-position") }} property to adjust the positioning of the image within the element's frame, and the {{ cssxref("object-fit") }} property to control how the image is resized to fit within the frame.

**Note:** Use these properties on the child `<img>` element, **not** the `<picture>` element.

## Examples

These examples demonstrate how different attributes of the [`source`](/html/element/source/) element change the selection of the image inside `<picture>`.

### The media attribute

The `media` attribute specifies a media condition (similar to a media query) that the user agent will evaluate for each [`source`](/html/element/source/) element.

If the [`source`](/html/element/source/)'s media condition evaluates to `false`, the browser skips it and evaluates the next element inside `<picture>`.

```html
<picture>
  <source srcset="mdn-logo-wide.png" media="(min-width: 600px)">
  <img src="mdn-logo-narrow.png" alt="MDN">
</picture>

```

### The srcset attribute

The [{{ htmlattrdef("srcset") }}](/html/element/source#attr-srcset) attribute is used to offer list of possible images _based on size_.

It is composed of a comma-separated list of image descriptors. Each image descriptor is composed of a URL of the image, and _either..._

-   a _width descriptor_, followed by a `w` (such as `300w`);  
    _OR_
-   a _pixel density descriptor_, followed by an `x` (such as `2x`) to serve a high-res image for high-DPI screens.

```html
<picture>
  <source srcset="logo-768.png 768w, logo-768-1.5x.png 1.5x">
  <source srcset="logo-480.png, logo-480-2x.png 2x">
  <img src="logo-320.png" alt="logo">
</picture>
```

### The type attribute

The `type` attribute specifies a [MIME type](/http/basics_of_http/mime_types) for the resource URL(s) in the [`source`](/html/element/source/) element's `srcset` attribute. If the user agent does not support the given type, the [`source`](/html/element/source/) element is skipped.

```html
<picture>
  <source srcset="logo.webp" type="image/webp">
  <img src="logo.png" alt="logo">
</picture>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<picture>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-picture-element) | {{ Spec2('HTML WHATWG') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.picture") }}

## See also

-   [`img`](/html/element/img/) element
-   [`source`](/html/element/source/) element
-   Positioning and sizing the picture within its frame: {{ cssxref("object-position") }} and {{ cssxref("object-fit") }}
-   [Image file type and format guide](/media/formats/image_types)