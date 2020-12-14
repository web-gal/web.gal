---
title: '<a>: The Anchor element'
tags:
  - Content
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Interactive content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Inline element
  - Reference
  - Web
permalink: html/element/a
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a'
browserCompact: html.elements.a
---
{{ HTMLRef }}

The **HTML `<a>` element** (or _anchor_ element), with [its `href` attribute](#href), creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address. Content within each `<a>` **should** indicate the link's destination.

{{ EmbedInteractiveExample("pages/tabbed/a.html") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ HTMLAttrDef("download") }}{{ HTMLVersionInline(5) }}
: Prompts the user to save the linked URL instead of navigating to it. Can be used with or without a value:

: -   Without a value, the browser will suggest a filename/extension, generated from various sources:
    -   The {{ HTTPHeader("Content-Disposition") }} HTTP header
    -   The final segment in the URL [path](/api/url/pathname)
    -   The [media type](/glossary/mime_type/) (from the ({{ HTTPHeader("Content-Type") }} header, the start of a [`data:` URL](/http/basics_of_http/data_uris), or {{ domxref("Blob.type") }} for a [`blob:` URL](/api/url/createobjecturl))
-   Defining a value suggests it as the filename. `/` and `\` characters are converted to underscores (`_`). Filesystems may forbid other characters in filenames, so browsers will adjust the suggested name if necessary.

**Notes:**

-   `download` only works for [same-origin URLs](/security/same-origin_policy), or the `blob:` and `data:` schemes.
-   Note: if the `Content-Disposition` header has different information from the `download` attribute, resulting behaviour may differ:
    
    -   If the header specifies a `filename`, it takes priority over a filename specified in the `download` attribute.
        
    -   If the header specifies a disposition of `inline`, Chrome, and Firefox 82 and later, prioritize the attribute and treat it as a download. Firefox versions before 82 prioritize the header and will display the content inline.

{{ HTMLAttrDef("href") }}
: The URL that the hyperlink points to. Links are not restricted to HTTP-based URLs — they can use any URL scheme supported by browsers:

-   Sections of a page with fragment URLs
-   Pieces of media files with media fragments
-   Telephone numbers with `tel:` URLs
-   Email addresses with `mailto:` URLs
-   While web browsers may not support other URL schemes, web sites can with `[registerProtocolHandler()](/api/navigator/registerprotocolhandler)`

{{ HTMLAttrDef("hreflang") }}
: Hints at the human language of the linked URL. No built-in functionality. Allowed values are the same as [the global `lang` attribute](/html/global_attributes/lang).

{{ HTMLAttrDef("ping") }}
: A space-separated list of URLs. When the link is followed, the browser will send {{ HTTPMethod("POST") }} requests with the body `PING` to the URLs. Typically for tracking.

{{ HTMLAttrDef("referrerpolicy") }}{{ Experimental_Inline }}
: How much of the [referrer](/http/headers/referer) to send when following the link. See [`Referrer-Policy`](/http/headers/referrer-policy) for possible values and their effects.

{{ HTMLAttrDef("rel") }}
: The relationship of the linked URL as space-separated [link types](/html/link_types).

{{ HTMLAttrDef("target") }}
: Where to display the linked URL, as the name for a _browsing context_ (a tab, window, or `<iframe>`). The following keywords have special meanings for where to load the URL:

-   `_self`: the current browsing context. (Default)
-   `_blank`: usually a new tab, but users can configure browsers to open a new window instead.
-   `_parent`: the parent browsing context of the current one. If no parent, behaves as `_self`.
-   `_top`: the topmost browsing context (the "highest" context that’s an ancestor of the current one). If no ancestors, behaves as `_self`.

**Note:** When using `target`, add `rel="noreferrer noopener"` to avoid exploitation of the `window.opener` API;

**Note:** In newer browser versions (e.g. Firefox 79+) setting `target="_blank"` on `<a>` elements implicitly provides the same `rel` behavior as setting `rel="noopener"`.

{{ HTMLAttrDef("type") }}
: Hints at the linked URL’s format with a [MIME type](/glossary/mime_type/). No built-in functionality.

### Obsolete attributes

{{ HTMLAttrDef("charset") }}{{ Obsolete_Inline("HTML5") }}
: Hinted at the [character encoding](/glossary/character_encoding/) of the linked URL.

**Note:** This attribute is obsolete and **should not be used by authors**. Use the HTTP {{ HTTPHeader("Content-Type") }} header on the linked URL.

{{ HTMLAttrDef("coords") }}{{ Obsolete_Inline("HTML5") }}
: Used with [the `shape` attribute](#shape). A comma-separated list of coordinates.

{{ HTMLAttrDef("name") }}{{ Obsolete_Inline("HTML5") }}
: Was required to define a possible target location in a page. In HTML 4.01, `id` and `name` could both be used on `<a>`, as long as they had identical values.

**Note:** Use the global attribute {{ HTMLAttrxRef("id") }} instead.

{{ HTMLAttrDef("rev") }}{{ Obsolete_Inline("HTML5") }}
: Specified a reverse link; the opposite of [the `rel` attribute](#rel). Deprecated for being very confusing.

{{ HTMLAttrDef("shape") }}{{ Obsolete_Inline("HTML5") }}
: The shape of the hyperlink’s region in an image map.

**Note:** Use the [`area`](/html/element/area/) element for image maps instead.

## Properties

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), [interactive content](/html/content_categories#interactive_content), palpable content. |
| Permitted content | [Transparent](/html/content_categories#transparent_content_model), containing either [flow content](/html/content_categories#flow_content) (excluding [interactive content](/html/content_categories#interactive_content)) or [phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content), or any element that accepts [flow content](/html/content_categories#flow_content), but not other `<a>` elements. |
| Implicit ARIA role | [`link`](https://w3c.github.io/aria/#link) when `href` attribute is present, otherwise [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | 
When `href` attribute is present:

-   [`button`](https://w3c.github.io/aria/#button)
-   [`checkbox`](https://w3c.github.io/aria/#checkbox)
-   [`menuitem`](https://w3c.github.io/aria/#menuitem)
-   [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox)
-   [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio)
-   [`option`](https://w3c.github.io/aria/#option)
-   [`radio`](https://w3c.github.io/aria/#radio)
-   [`switch`](https://w3c.github.io/aria/#switch)
-   [`tab`](https://w3c.github.io/aria/#tab)
-   [`treeitem`](https://w3c.github.io/aria/#treeitem)

When `href` attribute is not present:

-   any

 |
| DOM interface | {{ DOMxRef("HTMLAnchorElement") }} |

## Examples

### Linking to an absolute URL

#### HTML

```html
<a href="https://www.mozilla.com">
  Mozilla
</a>
```

#### Result

{{ EmbedLiveSample('Linking_to_an_absolute_URL') }}

### Linking to relative URLs

#### HTML

```html
<a href="//example.com">Scheme-relative URL</a>
<a href="/en-US/docs/Web/HTML">Origin-relative URL</a>
<a href="./p">Directory-relative URL</a>

```

#### CSS

```css
a { display: block; margin-bottom: 0.5em }
```

#### Result

{{ EmbedLiveSample('Linking_to_relative_URLs') }}

### Linking to an element on the same page

```html
<!-- <a> element links to the section below -->
<p><a href="#Section_further_down">
  Jump to the heading below
</a></p>

<!-- Heading to link to -->
<h2 id="Section_further_down">Section further down</h2>

```

**Note:** You can use `href="#top"` or the empty fragment (`href="#"`) to link to the top of the current page, [as defined in the HTML specification](https://html.spec.whatwg.org/multipage/browsing-the-web.html#scroll-to-the-fragment-identifier).

### Linking to an email address

To create links that open in the user's email program to let them send a new message, use the `mailto:` scheme:

```html
<a href="mailto:nowhere@mozilla.org">Send email to nowhere</a>
```

For details about `mailto:` URLs, such as including a subject or body, see [Email links](/guide/html/email_links) or [RFC 6068](https://tools.ietf.org/html/rfc6068).

### Linking to telephone numbers

```html
<a href="tel:+49.157.0156">+49 157 0156</a>
<a href="tel:+1(555)5309">(555) 5309</a>
```

`tel:` link behavior varies with device capabilities:

-   Cellular devices autodial the number.
-   Most operating systems have programs that can make calls, like Skype or FaceTime.
-   Websites can make phone calls with {{ domxref("Navigator/registerProtocolHandler", "registerProtocolHandler") }}, such as `web.skype.com`.
-   Other behaviors include saving the number to contacts, or sending the number to another device.

See [RFC 3966](https://tools.ietf.org/html/rfc3966) for syntax, additional features, and other details about the `tel:` URL scheme.

### Using the download attribute to save a <canvas> as a PNG

To save a [`canvas`](/html/element/canvas/) element’s contents as an image, you can create a link with a `download` attribute and the canvas data as a `data:` URL:

#### Example painting app with save link

##### HTML

```html
<p>Paint by holding down the mouse button and moving it.
  <a href="" download="my_painting.png">Download my painting</a>
</p>

<canvas width="300" height="300"></canvas>

```

##### CSS

```css
html {
  font-family: sans-serif;
}
canvas {
  background: #fff;
  border: 1px dashed;
}
a {
  display: inline-block;
  background: #69c;
  color: #fff;
  padding: 5px 10px;
}
```

##### JavaScript

```js
var canvas = document.querySelector('canvas'),
    c = canvas.getContext('2d');
c.fillStyle = 'hotpink';

function draw(x, y) {
  if (isDrawing) {
    c.beginPath();
    c.arc(x, y, 10, 0, Math.PI*2);
    c.closePath();
    c.fill();
  }
}

canvas.addEventListener('mousemove', event =>
  draw(event.offsetX, event.offsetY)
);
canvas.addEventListener('mousedown', () => isDrawing = true);
canvas.addEventListener('mouseup', () => isDrawing = false);

document.querySelector('a').addEventListener('click', event =>
  event.target.href = canvas.toDataURL()
);

```

##### Result

{{ EmbedLiveSample('Example_painting_app_with_save_link', '100%', '400') }}

## Security and privacy

`<a>` elements can have consequences for users’ security and privacy. See [`Referer` header: privacy and security concerns](/security/referer_header:_privacy_and_security_concerns) for information.

Using `target="_blank"` without `rel="noreferrer"` and `rel="noopener"` makes the website vulnerable to {{ domxref("window.opener") }} API exploitation attacks ([vulnerability description](https://www.jitbit.com/alexblog/256-targetblank---the-most-underestimated-vulnerability-ever/)), although note that, in newer browser versions (e.g. Firefox 79+) setting `target="_blank"` implicitly provides the same protection as setting `rel="noopener"`.

## Accessibility

### Strong link text

**The content inside a link should indicate where the link goes**, even out of context.

#### Inaccessible, weak link text

A sadly common mistake is to only link the words “click here” or “here”:

```html
<p>
  Learn more about our products <a href="/products">here</a>.
</p>

```

#### Strong link text

Luckily, this is an easy fix, and it’s actually shorter than the inaccessible version!

```html
<p>
  Learn more <a href="/products">about our products</a>.
</p>
```

Assistive software have shortcuts to list all links on a page. However, strong link text benefits all users — the “list all links” shortcut emulates how sighted users quickly scan pages.

### onclick events

Anchor elements are often abused as fake buttons by setting their `href` to `#` or `javascript:void(0)` to prevent the page from refreshing, then listening for their `click` events .

These bogus `href` values cause unexpected behavior when copying/dragging links, opening links in a new tab/window, bookmarking, or when JavaScript is loading, errors, or is disabled. They also convey incorrect semantics to assistive technologies, like screen readers.

Use a [`button`](/html/element/button/) instead. In general, **you should only use a hyperlink for navigation to a real URL**.

### External links and linking to non-HTML resources

Links that open in a new tab/window via `target="_blank"`, or links that point to a download file should indicate what will happen when the link is followed.

People experiencing low vision conditions, navigating with the aid of screen reading technology, or with cognitive concerns may be confused when a new tab, window, or application opens unexpectedly. Older screen-reading software may not even announce the behavior.

#### Link that opens a new tab/window

```html
<a target="_blank" href="https://www.wikipedia.org">
  Wikipedia (opens in new tab)
</a>

```

#### Link to a non-HTML resource

```html
<a href="2017-annual-report.ppt">
  2017 Annual Report (PowerPoint)
</a>

```

If an icon is used to signify link behavior, make sure it has {{ HTMLAttrxRef("alt", "img", "alt text", "true") }}:

```html
<a  target="_blank" href="https://www.wikipedia.org">
  Wikipedia
  <img alt="(opens in new tab)" src="newtab.svg">
</a>

<a href="2017-annual-report.ppt">
  2017 Annual Report
  <img alt="(PowerPoint file)" src="ppt-icon.svg">
</a>
```

-   [WebAIM: Links and Hypertext - Hypertext Links](https://webaim.org/techniques/hypertext/hypertext_links)
-   [MDN / Understanding WCAG, Guideline 3.2](/accessibility/understanding_wcag/understandable#guideline_3.2_—_predictable_make_web_pages_appear_and_operate_in_predictable_ways)
-   [G200: Opening new windows and tabs from a link only when necessary](https://www.w3.org/TR/WCAG20-TECHS/G200.html)
-   [G201: Giving users advanced warning when opening a new window](https://www.w3.org/TR/WCAG20-TECHS/G201.html)

### Skip links

A **skip link** is a link placed as early as possible in [`body`](/html/element/body/) content that points to the beginning of the page's main content. Usually, CSS hides a skip link offscreen until focused.

```
<body>
  <a href="#content">Skip to main content</a>

  <header>
    …
  </header>

  <main id="content"> <!-- The skip link jumps to here -->

```
```css
.skip-link {
  position: absolute;
  top: -3em;
  background: #fff;
}
.skip-link:focus {
  top: 0;
}
```

Skip links let keyboard users bypass content repeated throughout multiple pages, such as header navigation.

Skip links are especially useful for people who navigate with the aid of assistive technology such as switch control, voice command, or mouth sticks/head wands, where the act of moving through repetitive links can be laborious.

-   [WebAIM: "Skip Navigation" Links](https://webaim.org/techniques/skipnav/)
-   [How-to: Use Skip Navigation links](https://a11yproject.com/posts/2013-05-11-skip-nav-links/)
-   [MDN / Understanding WCAG, Guideline 2.4 explanations](/accessibility/understanding_wcag/operable#guideline_2.4_%e2%80%94_navigable_provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are)
-   [Understanding Success Criterion 2.4.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html)

### Size and proximity

#### Size

Interactive elements, like links, should provide an area large enough that it is easy to activate them. This helps a variety of people, including those with motor control issues and those using imprecise inputs such as a touchscreen. A minimum size of 44×44 [CSS pixels](https://www.w3.org/TR/WCAG21/#dfn-css-pixels) is recommended.

Text-only links in prose content are exempt from this requirement, but it’s still a good idea to make sure enough text is hyperlinked to be easily activated.

-   [Understanding Success Criterion 2.5.5: Target Size](https://www.w3.org/WAI/WCAG21/Understanding/target-size.html)
-   [Target Size and 2.5.5](http://adrianroselli.com/2019/06/target-size-and-2-5-5.html)
-   [Quick test: Large touch targets](https://a11yproject.com/posts/large-touch-targets/)

#### Proximity

Interactive elements, like links, placed in close visual proximity should have space separating them. Spacing helps people with motor control issues, who may otherwise accidentally activate the wrong interactive content.

Spacing may be created using CSS properties like {{ CSSxRef("margin") }}.

-   [Hand tremors and the giant-button-problem](https://axesslab.com/hand-tremors/)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**Referrer Policy** The definition of 'referrer attribute' in that specification](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy-delivery-referrer-attribute) | {{ Spec2("Referrer Policy") }} | Added the `referrerpolicy` attribute. |
| [**HTML Living Standard** The definition of '<a>' in that specification](https://html.spec.whatwg.org/multipage/textlevel-semantics.html#the-a-element) | {{ Spec2("HTML WHATWG") }} |  |
| [**HTML 5** The definition of '<a>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-a-element) | {{ Spec2("HTML5 W3C") }} |  |
| [**HTML 4.01 Specification** The definition of '<a>' in that specification](https://www.w3.org/TR/html401/struct/links.html#h-12.2) | {{ Spec2("HTML4.01") }} |  |

## Browser compatibility

{{ Compat("html.elements.a") }}

## See also

-   [`link`](/html/element/link/) is similar to `<a>`, but for metadata hyperlinks that are invisible to users.
-   {{ CSSxRef(":link") }} is a CSS pseudo-class that will match `<a>` elements with valid `href` attributes.