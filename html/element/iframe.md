---
title: '<iframe>: The Inline Frame element'
tags:
  - Content
  - Element
  - Embedded content
  - Embedding
  - Frames
  - HTML
  - HTML embedded content
  - Inline Frames
  - Reference
  - Web
  - embedded
  - iframe
permalink: html/element/iframe
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe'
browserCompact: html.elements.iframe
---
{{ HTMLRef }}

The **HTML Inline Frame element (`<iframe>`)** represents a nested [browsing context](/glossary/browsing_context/), embedding another HTML page into the current one.

{{ EmbedInteractiveExample("pages/tabbed/iframe.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

Each embedded browsing context has its own [session history](/api/history) and [document](/api/document). The browsing context that embeds the others is called the _parent browsing context_. The _topmost_ browsing context — the one with no parent — is usually the browser window, represented by the {{ domxref("Window") }} object.

Because each browsing context is a complete document environment, every `<iframe>` in a page requires increased memory and other computing resources. While theoretically you can use as many `<iframe>`s as you like, check for performance problems.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), embedded content, interactive content, palpable content. |
| Permitted content | None. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts embedded content. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`application`](https://w3c.github.io/aria/#application), [`document`](https://w3c.github.io/aria/#document), [`img`](https://w3c.github.io/aria/#img), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation) |
| DOM interface | {{ domxref("HTMLIFrameElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("allow") }}
: Specifies a [feature policy](/http/feature_policy) for the `<iframe>`. The policy defines what features are available to the `<iframe>` based on the origin of the request (e.g. access to the microphone, camera, battery, web-share API, etc.).  
  
For more information and examples see: [Using Feature Policy](/http/feature_policy/using_feature_policy) > [The iframe allow attribute](/http/feature_policy/using_feature_policy#the_iframe_allow_attribute).

{{ htmlattrdef("allowfullscreen") }}
: Set to `true` if the `<iframe>` can activate fullscreen mode by calling the {{ domxref("Element.requestFullscreen", "requestFullscreen()") }} method.

: This attribute is considered a legacy attribute and redefined as `allow="fullscreen"`.

{{ htmlattrdef("allowpaymentrequest") }}
: Set to `true` if a cross-origin `<iframe>` should be allowed to invoke the [Payment Request API](/api/payment_request_api).

: This attribute is considered a legacy attribute and redefined as `allow="payment"`.

{{ htmlattrdef("csp") }} {{ experimental_inline }}
: A [Content Security Policy](/http/csp) enforced for the embedded resource. See {{ domxref("HTMLIFrameElement.csp") }} for details.

{{ htmlattrdef("height") }}
: The height of the frame in CSS pixels. Default is `150`.

{{ htmlattrdef("loading") }} {{ experimental_inline }}
: Indicates how the browser should load the iframe:

-   `eager`: Load the iframe immediately, regardless if it is outside the visible viewport (this is the default value).
-   `lazy`: Defer loading of the iframe until it reaches a calculated distance from the viewport, as defined by the browser.

{{ htmlattrdef("name") }}
: A targetable name for the embedded browsing context. This can be used in the `target` attribute of the [`a`](/html/element/a/), [`form`](/html/element/form/), or [`base`](/html/element/base/) elements; the `formtarget` attribute of the [`input`](/html/element/input/) or [`button`](/html/element/button/) elements; or the `windowName` parameter in the {{ domxref("Window.open()","window.open()") }} method.

{{ htmlattrdef("referrerpolicy") }}
: Indicates which [referrer](/api/document/referrer) to send when fetching the frame's resource:

-   `no-referrer`: The {{ HTTPHeader("Referer") }} header will not be sent.
-   `no-referrer-when-downgrade` (default): The {{ HTTPHeader("Referer") }} header will not be sent to [origin](/glossary/origin/)s without [TLS](/glossary/tls/) ([HTTPS](/glossary/https/)).
-   `origin`: The sent referrer will be limited to the origin of the referring page: its [scheme](/en-US/docs/Archive/Mozilla/URIScheme), [host](/glossary/host/), and [port](/glossary/port/).
-   `origin-when-cross-origin`: The referrer sent to other origins will be limited to the scheme, the host, and the port. Navigations on the same origin will still include the path.
-   `same-origin`: A referrer will be sent for [same origin](/glossary/same-origin_policy/), but cross-origin requests will contain no referrer information.
-   `strict-origin`: Only send the origin of the document as the referrer when the protocol security level stays the same (HTTPS→HTTPS), but don't send it to a less secure destination (HTTPS→HTTP).
-   `strict-origin-when-cross-origin`: Send a full URL when performing a same-origin request, only send the origin when the protocol security level stays the same (HTTPS→HTTPS), and send no header to a less secure destination (HTTPS→HTTP).
-   `unsafe-url`: The referrer will include the origin _and_ the path (but not the [fragment](/api/htmlhyperlinkelementutils/hash), [password](/api/htmlhyperlinkelementutils/password), or [username](/api/htmlhyperlinkelementutils/username)). **This value is unsafe**, because it leaks origins and paths from TLS-protected resources to insecure origins.

{{ htmlattrdef("sandbox") }}
: Applies extra restrictions to the content in the frame. The value of the attribute can either be empty to apply all restrictions, or space-separated tokens to lift particular restrictions:

-   `allow-downloads-without-user-activation` {{ experimental_inline }}: Allows for downloads to occur without a gesture from the user.
-   `allow-downloads`: Allows for downloads to occur with a gesture from the user.
-   `allow-forms`: Allows the resource to submit forms. If this keyword is not used, form submission is blocked.
-   `allow-modals`: Lets the resource [open modal windows](https://html.spec.whatwg.org/multipage/origin.html#sandboxed-modals-flag).
-   `allow-orientation-lock`: Lets the resource [lock the screen orientation](/api/screen/lockorientation).
-   `allow-pointer-lock`: Lets the resource use the [Pointer Lock API](/en-US/docs/WebAPI/Pointer_Lock).
-   `allow-popups`: Allows popups (such as `window.open()`, `target="_blank"`, or `showModalDialog()`). If this keyword is not used, the popup will silently fail to open.
-   `allow-popups-to-escape-sandbox`: Lets the sandboxed document open new windows without those windows inheriting the sandboxing. For example, this can safely sandbox an advertisement without forcing the same restrictions upon the page the ad links to.
-   `allow-presentation`: Lets the resource start a [presentation session](/api/presentationrequest).
-   `allow-same-origin`: If this token is not used, the resource is treated as being from a special origin that always fails the [same-origin policy](/glossary/same-origin_policy/).
-   `allow-scripts`: Lets the resource run scripts (but not create popup windows).
-   `allow-storage-access-by-user-activation` {{ experimental_inline }}: Lets the resource request access to the parent's storage capabilities with the [Storage Access API](/api/storage_access_api).
-   `allow-top-navigation`: Lets the resource navigate the top-level browsing context (the one named `_top`).
-   `allow-top-navigation-by-user-activation`: Lets the resource navigate the top-level browsing context, but only if initiated by a user gesture.

**Notes about sandboxing:**

-   When the embedded document has the same origin as the embedding page, it is **strongly discouraged** to use both `allow-scripts` and `allow-same-origin`, as that lets the embedded document remove the `sandbox` attribute — making it no more secure than not using the `sandbox` attribute at all.
-   Sandboxing is useless if the attacker can display content outside a sandboxed `iframe` — such as if the viewer opens the frame in a new tab. Such content should be also served from a _separate origin_ to limit potential damage.
-   The `sandbox` attribute is unsupported in Internet Explorer 9 and earlier.

{{ htmlattrdef("src") }}
: The URL of the page to embed. Use a value of `about:blank` to embed an empty page that conforms to the [same-origin policy](/security/same-origin_policy#inherited_origins). Also note that programatically removing an `<iframe>`'s src attribute (e.g. via {{ domxref("Element.removeAttribute()") }}) causes `about:blank` to be loaded in the frame in Firefox (from version 65), Chromium-based browsers, and Safari/iOS.

{{ htmlattrdef("srcdoc") }}
: Inline HTML to embed, overriding the `src` attribute. If a browser does not support the `srcdoc` attribute, it will fall back to the URL in the `src` attribute.

{{ htmlattrdef("width") }}
: The width of the frame in CSS pixels. Default is `300`.

### Deprecated attributes

These attributes are deprecated and may no longer be supported by all user agents. You should not use them in new content, and try to remove them from existing content.

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: The alignment of this element with respect to the surrounding context.

{{ htmlattrdef("frameborder") }} {{ deprecated_inline }}
: The value `1` (the default) draws a border around this frame. The value `0` removes the border around this frame, but you should instead use the CSS property {{ cssxref("border") }} to control `<iframe>` borders.

{{ htmlattrdef("longdesc") }} {{ deprecated_inline }}
: A URL of a long description of the frame's content. Due to widespread misuse, this is not helpful for non-visual browsers.

{{ htmlattrdef("marginheight") }} {{ deprecated_inline }}
: The amount of space in pixels between the frame's content and its top and bottom borders.

{{ htmlattrdef("marginwidth") }} {{ deprecated_inline }}
: The amount of space in pixels between the frame's content and its left and right borders.

{{ htmlattrdef("scrolling") }} {{ deprecated_inline }}
: Indicates when the browser should provide a scrollbar for the frame:

-   `auto`: Only when the frame's content is larger than its dimensions.
-   `yes`: Always show a scrollbar.
-   `no`: Never show a scrollbar.

### Non-standard attributes

{{ htmlattrdef("mozbrowser") }} {{ non-standard_inline }}
: See [bug 1318532](https://bugzilla.mozilla.org/show_bug.cgi?id=1318532) for exposing this to WebExtensions in Firefox.

Makes the `<iframe>` act like a top-level browser window. See [Browser API](/en-US/docs/Mozilla/Gecko/Chrome/API/Browser_API) for details.  
**Available only to [WebExtensions](/en-US/docs/Mozilla/Add-ons/WebExtensions).**

## Scripting

Inline frames, like [`frame`](/html/element/frame/) elements, are included in the {{ domxref("window.frames") }} pseudo-array.

With the DOM {{ domxref("HTMLIFrameElement") }} object, scripts can access the {{ domxref("window") }} object of the framed resource via the {{ domxref("HTMLIFrameElement.contentWindow", "contentWindow") }} property. The {{ domxref("HTMLIFrameElement.contentDocument", "contentDocument") }} property refers to the `document` inside the `<iframe>`, same as `contentWindow.document`.

From the inside of a frame, a script can get a reference to its parent window with {{ domxref("window.parent") }}.

Script access to a frame's content is subject to the [same-origin policy](/security/same-origin_policy). Scripts cannot access most properties in other `window` objects if the script was loaded from a different origin, including scripts inside a frame accessing the frame's parent. Cross-origin communication can be achieved using {{ domxref("Window.postMessage()") }}.

## Positioning and scaling

As a [replaced element](/css/replaced_element), the position, alignment, and scaling of the embedded document within the `<iframe>` element's box, can be adjusted with the {{ cssxref("object-position") }} and {{ cssxref("object-fit") }} properties.

## Examples

### A simple <iframe>

An `<iframe>` in action. After creating the frame, when the user clicks a button, its title is displayed in an alert.

#### HTML

```html
<iframe src="https://mdn-samples.mozilla.org/snippets/html/iframe-simple-contents.html"
            title="iframe Example 1" width="400" height="300">
</iframe>
```

#### Result

{{ EmbedLiveSample('Example1', 640,400) }}

## Accessibility concerns

People navigating with assistive technology such as a screen reader can use the [`title` attribute](/html/global_attributes/title) on an `<iframe>` to label its content. The title's value should concisely describe the embedded content:

```html
<iframe title="Wikipedia page for Avocados" src="https://en.wikipedia.org/wiki/Avocado"></iframe>
```

Without this title, they have to navigate into the `<iframe>` to determine what its embedded content is. This context shift can be confusing and time-consuming, especially for pages with multiple `<iframe>`s and/or if embeds contain interactive content like video or audio.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**Referrer Policy** The definition of 'referrerpolicy attribute' in that specification](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy-delivery-referrer-attribute) | {{ Spec2('Referrer Policy') }} | Added the `referrerpolicy` attribute. |
| [**HTML Living Standard** The definition of '<iframe>' in that specification](https://html.spec.whatwg.org/multipage/iframe-embed-object.html#the-iframe-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<iframe>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-iframe-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<iframe>' in that specification](https://www.w3.org/TR/html401/present/frames.html#h-16.5) | {{ Spec2('HTML4.01') }} |  |
| [**Screen Orientation API**](https://w3c.github.io/screen-orientation/) | {{ Spec2('Screen Orientation') }} | Adds `allow-orientation-lock` to the `sandbox` attribute. |

## Browser compatibility

{{ Compat("html.elements.iframe", 3) }}

## See also

-   [Privacy, permissions, and information security](/privacy)