---
title: '<content>: The Shadow DOM Content Placeholder element (obsolete)'
tags:
  - Content
  - DOM
  - Deprecated
  - Element
  - HTML
  - HTML Web Components
  - Placeholder
  - Reference
  - Web
  - Web Components
  - shadow dom
permalink: html/element/content
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/content'
deprecated: true
browserCompact: html.elements.content
---
The **HTML `<content>` element**—an obsolete part of the [Web Components](/web_components) suite of technologies—was used inside of [Shadow DOM](/web_components/shadow_dom) as an [insertion point](/glossary/insertion_point/), and wasn't meant to be used in ordinary HTML. It has now been replaced by the [`slot`](/html/element/slot/) element, which creates a point in the DOM at which a shadow DOM can be inserted.

**Note:** Though present in early draft of the specifications and implemented in several browsers, this element has been removed in later versions of the spec, and should not be used. It is documented here to assist in adapting code written during the time it was included in the spec to work with newer versions of the specification.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories "HTML/Content_categories") | [Transparent content](/html/content_categories#transparent_content_model "HTML/Content_categories#Transparent_content_model"). |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parent elements | Any element that accepts flow content. |
| DOM interface | {{ domxref("HTMLContentElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

`select`
: A comma-separated list of selectors. These have the same syntax as CSS selectors. They select the content to insert in place of the `<content>` element.

## Example

Here is a simple example of using the `<content>` element. It is an HTML file with everything needed in it.

**Note:** For this code to work, the browser you display it in must support Web Components. See [Enabling Web Components in Firefox](/web_components#enabling_web_components_in_firefox).

```html
<html>
  <head></head>
  <body>
  <!-- The original content accessed by <content> -->
  <div>
    <h4>My Content Heading</h4>
    <p>My content text</p>
  </div>

  <script>
  // Get the <div> above.
  var myContent = document.querySelector('div');
  // Create a shadow DOM on the <div>
  var shadowroot = myContent.createShadowRoot();
  // Insert into the shadow DOM a new heading and
  // part of the original content: the <p> tag.
  shadowroot.innerHTML =
   '<h2>Inserted Heading</h2> <content select="p"></content>';
  </script>

  </body>
</html>

```

If you display this in a web browser it should look like the following.

![content example](https://mdn.mozillademos.org/files/10077/content-example.png)

## Specifications

This element is no longer defined by any specifications.

## Browser compatibility

{{ Compat("html.elements.content") }}

## See also

-   [Web Components](/web_components)
-   [`shadow`](/html/element/shadow/), [`slot`](/html/element/slot/), [`template`](/html/element/template/), [`element`](/html/element/element/)

{{ HTMLRef }}