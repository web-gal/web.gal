---
title: '<img>: The Image Embed element'
tags:
  - Content
  - Element
  - Graphics
  - HTML
  - HTML Graphics
  - HTML Images
  - HTML Photos
  - HTML Pictures
  - HTML embedded content
  - Image
  - Image Element
  - Media
  - Multimedia
  - Photos
  - Pictures
  - Reference
  - Web
permalink: html/element/img
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img'
browserCompact: html.elements.img
---
{{ HTMLRef }}

The **HTML `<img>` element** embeds an image into the document.

{{ EmbedInteractiveExample("pages/tabbed/img.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The above example shows usage of the `<img>` element:

-   The `src` attribute is **required**, and contains the path to the image you want to embed.
-   The `alt` attribute holds a text description of the image, which isn't mandatory but is **incredibly useful** for accessibility — screen readers read this description out to their users so they know what the image means. Alt text is also displayed on the page if the image can't be loaded for some reason: for example, network errors, content blocking, or linkrot.

There are many other attributes to achieve various purposes:

-   [Referrer](/http/headers/referrer-policy)/[CORS](/glossary/cors/) control for security and privacy: see {{ htmlattrxref("crossorigin", "img") }} and {{ htmlattrxref("referrerpolicy", "img") }}.
-   Use both {{ htmlattrxref("width", "img") }} and {{ htmlattrxref("height", "img") }} to set the intrinsic size of the image, allowing it to take up space before it loads, to mitigate content layout shifts.
-   Responsive image hints with {{ htmlattrxref("sizes", "img") }} and {{ htmlattrxref("srcset", "img") }} (see also the [`picture`](/html/element/picture/) element and our [Responsive images](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) tutorial).

## Supported image formats

The HTML standard doesn't list what image formats to support, so each [user agent](/glossary/user_agent/) supports different formats.

{{ page("/en-US/docs/Web/Media/Formats/Image_types", "Common_image_file_types") }}

**Note:** See [Image file type and format guide](/media/formats/image_types) for more comprehensive information about image formats supported by web browsers. This includes image formats that are supported but not recommended for web content (e.g. ICO, BMP, etc.)

## Image loading errors

If an error occurs while loading or rendering an image, and an {{ htmlattrxref("onerror") }} event handler has been set on the {{ event("error") }} event, that event handler will get called. This can happen in a number of situations, including:

-   The `src` attribute is empty (`""`) or `null`.
-   The `src` [URL](/glossary/url/) is the same as the URL of the page the user is currently on.
-   The image is corrupted in some way that prevents it from being loaded.
-   The image's metadata is corrupted in such a way that it's impossible to retrieve its dimensions, and no dimensions were specified in the `<img>` element's attributes.
-   The image is in a format not supported by the [user agent](/glossary/user_agent/).

## Attributes

This element includes the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("alt") }}
: Defines an alternative text description of the image.

**Note:** Browsers do not always display images. There are a number of situations in which a browser might not display images, such as:

-   Non-visual browsers (such as those used by people with visual impairments)
-   The user chooses not to display images (saving bandwidth, privacy reasons)
-   The image is invalid or an [unsupported type](#Supported_image_formats)

In these cases, the browser may replace the image with the text in the element's `alt` attribute. For these reasons and others, provide a useful value for `alt` whenever possible.

Omitting `alt` altogether indicates that the image is a key part of the content and no textual equivalent is available. Setting this attribute to an empty string (`alt=""`) indicates that this image is _not_ a key part of the content (it’s decoration or a tracking pixel), and that non-visual browsers may omit it from [rendering](/glossary/rendering_engine/). Visual browsers will also hide the broken image icon if the `alt` is empty and the image failed to display.

This attribute is also used when copying and pasting the image to text, or saving a linked image to a bookmark.

{{ htmlattrdef("crossorigin") }}
: Indicates if the fetching of the image must be done using a [CORS](/glossary/cors/) request. Image data from a [CORS-enabled image](/en-US/docs/CORS_Enabled_Image) returned from a CORS request can be reused in the [`canvas`](/html/element/canvas/) element without being marked "[tainted](/html/cors_enabled_image#what_is_a_tainted_canvas)".

If the `crossorigin` attribute is _not_ specified, then a non-CORS request is sent (without the {{ httpheader("Origin") }} request header), and the browser marks the image as tainted and restricts access to its image data, preventing its usage in [`canvas`](/html/element/canvas/) elements.

If the `crossorigin` attribute _is_ specified, then a CORS request is sent (with the {{ httpheader("Origin") }} request header); but if the server does not opt into allowing cross-origin access to the image data by the origin site (by not sending any {{ httpheader("Access-Control-Allow-Origin") }} response header, or by not including the site's origin in any {{ httpheader("Access-Control-Allow-Origin") }} response header it does send), then the browser marks the image as tainted and restricts access to its image data, preventing its usage in [`canvas`](/html/element/canvas/) elements.

Allowed values:

`anonymous`
: A CORS request is sent with credentials omitted (that is, no [cookies](/glossary/cookie/), [X.509 certificates](https://tools.ietf.org/html/rfc5280), or {{ httpheader("Authorization") }} request header).

`use-credentials`
: The CORS request is sent with any credentials included (that is, cookies, X.509 certificates, and the `Authorization` request header). If the server does not opt into sharing credentials with the origin site (by sending back the `Access-Control-Allow-Credentials: true` response header), then the browser marks the image as tainted and restricts access to its image data.

If the attribute has an invalid value, browsers handle it as if the `anonymous` value was used. See [CORS settings attributes](/en-US/docs/HTML/CORS_settings_attributes) for additional information.

{{ htmlattrdef("decoding") }}
: Provides an image decoding hint to the browser. Allowed values:

: `sync`
: Decode the image synchronously, for atomic presentation with other content.

`async`
: Decode the image asynchronously, to reduce delay in presenting other content.

`auto`
: Default: no preference for the decoding mode. The browser decides what is best for the user.

{{ htmlattrdef("height") }}
: The intrinsic height of the image, in pixels. Must be an integer without a unit.

{{ htmlattrdef("intrinsicsize") }} {{ deprecated_inline }}
: This attribute tells the browser to ignore the actual [intrinsic size](/glossary/intrinsic_size/) of the image and pretend it’s the size specified in the attribute. Specifically, the image would raster at these dimensions and `naturalWidth`/`naturalHeight` on images would return the values specified in this attribute. [Explainer](https://github.com/ojanvafai/intrinsicsize-attribute), [examples](https://googlechrome.github.io/samples/intrinsic-size/index.html)

{{ htmlattrdef("ismap") }}
: This Boolean attribute indicates that the image is part of a [server-side map](https://en.wikipedia.org/wiki/Image_map#Server-side). If so, the coordinates where the user clicked on the image are sent to the server.

**Note:** This attribute is allowed only if the `<img>` element is a descendant of an [`a`](/html/element/a/) element with a valid {{ htmlattrxref("href","a") }} attribute. This gives users without pointing devices a fallback destination.

{{ htmlattrdef("loading") }}
: Indicates how the browser should load the image:

-   `eager`: Loads the image immediately, regardless of whether or not the image is currently within the visible viewport (this is the default value).
-   `lazy`: Defers loading the image until it reaches a calculated distance from the viewport, as defined by the browser. The intent is to avoid the network and storage bandwidth needed to handle the image until it's reasonably certain that it will be needed. This generally improves the performance of the content in most typical use cases.
    
    **Note:** Loading is only deferred when JavaScript is enabled. This is an anti-tracking measure, because if a user agent supported lazy loading when scripting is disabled, it would still be possible for a site to track a user's approximate scroll position throughout a session, by strategically placing images in a page's markup such that a server can track how many images are requested and when.

{{ htmlattrdef("referrerpolicy") }} {{ experimental_inline }}
: A string indicating which referrer to use when fetching the resource:

-   `no-referrer`: The {{ httpheader("Referer") }} header will not be sent.
-   `no-referrer-when-downgrade`: No `Referer` header is sent when navigating to an origin without [HTTPS](/glossary/https/). This is the default if no policy is otherwise specified.
-   `origin`: The `Referer` header will include the page's origin ([scheme](/glossary/scheme/), [host](/glossary/host/), and [port](/glossary/port/)).
-   `origin-when-cross-origin`: Navigating to other origins will limit the included referral data to the scheme, host, and port, while navigating from the same origin will include the full path and query string.
-   `unsafe-url`: The `Referer` header will always include the origin, path and query string, but not the fragment, password, or username. **This is unsafe** because it can leak information from TLS-protected resources to insecure origins.

{{ htmlattrdef("sizes") }}
: One or more strings separated by commas, indicating a set of source sizes. Each source size consists of:

1.  A [media condition](/css/media_queries/using_media_queries#syntax). This must be omitted for the last item in the list.
2.  A source size value.

Media Conditions describe properties of the _viewport_, not of the _image_. For example, `(max-height: 500px) 1000px` proposes to use a source of 1000px width, if the _viewport_ is not higher than 500px.

Source size values specify the intended display size of the image. [User agents](/glossary/user_agent/) use the current source size to select one of the sources supplied by the `srcset` attribute, when those sources are described using width (`w`) descriptors. The selected source size affects the [intrinsic size](/glossary/intrinsic_size/) of the image (the image’s display size if no [CSS](/glossary/css/) styling is applied). If the `srcset` attribute is absent, or contains no values with a width descriptor, then the `sizes` attribute has no effect.

{{ htmlattrdef("src") }}
: The image [URL](/glossary/url/). Mandatory for the `<img>` element. On [browsers](/glossary/browser/) supporting `srcset`, `src` is treated like a candidate image with a pixel density descriptor `1x`, unless an image with this pixel density descriptor is already defined in `srcset`, or unless `srcset` contains `w` descriptors.

{{ htmlattrdef("srcset") }}
: One or more strings separated by commas, indicating possible image sources for the [user agent](/glossary/user_agent/) to use. Each string is composed of:

1.  A [URL](/glossary/url/) to an image
2.  Optionally, whitespace followed by one of:
    -   A width descriptor (a positive integer directly followed by `w`). The width descriptor is divided by the source size given in the `sizes` attribute to calculate the effective pixel density.
    -   A pixel density descriptor (a positive floating point number directly followed by `x`).

If no descriptor is specified, the source is assigned the default descriptor of `1x`.

It is incorrect to mix width descriptors and pixel density descriptors in the same `srcset` attribute. Duplicate descriptors (for instance, two sources in the same `srcset` which are both described with `2x`) are also invalid.

The user agent selects any of the available sources at its discretion. This provides them with significant leeway to tailor their selection based on things like user preferences or [bandwidth](/glossary/bandwidth/) conditions. See our [Responsive images](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) tutorial for an example.

{{ htmlattrdef("width") }}
: The intrinsic width of the image in pixels. Must be an integer without a unit.

{{ htmlattrdef("usemap") }}
: The partial [URL](/glossary/url/) (starting with `#`) of an [image map](/en-US/docs/HTML/Element/map) associated with the element.

**Note:** You cannot use this attribute if the `<img>` element is inside an [`a`](/html/element/a/) or [`button`](/html/element/button/) element.

### Deprecated attributes

{{ htmlattrdef("align") }} {{ Obsolete_Inline }}
: Aligns the image with its surrounding context. Use the {{ cssxref('float') }} and/or {{ cssxref('vertical-align') }} [CSS](/glossary/css/) properties instead of this attribute. Allowed values:

: `top`
: Equivalent to `vertical-align: top` or `vertical-align: text-top`

`middle`
: Equivalent to `vertical-align: -moz-middle-with-baseline`

`bottom`
: The default, equivalent to `vertical-align: unset` or `vertical-align: initial`

`left`
: Equivalent to `float: left`

`right`
: Equivalent to `float: right`

{{ htmlattrdef("border") }} {{ Obsolete_Inline }}
: The width of a border around the image. Use the {{ cssxref('border') }} [CSS](/glossary/css/) property instead.

{{ htmlattrdef("hspace") }} {{ Obsolete_Inline }}
: The number of pixels of white space on the left and right of the image. Use the {{ cssxref('margin') }} CSS property instead.

{{ htmlattrdef("longdesc") }} {{ Obsolete_Inline }}
: A link to a more detailed description of the image. Possible values are a [URL](/glossary/url/) or an element {{ htmlattrxref("id") }}.

**Note:** This attribute is mentioned in the latest [W3C](/glossary/w3c/) version, [HTML 5.2](https://www.w3.org/TR/html52/obsolete.html#element-attrdef-img-longdesc), but has been removed from the [WHATWG](/glossary/whatwg/)’s [HTML Living Standard](https://html.spec.whatwg.org/multipage/embedded-content.html#the-img-element). It has an uncertain future; authors should use a [WAI](/glossary/wai/)-[ARIA](/glossary/aria/) alternative such as [`aria-describedby`](https://www.w3.org/TR/wai-aria-1.1/#aria-describedby) or [`aria-details`](https://www.w3.org/TR/wai-aria-1.1/#aria-details).

{{ htmlattrdef("name") }} {{ Obsolete_Inline }}
: A name for the element. Use the {{ htmlattrxref("id") }} attribute instead.

{{ htmlattrdef("vspace") }} {{ Obsolete_Inline }}
: The number of pixels of white space above and below the image. Use the {{ cssxref('margin') }} CSS property instead.

## Styling with CSS

`<img>` is a [replaced element](/css/replaced_element); it has a {{ cssxref("display") }} value of `inline` by default, but its default dimensions are defined by the embedded image's intrinsic values, like it were `inline-block`. You can set properties like {{ cssxref("border") }}/{{ cssxref("border-radius") }}, {{ cssxref("padding") }}/{{ cssxref("margin") }}, {{ cssxref("width") }}, {{ cssxref("height") }}, etc. on an image.

`<img>` has no baseline, so when images are used in an inline formatting context with {{ cssxref("vertical-align") }}`: baseline`, the bottom of the image will be placed on the text baseline.

You can use the {{ cssxref("object-position") }} property to position the image within the element's box, and the {{ cssxref("object-fit") }} property to adjust the sizing of the image within the box (for example, whether the image should fit the box or fill it even if clipping is required).

Depending on its type, an image may have an intrinsic width and height. For some image types, however, intrinsic dimensions are unnecessary. [SVG](/glossary/svg/) images, for instance, have no intrinsic dimensions if their root {{ SVGElement("svg") }} element doesn't have a `width` or `height` set on it.

## Examples

### Alternative text

The following example embeds an image into the page and includes alternative text for accessibility.

```html
<img src="https://developer.mozilla.org/static/img/favicon144.png"
     alt="MDN logo">

```

{{ EmbedLiveSample('Alternative_text', '100%', '160')  }}

### Image link

This example builds upon the previous one, showing how to turn the image into a link. To do so, nest the `<img>` tag inside the [`a`](/html/element/a/). You should made the alternative text describe the resource the link is pointing to, as if you were using a text link instead.

```html
<a href="https://developer.mozilla.org">
  <img src="https://developer.mozilla.org/static/img/favicon144.png"
       alt="Visit the MDN site">
</a>
```

{{ EmbedLiveSample('Image_link', '100%', '160')  }}

### Using the srcset attribute

In this example we include a `srcset` attribute with a reference to a high-resolution version of the logo; this will be loaded instead of the `src` image on high-resolution devices. The image referenced in the `src` attribute is counted as a `1x` candidate in [user agents](/glossary/user_agent/) that support `srcset`.

```html
 <img src="https://developer.mozilla.org/static/img/favicon72.png"
      alt="MDN logo"
      srcset="https://developer.mozilla.org/static/img/favicon144.png 2x">
```

{{ EmbedLiveSample("Using_the_srcset_attribute", "100%", "160") }}

### Using the srcset and sizes attributes

The `src` attribute is ignored in [user agents](/glossary/user_agent/) that support `srcset` when `w` descriptors are included. When the `(max-width: 600px)` media condition matches, the 200 pixel-wide image will load (it is the one that matches `200px` most closely), otherwise the other image will load.

```html
 <img src="/files/16864/clock-demo-200px.png"
      alt="Clock"
      srcset="/files/16864/clock-demo-200px.png 200w,
          /files/16797/clock-demo-400px.png 400w"
      sizes="(max-width: 600px) 200px, 50vw">
```

{{ EmbedLiveSample("Using_the_srcset_and_sizes_attributes", "100%", 350) }}

To see the resizing in action, [view the example on a separate page](https://mdn.mozillademos.org/en-US/docs/Web/HTML/Element/img$samples/Using_the_srcset_and_sizes_attributes), so you can actually resize the content area.

## Security and privacy concerns

Although `<img>` elements have innocent uses, they can have undesirable consequences for user security and privacy. See [Referer header: privacy and security concerns](/security/referer_header:_privacy_and_security_concerns) for more information and mitigations.

## Accessibility concerns

### Authoring meaningful alternate descriptions

An `alt` attribute's value should clearly and concisely describe the image's content. It should not describe the presence of the image itself or the file name of the image. If the `alt` attribute is purposefully left off because the image has no textual equivalent, consider alternate methods to present what the image is trying to communicate.

#### Don't

```html
<img alt="image" src="penguin.jpg">

```

#### Do

```html
<img alt="A Rockhopper Penguin standing on a beach." src="penguin.jpg">

```

When an `alt` attribute is not present on an image, some screen readers may announce the image's file name instead. This can be a confusing experience if the file name isn't representative of the image's contents.

-   [An alt Decision Tree • Images • WAI Web Accessibility Tutorials](https://www.w3.org/WAI/tutorials/images/decision-tree/)
-   [Alt-texts: The Ultimate Guide — Axess Lab](https://axesslab.com/alt-texts/)
-   [How to Design Great Alt Text: An Introduction | Deque](https://www.deque.com/blog/great-alt-text-introduction/)
-   [MDN Understanding WCAG, Guideline 1.1 explanations](/accessibility/understanding_wcag/perceivable#guideline_1.1_—_providing_text_alternatives_for_non-text_content)
-   [Understanding Success Criterion 1.1.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv-all.html)

### The title attribute

The {{ htmlattrxref("title") }} attribute is not an acceptable substitute for the `alt` attribute. Additionally, avoid duplicating the `alt` attribute's value in a `title` attribute declared on the same image. Doing so may cause some screen readers to announce the description twice, creating a confusing experience.

The `title` attribute should also not be used as supplemental captioning information to accompany an image's `alt` description. If an image needs a caption, use the `[figure](/html/element/figure)` and `[figcaption](/html/element/figcaption)` elements.

The value of the `title` attribute is usually presented to the user as a tooltip, which appears shortly after the cursor stops moving over the image. While this _can_ provide additional information to the user, you should not assume that the user will ever see it: the user may only have keyboard or touchscreen. If you have information that's particularly important or valuable for the user, present it inline using one of the methods mentioned above instead of using `title`.

-   [Using the HTML title attribute – updated | The Paciello Group](https://developer.paciellogroup.com/blog/2013/01/using-the-html-title-attribute-updated/)

## Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), [phrasing content](/guide/html/content_categories#phrasing_content), [embedded content](/guide/html/content_categories#embedded_content), [palpable content](/guide/html/content_categories#palpable_content). If the element has a `usemap` attribute, it also is a part of the interactive content category. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | Must have a start tag and must not have an end tag. |
| Permitted parents | Any element that accepts embedded content. |
| Implicit ARIA role | 
-   with non-empty `alt` attribute or no `alt` attribute: `[img](/accessibility/aria/roles/role_img)`
-   with empty `alt` attribute: [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role)

 |
| Permitted ARIA roles | 

-   with non-empty `alt` attribute:
    -   `[button](/accessibility/aria/roles/button_role)`
    -   `[checkbox](/accessibility/aria/roles/checkbox_role)`
    -   [`link`](https://w3c.github.io/aria/#link)
    -   [`menuitem`](https://w3c.github.io/aria/#menuitem)
    -   [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox)
    -   [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio)
    -   [`option`](https://w3c.github.io/aria/#option)
    -   [`progressbar`](https://w3c.github.io/aria/#progressbar)
    -   [`scrollbar`](https://w3c.github.io/aria/#scrollbar)
    -   [`separator`](https://w3c.github.io/aria/#separator)
    -   [`slider`](https://w3c.github.io/aria/#slider)
    -   `[switch](/accessibility/aria/roles/switch_role)`
    -   `[tab](/accessibility/aria/roles/tab_role)`
    -   [`treeitem`](https://w3c.github.io/aria/#treeitem)
-   with empty `alt` attribute, [`none`](https://w3c.github.io/aria/#none) or [`presentation`](https://w3c.github.io/aria/#presentation)
-   with no `alt` attribute, no `role` permitted

 |
| DOM interface | {{ domxref("HTMLImageElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**Referrer Policy** The definition of 'referrer attribute' in that specification](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy-delivery-referrer-attribute) | {{ Spec2('Referrer Policy') }} | Added the `referrerpolicy` attribute. |
| [**HTML Living Standard** The definition of '<img>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-img-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<img>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-img-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<img>' in that specification](https://www.w3.org/TR/html401/struct/objects.html#h-13.2) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.img") }}

## See also

-   [Images in HTML](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
-   [Image file type and format guide](/media/formats/image_types)
-   [Responsive images](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
-   [`picture`](/html/element/picture/), [`object`](/html/element/object/) and [`embed`](/html/element/embed/) elements
-   Other image-related CSS properties: {{ cssxref("object-fit") }}, {{ cssxref("object-position") }}, {{ cssxref("image-orientation") }}, {{ cssxref("image-rendering") }}, and {{ cssxref("image-resolution") }}.