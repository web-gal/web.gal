---
title: <area>
tags:
  - Content
  - Element
  - HTML
  - 'HTML:Flow content'
  - 'HTML:Phrasing content'
  - Multimedia
  - Reference
  - Web
permalink: html/element/area
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/area'
browserCompact: html.elements.area
---
{{ HTMLRef }}

The **HTML `<area>` element** defines an area inside an image map that has predefined clickable areas. An image map allows geometric areas on an image to be associated with [hypertext link](/glossary/hyperlink/).

This element is used only within a [`map`](/html/element/map/) element.

{{ EmbedInteractiveExample("pages/tabbed/area.html", "tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content). |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | Must have a start tag and must not have an end tag. |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). The `<area>` element must have an ancestor [`map`](/html/element/map/), but it need not be a direct parent. |
| Implicit ARIA role | [`link`](https://w3c.github.io/aria/#link) when {{ htmlattrxref("href", "area") }} attribute is present, otherwise [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLAreaElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("alt") }}
: A text string alternative to display on browsers that do not display images. The text should be phrased so that it presents the user with the same kind of choice as the image would offer when displayed without the alternative text. This attribute is required only if the {{ htmlattrxref("href", "area") }} attribute is used.

{{ htmlattrdef("coords") }}
: The `coords` attribute details the coordinates of the `[shape](#attr-shape)` attribute in size, shape, and placement of an `<area>`.

: -   `rect`: the value is `x1,y1,x2,y2`. Value specifies the coordinates of the top-left and bottom-right corner of the rectangle.  
    For example: `<area shape="rect" coords="0,0,253,27" href="#" target="_blank" alt="Mozilla">` The coords in the above example specify: 0,0 as the top-left corner and 253,27 as the bottom-right corner of the rectangle.
-   `circle`: the value is `x,y,radius`. Value specifies the coordinates of the circle center and the radius.  
    For example: `<area shape="circle" coords="130,136,60" href="#" target="_blank" alt="MDN">`
-   `poly`: the value is `x1,y1,x2,y2,..,xn,yn`. Value specifies the coordinates of the edges of the polygon. If the first and last coordinate pairs are not the same, the browser will add the last coordinate pair to close the polygon
-   `default`: defines the entire region

The values are numbers of CSS pixels.

{{ htmlattrdef("download") }}
: This attribute, if present, indicates that the author intends the hyperlink to be used for downloading a resource. See [`a`](/html/element/a/) for a full description of the {{ htmlattrxref("download", "a") }} attribute.

{{ htmlattrdef("href") }}
: The hyperlink target for the area. Its value is a valid URL. This attribute may be omitted; if so, the `<area>` element does not represent a hyperlink.

{{ htmlattrdef("hreflang") }}
: Indicates the language of the linked resource. Allowed values are determined by [BCP47](https://www.ietf.org/rfc/bcp/bcp47.txt "Tags for Identifying Languages"). Use this attribute only if the {{ htmlattrxref("href", "area") }} attribute is present.

{{ htmlattrdef("ping") }}
: Contains a space-separated list of URLs to which, when the hyperlink is followed, {{ HTTPMethod("POST") }} requests with the body `PING` will be sent by the browser (in the background). Typically used for tracking.

{{ htmlattrdef("referrerpolicy") }} {{ experimental_inline }}
: A string indicating which referrer to use when fetching the resource:

-   "`no-referrer`" meaning that the `Referer:` header will not be sent.
-   "`no-referrer-when-downgrade`" meaning that no `Referer:` header will be sent when navigating to an origin without TLS (HTTPS). This is a user agent’s default behavior, if no policy is otherwise specified.
-   "`origin`" meaning that the referrer will be the origin of the page, that is roughly the scheme, the host and the port.
-   "`origin-when-cross-origin`" meaning that navigations to other origins will be limited to the scheme, the host and the port, while navigations on the same origin will include the referrer's path.
-   "`unsafe-url`" meaning that the referrer will include the origin and the path (but not the fragment, password, or username). This case is unsafe because it can leak origins and paths from TLS-protected resources to insecure origins.

{{ htmlattrdef("rel") }}
: For anchors containing the {{ htmlattrxref("href", "area") }} attribute, this attribute specifies the relationship of the target object to the link object. The value is a space-separated list of [link types values](/html/link_types). The values and their semantics will be registered by some authority that might have meaning to the document author. The default relationship, if no other is given, is void. Use this attribute only if the {{ htmlattrxref("href", "area") }} attribute is present.

{{ htmlattrdef("shape") }}
: The shape of the associated hot spot. The specifications for HTML defines the values `rect`, which defines a rectangular region; `circle`, which defines a circular region; `poly`, which defines a polygon; and `default`, which indicates the entire region beyond any defined shapes.

: Many browsers, notably Internet Explorer 4 and higher, support `circ`, `polygon`, and `rectangle` as valid values for {{ htmlattrxref("shape", "area") }}, but these values are non-standard.

{{ htmlattrdef("target") }}
: A keyword or author-defined name of the [browsing context](/glossary/browsing_context/) to display the linked resource.

: The following keywords have special meanings:

-   `_self` (default): Show the resource in the current browsing context.
-   `_blank`: Show the resource in a new, unnamed browsing context.
-   `_parent`: Show the resource in the parent browsing context of the current one, if the current page is inside a frame. If there is no parent, acts the same as `_self`.
-   `_top`: Show the resource in the topmost browsing context (the browsing context that is an ancestor of the current one and has no parent). If there is no parent, acts the same as `_self`.

: Use this attribute only if the {{ htmlattrxref("href", "area") }} attribute is present.

**Note:** In newer browser versions (e.g. Firefox 79+) setting `target="_blank"` on `<area>` elements implicitly provides the same `rel` behavior as setting `rel="noopener"`.

### Deprecated attributes

{{ htmlattrdef("name") }} {{ deprecated_inline }}
: Define a names for the clickable area so that it can be scripted by older browsers.

{{ htmlattrdef("nohref") }} {{ deprecated_inline }}
: Indicates that no hyperlink exists for the associated area.

**Note:** Since HTML5, omitting the `href` attribute is sufficient.

{{ htmlattrdef("tabindex") }} {{ deprecated_inline }}
: A numeric value specifying the position of the defined area in the browser tabbing order. This attribute is global in HTML5.

{{ htmlattrdef("type") }} {{ deprecated_inline }}
: No effect. Browsers ignore it. (The W3C 5.3 fork of the HTML specification defines it as valid, but [the canonical HTML specification](https://html.spec.whatwg.org/multipage/#the-area-element) doesn’t, and it has no effect in any user agents.)

## Examples

```html
<map name="primary">
  <area shape="circle" coords="75,75,75" href="left.html" alt="Click to go Left">
  <area shape="circle" coords="275,75,75" href="right.html" alt="Click to go Right">
</map>
<img usemap="#primary" src="http://placehold.it/350x150" alt="350 x 150 pic">
```

### Result

{{ EmbedLiveSample('Examples', 360, 160)  }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**Referrer Policy** The definition of 'referrerpolicy attribute' in that specification](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy-delivery-referrer-attribute) | {{ Spec2('Referrer Policy') }} | Added the `referrerpolicy` attribute. |
| [**HTML Living Standard** The definition of '<area>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-area-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<area>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-area-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<area>' in that specification](https://www.w3.org/TR/html401/struct/objects.html#h-13.6.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.area") }}