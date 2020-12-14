---
title: '<shadow>: The obsolete Shadow Root element'
tags:
  - Deprecated
  - Element
  - HTML
  - HTML Web Components
  - Reference
  - Shadow Root
  - Web Components
  - shadow
  - shadow dom
permalink: html/element/shadow
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/shadow'
deprecated: true
browserCompact: html.elements.shadow
---
The **HTML `<shadow>` element**—an obsolete part of the [Web Components](/web_components) technology suite—was intended to be used as a shadow DOM [insertion point](/glossary/insertion_point/). You might have used it if you have created multiple shadow roots under a shadow host. It is not useful in ordinary HTML.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Transparent content](/html/content_categories#transparent_content_model) |
| Permitted content | [Flow content](/html/content_categories#flow_content) |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts flow content. |
| Permitted ARIA roles | None |
| DOM interface | {{ domxref("HTMLShadowElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

## Example

Here is a simple example of using the `<shadow>` element. It is an HTML file with everything needed in it.

**Note:** This is an experimental technology. For this code to work, the browser you display it in must support Web Components. See [Enabling Web Components in Firefox](/web_components#enabling_web_components_in_firefox).

```html
<html>
  <head></head>
  <body>

  <!-- This <div> will hold the shadow roots. -->
  <div>
    <!-- This heading will not be displayed -->
    <h4>My Original Heading</h4>
  </div>

  <script>
    // Get the <div> above with its content
    var origContent = document.querySelector('div');
    // Create the first shadow root
    var shadowroot1 = origContent.createShadowRoot();
    // Create the second shadow root
    var shadowroot2 = origContent.createShadowRoot();

    // Insert something into the older shadow root
    shadowroot1.innerHTML =
      '<p>Older shadow root inserted by
          &lt;shadow&gt;</p>';
    // Insert into younger shadow root, including <shadow>.
    // The previous markup will not be displayed unless
    // <shadow> is used below.
    shadowroot2.innerHTML =
      '<shadow></shadow> <p>Younger shadow
       root, displayed because it is the youngest.</p>';
  </script>

  </body>
</html>

```

If you display this in a web browser it should look like the following.

![shadow example](https://mdn.mozillademos.org/files/10083/shadow-example.png)

## Specifications

This element is no longer defined by any specifications.

## Browser compatibility

{{ Compat("html.elements.shadow") }}

## See also

-   [Web Components](/web_components)
-   [`content`](/html/element/content/), [`slot`](/html/element/slot/), [`template`](/html/element/template/), [`element`](/html/element/element/)

{{ HTMLRef }}