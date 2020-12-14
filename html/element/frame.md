---
title: <frame>
tags:
  - Deprecated
  - Element
  - HTML
  - Reference
  - Web
permalink: html/element/frame
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frame'
deprecated: true
browserCompact: html.elements.frame
---
{{ HTMLRef }}

`<frame>` is an HTML element which defines a particular area in which another HTML document can be displayed. A frame should be used within a [`frameset`](/html/element/frameset/).

Using the `<frame>` element is not encouraged because of certain disadvantages such as performance problems and lack of accessibility for users with screen readers. Instead of the `<frame>` element, [`iframe`](/html/element/iframe/) may be preferred.

## Attributes

Like all other HTML elements, this element supports the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("src") }}
: This attribute specifies the document that will be displayed by the frame.

{{ htmlattrdef("name") }}
: This attribute is used for labeling frames. Without labeling, every link will open in the frame that it’s in – the closest parent frame. See the {{ htmlattrxref("target","a") }} attribute for more information.

{{ htmlattrdef("noresize") }}
: This attribute prevents resizing of frames by users.

{{ htmlattrdef("scrolling") }}
: This attribute defines the existence of a scrollbar. If this attribute is not used, the browser adds a scrollbar when necessary. There are two choices: "yes" for forcing a scrollbar even when it is not necessary and "no" for forcing no scrollbar even when it _is_ necessary.

{{ htmlattrdef("marginheight") }}
: This attribute defines the height of the margin between frames.

{{ htmlattrdef("marginwidth") }}
: This attribute defines the width of the margin between frames.

{{ htmlattrdef("frameborder") }}
: This attribute allows you to specify a frame’s border.

## Example

```html
<frameset cols="50%,50%">
  <frame src="https://developer.mozilla.org/en/HTML/Element/iframe" />
  <frame src="https://developer.mozilla.org/en/HTML/Element/frame" />
</frameset>

```

## Browser compatibility

{{ Compat("html.elements.frame") }}

## See also

-   [`frameset`](/html/element/frameset/)
-   [`iframe`](/html/element/iframe/)